# Ansible Automation Project - Docker and NGINX

## Overview
This project automates the installation and configuration of Docker and NGINX
on Linux systems using Ansible. It demonstrates real DevOps automation using
roles, inventory, variables, templates, and handlers.

## Tools and Technologies
- Ansible
- Docker
- NGINX
- Ubuntu Linux
- YAML

## Project Structure
.

├── LICENSE
├── README.md
├── ansible.cfg
├── group_vars
│   └── web.yml
├── inventory
│   └── hosts
├── roles
│   ├── docker
│   │   └── tasks
│   │       └── main.yml
│   └── nginx
│       ├── handlers
│       │   └── main.yml
│       ├── tasks
│       │   └── main.yml
│       └── templates
│           └── nginx.conf.j2
├── screenshots
│   ├── ansible-automation-architecture.drawio
│   └── ansible-automation-architecture.png
└── site.yml


## Prerequisites
- Linux system (Ubuntu recommended)
- Ansible installed
- Sudo access
- Internet connectivity

## How to Run the Project

1. Navigate to the project directory
   cd ansible-automation-project

2. Run the Ansible playbook
   ansible-playbook site.yml --ask-become-pass

##  Architecture Diagram

![Ansible Role-Based Automation Architecture]
(ansible-automation-architecture.png)

This diagram shows the complete automation flow:
- Developer runs the Ansible playbook
- Ansible Control Node uses inventory to target hosts
- Docker and NGINX are configured using role-based automation

## Verification

Check Docker:
docker --version

Check NGINX:
systemctl status nginx

Open in browser:
http://localhost

## What This Project Demonstrates
- Infrastructure automation using Ansible
- Role-based configuration management
- Idempotent playbook execution
- Template-driven NGINX configuration
- Handler-based service restart
- Real-world DevOps troubleshooting

## Interview Explanation
This project automates Docker and NGINX setup using Ansible roles. It runs on
real Linux systems and demonstrates practical DevOps automation instead of
theoretical examples.

## Author
Rahul Rana 
Aspiring DevOps / Cloud Engineer
