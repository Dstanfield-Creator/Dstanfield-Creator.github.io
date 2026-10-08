---
title: "A backup job that failed silently for a month"
---

# A backup job that failed silently for a month

*How a full root disk broke weekly backups without anyone noticing, and what I changed so it cannot happen quietly again.*

The weekly `vzdump` job on my Proxmox node wrote its archives to `local`, the 96 GB root disk. For over a month, every Sunday run failed with:

```
ERROR: Backup of VM 106 failed - write error - Broken pipe
```

Nobody saw it, because nothing was watching the job, and a full root disk does not announce itself. It also quietly blocked ISO downloads and template builds. The dumps had filled the disk, and each new run tried to write into no free space.

## Root cause, not symptom

The symptom was "backups fail". The cause was "the root disk is the wrong place for backups". `/var/lib/vz/dump` had grown to 63 GB of the 96 GB root. Clearing it would have fixed the symptom until the next month. The real fix was to stop backing up to the root disk at all.

## The rebuild

I stood up a dedicated Proxmox Backup Server as its own VM, with its datastore on a separate 250 GB disk that is itself excluded from `vzdump`:

- VM with `protection=1`, so a tired human or a runaway token cannot delete it.
- A `pbs` storage entry on the node, authenticated with a scoped API token.
- Prune policy: keep 4 weekly and 3 monthly. Deduplication means seven weekly copies of a Windows DC cost barely more than one.

One gotcha cost an hour: **a PBS token's privileges are capped by its owning user**, so granting the datastore role to the token alone fails with a permission error. The ACL has to be on the user as well.

## What I changed so it stays visible

- Backups now go to PBS, never the root disk.
- A monitoring rule alerts when any VM's newest backup is older than eight days, which is the exact failure I missed.
- A rule alerts when `local` passes 85 percent, which is what filled up in the first place.

Those two alerts are the point. The backup target moving was necessary, but the thing that actually failed was that a weekly job could die every week and stay silent. The full write-up is in the [Proxmox Backup Server](https://github.com/Dstanfield-Creator/lab-ops/tree/main/docs/proxmox-backup-server) project.
