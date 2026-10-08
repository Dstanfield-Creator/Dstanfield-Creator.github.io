---
title: "The UFW rule was correct and still locked me out"
---

# The UFW rule was correct and still locked me out

*A conntrack lesson from enabling a firewall over SSH, and the dead-man switch that saved it.*

I was enabling UFW for the first time on a headless VM, over SSH, with a rule set I had checked twice:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow from 192.0.2.0/24 to any port 22 proto tcp
sudo ufw enable
```

The moment `ufw enable` ran, the session froze. No error, no disconnect, just a dead terminal. The rules were right. SSH from the management subnet was explicitly allowed. So what happened?

## Connection tracking, mid-stream

The firewall loads its state table empty. My SSH connection already existed when UFW came up, so conntrack picked it up in the middle of the conversation, without having seen the TCP handshake. It never learned the window-scaling the two ends had negotiated. Once the window grew past what conntrack believed was valid, the kernel marked those packets `INVALID`, and UFW's default `ufw-before-input` chain drops `INVALID`:

```
-A ufw-before-input -m conntrack --ctstate INVALID -j DROP
```

A connection opened *after* the firewall is up is tracked from its SYN and never hits this. The existing one had nowhere to go.

## What saved it

Thirty seconds before enabling, I had armed a transient timer:

```bash
sudo systemd-run --unit=fw-deadman --on-active=180 /usr/sbin/ufw disable
```

Three minutes later UFW disabled itself and SSH came back. I enabled the firewall properly the second time, out-of-band, from the hypervisor, so no SSH session was in the loop at all:

```bash
qm guest exec <vmid> -- ufw --force enable
```

## The procedure that came out of it

1. Arm a rollback timer before touching the firewall.
2. Make the change out-of-band where possible.
3. Test from a brand-new SSH session, never the one that made the change.
4. Only disarm the timer once the new session works. If it fails, do nothing and let the timer roll back.

I wrapped it in a small script, [`fw-deadman`](https://github.com/Dstanfield-Creator/projects/tree/master/tools/firewall-deadman-switch), and wrote it up as a [runbook](https://github.com/Dstanfield-Creator/guides/blob/master/runbooks/remote-firewall-change.md). The rule being correct was never the question. The question was whether I could still get in if it was not.
