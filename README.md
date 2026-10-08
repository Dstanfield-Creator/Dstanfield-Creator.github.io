# Danny Stanfield

**Junior SecOps Analyst · Perth, Western Australia**

SIEM and EDR triage, detection engineering, Zero Trust operations, and a Proxmox homelab that gets documented as it gets built. This page indexes every write-up, reference and tool across my GitHub, organised by department.

- GitHub: [github.com/Dstanfield-Creator](https://github.com/Dstanfield-Creator)
- LinkedIn: [linkedin.com/in/danny-stanfield](https://linkedin.com/in/danny-stanfield)

## Flagship repositories

- [detections](https://github.com/Dstanfield-Creator/cyber-resources/tree/master/detections) - detection-as-code: Sigma rules mapped to MITRE ATT&CK, validated in CI
- [lab-ops](https://github.com/Dstanfield-Creator/lab-ops) - the homelab as code and in prose: Ansible, Compose, Terraform, lab scripts and the build write-ups
- [network](https://github.com/Dstanfield-Creator/network) - zero-trust access, campus design, firewall tooling and the dead-man switch

---

## 🏢 Work by Department

Six departments, each with its own repositories. Nothing lives outside its department.

| Department | Repositories |
|---|---|
| 🛡️ Security Operations | cyber-resources (detections/, monitoring/, reference, labs) |
| 🖥️ Infrastructure & Platform | lab-ops, server-administration |
| 🌐 Network | network |
| ☁️ Cloud | cloud-infrastructure |
| 🤖 AI & Automation | ai-automation |
| 🔧 General IT & Service Desk | general-it, Powershell-Scripts |

### 🛡️ Security Operations

**[cyber-resources](https://github.com/Dstanfield-Creator/cyber-resources)** - detection-as-code, monitoring, a technique and tool reference written from the defender's side, and the lab ranges it is practised in

- **Detections** ([detections/](https://github.com/Dstanfield-Creator/cyber-resources/tree/master/detections)): [Rules](https://github.com/Dstanfield-Creator/cyber-resources/tree/master/detections/rules) - Windows (6), Linux (3), web (2), network (1), cloud (1), each mapped to MITRE ATT&CK and structurally validated in CI · [How rules are tested](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/detections/docs/testing.md) · [Windows AD Logging Baseline for Detection](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/detections/docs/windows-ad-logging-baseline-for-detection.md) - Advanced Audit Policy, Sysmon, forwarding, attack-to-event map
- **Monitoring & Observability** ([monitoring/](https://github.com/Dstanfield-Creator/cyber-resources/tree/master/monitoring)): [MyDashboard](https://github.com/Dstanfield-Creator/cyber-resources/tree/master/monitoring/mydashboard) - Prometheus + Grafana lab health dashboard design with alerts derived from real incidents · [Monitoring Stack (Compose)](https://github.com/Dstanfield-Creator/cyber-resources/tree/master/monitoring/compose/monitoring-stack) - Prometheus, Alertmanager, Grafana, node_exporter, cAdvisor, blackbox SSH probes, starter alerts · [Lab Monitoring (Compose)](https://github.com/Dstanfield-Creator/cyber-resources/tree/master/monitoring/compose/lab-monitoring) - the version deployed in the lab · [Prometheus node_exporter Setup](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/monitoring/docs/prometheus-node-exporter-setup.md) - sandboxed unit, textfile collector, scrape config, useful PromQL
- **Defensive operations:** [Detection Engineering](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/detection-engineering.md) · [Threat Hunting](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/threat-hunting.md) · [Incident Response](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/incident-response.md) · [SIEM Configuration](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/siem-configuration.md) · [Intrusion Detection](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/intrusion-detection.md) · [Forensics](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/forensics.md) · [Honeypots](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/honeypots.md) · [Firewall Configuration](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/firewall-configuration.md) · [Network Segmentation](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/network-segmentation.md)
- **Attack write-ups:** [Brute Force](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/brute-force-attacks.md) · [DoS](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/dos-attacks.md) · [DDoS](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/ddos-attacks.md) · [Phishing](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/phishing.md) · [Social Engineering](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/social-engineering.md) · [Lateral Movement](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/lateral-movement.md) · [Persistence](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/persistence.md) · [Privilege Escalation](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/privilege-escalation.md) · [Web Application Attacks](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/web-application-attacks.md) · [Cross-Site Scripting](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/cross-site-scripting.md) · [File Inclusion](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/file-inclusion.md) · [Network Protocol Attacks](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/network-protocol-attacks.md)
- **Techniques:** [Enumeration](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/enumeration.md) · [Port Scanning](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/port-scanning.md) · [Network Scanning](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/network-scanning.md) · [Service Discovery](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/service-discovery.md) · [DNS Enumeration](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/dns-enumeration.md) · [Web App Enumeration](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/web-application-enumeration.md) · [Vulnerability Scanning](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/vulnerability-scanning.md) · [OSINT](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/osint.md) · [Online Password Attacks](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/password-attacks-online.md) · [Password Cracking](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/password-cracking.md) · [Authentication Bypass](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/authentication-bypass.md) · [SQL Injection](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/sql-injection.md) · [Command Injection](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/command-injection.md) · [Reverse Shells](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/reverse-shells.md) · [Post-Exploitation](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/post-exploitation.md) · [C2 Communication](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/c2-communication.md) · [Exfiltration](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/exfiltration.md) · [Protocol Analysis](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/protocol-analysis.md) · [Log Analysis](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/log-analysis.md) · [Social Engineering](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/social-engineering.md)
- **Tools:** [Nmap](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/nmap.md) · [Wireshark](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/wireshark.md) · [Burp Suite](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/burp-suite.md) · [Metasploit](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/metasploit-framework.md) · [sqlmap](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/sqlmap.md) · [Nikto](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/nikto.md) · [Hydra](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/hydra.md) · [Hashcat](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/hashcat.md) · [John the Ripper](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/john-the-ripper.md) · [Mimikatz](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/mimikatz.md) · [Aircrack-ng](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/aircrack-ng.md) · [Kali Linux](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/kali-linux.md)
- **Labs:** [Ludus Cyber Range](https://github.com/Dstanfield-Creator/cyber-resources/tree/master/labs/ludus-cyber-range) - reproducible AD attack / detection range: router, Server 2022 DC, Win 11 workstation, Kali · [HackTheBox tracker](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/labs/htb/README.md) · [write-up template](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/labs/htb/_template.md)

### 🖥️ Infrastructure & Platform

**[lab-ops](https://github.com/Dstanfield-Creator/lab-ops)** - the single-node Proxmox homelab as code and in prose

- **As code:** [Ansible host baseline](https://github.com/Dstanfield-Creator/lab-ops/tree/main/ansible) - admin user, sshd hardening drop-in, UFW, unattended upgrades · [Compose services](https://github.com/Dstanfield-Creator/lab-ops/tree/main/compose/services) - Nginx Proxy Manager, n8n, Uptime Kuma · [Terraform: Proxmox VM](https://github.com/Dstanfield-Creator/lab-ops/tree/main/terraform/proxmox-vm) - Debian 12 cloud image, cloud-init snippet, VirtIO on LVM-thin · [Proxmox host notes](https://github.com/Dstanfield-Creator/lab-ops/blob/main/proxmox/README.md) · [Renovate](https://github.com/Dstanfield-Creator/lab-ops/blob/main/renovate.json)
- **Build write-ups:** [Proxmox Lab Platform](https://github.com/Dstanfield-Creator/lab-ops/tree/main/docs/proxmox-lab-platform) - single-node PVE 9 host: storage, bridges, guest inventory, operating modes, power management · [Proxmox Backup Server](https://github.com/Dstanfield-Creator/lab-ops/tree/main/docs/proxmox-backup-server) - dedicated PBS 4 VM, token ACL gotchas, prune policy, root cause of silent backup failures · [Docker Services Host](https://github.com/Dstanfield-Creator/lab-ops/tree/main/docs/docker-services-host) - service platform migrated from a Raspberry Pi 5 to a PVE VM · [Minecraft Server](https://github.com/Dstanfield-Creator/lab-ops/tree/main/docs/minecraft-server) - systemd-managed game server on bare metal, Tailscale access · [Cloud-init for Proxmox and Cloud VMs](https://github.com/Dstanfield-Creator/lab-ops/blob/main/docs/cloud-init-for-proxmox-and-cloud-vms.md)
- **Scripts:** [Lab Power Scripts](https://github.com/Dstanfield-Creator/lab-ops/tree/main/scripts/lab-power-scripts) - `lab-up` / `lab-down`: Wake-on-LAN + Proxmox API orchestration with research / ds-lab modes · [lab-ssh-check](https://github.com/Dstanfield-Creator/lab-ops/tree/main/scripts/lab-ssh-check) - parallel SSH reachability and key-auth checker that classifies every failure

**[server-administration](https://github.com/Dstanfield-Creator/server-administration)** - hardening, guides and reference for Linux, Windows and Proxmox

- **Hardening:** [OpenSSH Server Hardening](https://github.com/Dstanfield-Creator/server-administration/blob/master/hardening/openssh-server-hardening.md) - key-only drop-in, modern crypto, host key cleanup, restricted automation keys, ssh-audit · [systemd Service Sandboxing](https://github.com/Dstanfield-Creator/server-administration/blob/master/hardening/systemd-service-sandboxing.md) - confinement directives, JIT runtime caveats, systemd-analyze security scoring
- **Guides:** [Proxmox API Tokens with Least Privilege](https://github.com/Dstanfield-Creator/server-administration/blob/master/guides/proxmox-api-token-least-privilege.md) - custom roles, path-scoped ACLs, protected VMs, safe secret handling · [New Proxmox VM Checklist](https://github.com/Dstanfield-Creator/server-administration/blob/master/guides/new-proxmox-vm-checklist.md) - tickable path from created to in service · [SSH Key Authentication Failures](https://github.com/Dstanfield-Creator/server-administration/blob/master/guides/ssh-key-auth-failures.md) - classify DNS / DOWN / AUTH / HOSTKEY / HOSTKEY! / AGENT and fix the right layer
- **Reference:** [Proxmox VE CLI Cheatsheet](https://github.com/Dstanfield-Creator/server-administration/blob/master/reference/proxmox-cli-cheatsheet.md) - qm, pct, pvesm, pveum, vzdump, pvesh, task logs, storage housekeeping

**Write-up:** [A backup job that failed silently for a month](https://dstanfield-creator.github.io/writeups/silent-backup-failure.html)

### 🌐 Network

**[network](https://github.com/Dstanfield-Creator/network)** - zero-trust remote access, campus design, firewalls and connectivity troubleshooting

- **Remote access:** [Tailscale Remote Access](https://github.com/Dstanfield-Creator/network/tree/main/remote-access/tailscale-remote-access) - WireGuard mesh, MagicDNS names as SSH handles, 1Password SSH agent, no port-forwards · [Raspberry Pi Travel Router](https://github.com/Dstanfield-Creator/network/tree/main/remote-access/pi-travel-router) - OpenWrt pocket router with a Tailscale exit node
- **Design:** [Cisco Enterprise Network Design](https://github.com/Dstanfield-Creator/network/tree/main/design/cisco-enterprise-network-design) - multi-VLAN campus: core SVIs, DHCP relay, hardened access ports, ASA NAT and policy, verification commands
- **Firewall:** [Firewall Dead-Man Switch](https://github.com/Dstanfield-Creator/network/tree/main/firewall/firewall-deadman-switch) - systemd timer that rolls back a remote firewall change if it locks you out · [Remote Firewall Change Without Lockout](https://github.com/Dstanfield-Creator/network/blob/main/firewall/remote-firewall-change.md) - arm the rollback, change out-of-band, test from a new session, disarm · [UFW Baseline for Headless Servers](https://github.com/Dstanfield-Creator/network/blob/main/firewall/ufw-baseline-linux.md) - default deny, management-subnet SSH, Tailscale interface, rate limiting
- **Troubleshooting:** [DNS, DHCP and Connectivity](https://github.com/Dstanfield-Creator/network/blob/main/troubleshooting/dns-dhcp-and-connectivity.md) - layered diagnosis on Windows and Linux, failure signatures, DHCP relay checks
- **Case study:** [Network Optimisation & Security Enhancement](https://github.com/Dstanfield-Creator/network/tree/main/case-studies/network-security-enhancement) - segmentation, Fortinet firewall/IDS, Veeam/Acronis backup, PowerShell automation
- **Attack-side reference (cyber-resources):** [Firewall Configuration](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/firewall-configuration.md) · [Network Segmentation](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/network-segmentation.md) · [Network Protocol Attacks](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/docs/network-protocol-attacks.md) · [Network Scanning](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/network-scanning.md) · [Port Scanning](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/port-scanning.md) · [DNS Enumeration](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/dns-enumeration.md) · [Protocol Analysis](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/techniques/protocol-analysis.md) · [Wireshark](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/wireshark.md) · [Nmap](https://github.com/Dstanfield-Creator/cyber-resources/blob/master/tools/nmap.md)

**Write-up:** [The UFW rule was correct and still locked me out](https://dstanfield-creator.github.io/writeups/ufw-lockout.html)

### ☁️ Cloud

**[cloud-infrastructure](https://github.com/Dstanfield-Creator/cloud-infrastructure)** - Infrastructure as Code and cloud reference

- [Terraform: AWS VPC/EC2 Baseline](https://github.com/Dstanfield-Creator/cloud-infrastructure/tree/master/terraform/aws-vpc-ec2-baseline) - two-AZ VPC, single NAT gateway, SSM-only EC2 with IMDSv2 and encrypted gp3
- [AWS and Azure CLI Cheatsheet](https://github.com/Dstanfield-Creator/cloud-infrastructure/blob/master/reference/cloud-cli-cheatsheet.md) - identity, instances, security groups, storage exposure checks, cost, remote shells
- Case study: [Cloud Services & VM Management](https://github.com/Dstanfield-Creator/cloud-infrastructure/tree/master/case-studies/cloud-vm-management) - Azure VM/storage/network operations, PowerShell automation, ServiceNow/ITIL

### 🤖 AI & Automation

**[ai-automation](https://github.com/Dstanfield-Creator/ai-automation)** - AI agents with real operational reach, held to the controls of a junior admin's service account

- [Paperclip AI Agents](https://github.com/Dstanfield-Creator/ai-automation/tree/main/paperclip-ai-agents) - self-hosted agent platform where agents build and retire VMs through least-privilege Proxmox/PBS tokens, with protected VMs and a hardened host
- n8n workflow automation for lab notifications, log enrichment and scheduled checks runs on the [Docker Services Host](https://github.com/Dstanfield-Creator/lab-ops/tree/main/docs/docker-services-host) and is defined in the [lab-ops Compose services](https://github.com/Dstanfield-Creator/lab-ops/tree/main/compose/services)

### 🔧 General IT & Service Desk

**[general-it](https://github.com/Dstanfield-Creator/general-it)** - IT operations, troubleshooting and administration

- [Troubleshooting Methodology](https://github.com/Dstanfield-Creator/general-it/blob/master/docs/troubleshooting-methodology.md) - define, reproduce, gather facts, split, one hypothesis at a time, verify, document, escalate
- [User Onboarding and Offboarding Checklist](https://github.com/Dstanfield-Creator/general-it/blob/master/administration/user-onboarding-offboarding-checklist.md) - joiner and leaver checklists for AD and Microsoft 365 with the PowerShell behind each step
- [Windows and Linux Command Equivalents](https://github.com/Dstanfield-Creator/general-it/blob/master/reference/windows-linux-command-equivalents.md) - seventy-row task reference plus PowerShell-to-bash idiom notes
- [Change Management for Small Teams](https://github.com/Dstanfield-Creator/general-it/blob/master/docs/change-management-for-small-teams.md) - change record template, change types, armed rollbacks, blameless post-incident notes
- [Documentation vs Live State](https://github.com/Dstanfield-Creator/general-it/blob/master/docs/documentation-vs-live-state.md) - verify with live commands, date and status every doc, retire docs with the hardware

**[Powershell-Scripts](https://github.com/Dstanfield-Creator/Powershell-Scripts)** - Active Directory GUI tooling for a service desk

- [AD Tool](https://github.com/Dstanfield-Creator/Powershell-Scripts/blob/main/AD%20Tool) - tabbed GUI for bulk group changes, account mirroring, Teams numbers, offboarding · [Pull User Details in Active Directory](https://github.com/Dstanfield-Creator/Powershell-Scripts/blob/main/Pull%20User%20Details%20in%20Active%20Directory) - lookup GUI

---

## Write-ups

- [The UFW rule was correct and still locked me out](https://dstanfield-creator.github.io/writeups/ufw-lockout.html) - a conntrack lesson and the dead-man switch that saved the box
- [A backup job that failed silently for a month](https://dstanfield-creator.github.io/writeups/silent-backup-failure.html) - a full root disk, a Proxmox Backup Server rebuild, and alerting on the real failure

---

Last updated October 2026
