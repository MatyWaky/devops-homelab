# DevOps Homelab

A practical DevOps and infrastructure automation project built on a self-hosted Proxmox VE environment.

The goal of this repository is to design, deploy, automate, and maintain a realistic multi-server infrastructure while developing practical skills in Linux system administration and DevOps engineering.

## Project Goals

- Develop practical Linux system administration skills.
- Automate infrastructure configuration using Ansible.
- Learn containerization and application deployment with Docker.
- Implement Infrastructure as Code using Terraform.
- Build CI/CD pipelines with GitHub Actions.
- Deploy monitoring and observability solutions.
- Document infrastructure, configuration, and operational procedures.

## Infrastructure

The environment runs on Proxmox VE and consists of dedicated virtual machines.

| VM | Operating System | Role | Status |
|---|---|---|---|
| OPS01 | Ubuntu Server 26.04 | Ansible Control Node | Operational |
| APP01 | Ubuntu Server 26.04 | Application Server | Operational |
| DB01 | Rocky Linux 10 | Database Server | Planned |
| MON01 | Debian 13 | Monitoring Server | Planned |

## Technology Stack

| Technology | Purpose | Status |
|---|---|---|
| Proxmox VE | Virtualization platform | In use |
| Linux | Server operating systems | In use |
| Git / GitHub | Version control and collaboration workflow | In use |
| Ansible | Configuration management and automation | In use |
| Docker | Containerization | Planned |
| Terraform | Infrastructure as Code | Planned |
| GitHub Actions | CI/CD automation | Planned |
| Prometheus | Metrics collection | Planned |
| Grafana | Monitoring and visualization | Planned |

## Ansible

Ansible runs from OPS01 and manages remote Linux servers over SSH.

Current implementation includes:

- Dedicated `ansible` automation account on managed hosts.
- SSH key-based authentication.
- Privilege escalation through sudo.
- INI-based inventory with parent groups.
- Centralized connection variables using `group_vars`.

## Repository Structure

```text
.
├── ansible/
│   ├── inventory/
│   │   ├── hosts.ini
│   │   └── group_vars/
│   │   	└── all.yml
│   └── ansible.cfg
├── .gitignore
└── README.md
```

## Development Workflow

The project follows a GitHub Flow-based workflow:

1. Create a feature or fix branch from `main`.
2. Implement changes on the local development workstation.
3. Commit and push changes to GitHub.
4. Test changes in the homelab environment.
5. Review and merge through a Pull Request.

The `main` branch represents the approved project state.

## Project Status

This project is actively developed. Infrastructure components and technologies are introduced incrementally, with an emphasis on practical implementation, reproducibility, and documentation.