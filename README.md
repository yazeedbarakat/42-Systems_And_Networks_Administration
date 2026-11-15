# 42 — Systems and Networks Administration

*Projects completed as part of the 42 curriculum by **ybarakat** at 42 Irbid.*

## About this module

This module puts you in the role of a system administrator who builds, secures and manages server infrastructure from scratch. It covers virtualization, networking fundamentals and containerization, ending with deploying and orchestrating a multi-service application.

## Projects

| Project | What it covers |
|---|---|
| [Born2beRoot](./Born2beRoot) · [subject](https://code.42.tech/modules/7ccc7056-93fc-4174-afac-e881d9783624/projects/558bb401-93ba-4c66-9889-60ed63719047) | A headless Debian server in VirtualBox with encrypted LVM partitions, hardened SSH, UFW firewall, AppArmor, strict password and `sudo` policies, and a monitoring script scheduled with `cron`. The repo holds the VM's `signature.txt` and setup notes. |
| [Net_Practice](./Net_Practice) · [subject](https://code.42.tech/modules/7ccc7056-93fc-4174-afac-e881d9783624/projects/55f55ca1-02db-422c-9e6b-363be234c578) | 10 levels of broken network diagrams, fixed by choosing correct IP addresses, subnet masks and routing tables. Solutions are exported as `level1.json` … `level10.json`. |
| [Inception](https://github.com/yazeedbarakat/Inception) · [subject](https://code.42.tech/modules/7ccc7056-93fc-4174-afac-e881d9783624/projects/fb33c01f-ba3a-4ad7-92af-e35686e8cb20) | A small infrastructure of Docker containers orchestrated with Docker Compose inside a VM: NGINX (TLS only) → WordPress + PHP-FPM → MariaDB. Each service runs in its own container built from a custom Dockerfile, connected through a dedicated Docker network, with persistent named volumes and credentials kept out of the images. *(separate repository)* |

## Key concepts

- Virtualization and disk partitioning (LVM, LUKS encryption)
- Users, groups and permissions
- Service hardening (SSH on a non-default port, root login disabled)
- Firewalls and mandatory access control (UFW, AppArmor)
- Password policies (PAM) and `sudo` logging
- Shell scripting and task scheduling (`cron`)
- IPv4 addressing, CIDR and subnet masks
- Routing tables, default gateways, and how switches and routers forward traffic
- Public vs. private address ranges
- Containers vs. VMs, writing Dockerfiles, and running one foreground process per container (PID 1)
- Docker Compose, Docker networks, volumes, and secrets management

## Usage

- **Born2beRoot** — compare `signature.txt` with the SHA1 of your `.vdi` to confirm the VM is untouched since submission. See [Born2beRoot/README.md](./Born2beRoot/README.md) for the full setup.
- **Net_Practice** — load the training interface, then import any `levelN.json` to view the solution. See [Net_Practice/README.md](./Net_Practice/README.md).
- **Inception** — see the [Inception repository](https://github.com/yazeedbarakat/Inception) for build and run instructions.
