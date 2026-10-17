# Building a Debian Docker Host on Proxmox VE

**IT Infrastructure | Virtualization | Containerization | Linux Administration**

**Status:** Completed — October 2026

## Overview

Deployed and configured a dedicated Debian 13 virtual machine on Proxmox VE to serve as a centralized Docker host for my homelab.

The goal was to establish a secure, reliable, and scalable foundation for deploying containerized applications and self-hosted services.

## Technologies Used

- **Proxmox VE 9.2** — Virtualization platform
- **Debian 13** — Linux server operating system
- **Docker Engine & Docker Compose** — Containerization
- **SSH** — Remote administration
- **UFW** — Firewall security
- **QEMU Guest Agent** — Virtual machine integration
- **Unattended Upgrades** — Automated system maintenance

## Virtual Machine Specifications

| Component | Configuration |
|---|---|
| VM Name | docker-01 |
| VM ID | 100 |
| Operating System | Debian 13 |
| CPU | 8 vCPUs |
| Memory | 16 GB |
| Storage | 80 GiB |
| Firmware | OVMF (UEFI) |
| Network | VirtIO / vmbr0 |

## Implementation

1. **Virtual Machine Deployment** — Provisioned a dedicated Debian VM on Proxmox VE.
2. **Operating System Configuration** — Installed Debian 13, system updates, and QEMU Guest Agent.
3. **Network & Remote Access** — Configured DHCP reservation and SSH administration.
4. **Docker Installation** — Installed Docker Engine and Docker Compose from the official Docker repository.
5. **Host Organization** — Created dedicated directories for Compose files, persistent application data, and scripts.
6. **Docker Configuration** — Configured local log rotation and automatic service startup.
7. **Security & Maintenance** — Enabled UFW firewall protection and unattended system upgrades.
8. **Backup & Recovery** — Created a Proxmox recovery snapshot before deploying applications.

## Testing & Results

Successfully verified:

- Debian operating system and network connectivity
- SSH remote access
- QEMU Guest Agent functionality
- Docker Engine and Docker Compose
- Successful `hello-world` container execution
- Docker logging configuration
- UFW firewall protection
- Automatic update configuration
- Docker services enabled at startup

**Result:** A fully operational Docker host ready for future containerized applications.

## Full Project Documentation

The complete technical report includes configuration procedures, commands, screenshots, verification results, and implementation details.

**[View Full Project Documentation](https://docs.google.com/document/d/1r8vTCQUO-v1bKWIk8zPReYMo1yHpUMn5I5FvH0RjOVU/edit?usp=sharing)**

## Next Steps

- Deploy Portainer for centralized container management.
- Deploy self-hosted applications using Docker Compose.
- Configure persistent storage and application backups.
- Expand monitoring and security capabilities.

---

*Part of my Cybersecurity & IT Homelab Portfolio.*
