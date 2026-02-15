# Ansible Automation Project – Docker & NGINX

## Overview
This project demonstrates real-world infrastructure automation using Ansible.
It automates the installation and configuration of Docker and NGINX on Linux systems
using role-based Ansible architecture.

The project follows production-style best practices such as:
- Role separation
- Inventory-based targeting
- Variable management
- Jinja2 templating
- Handler-driven service restarts
- Idempotent execution

This is a practical DevOps automation project, not a theoretical or tutorial-only example.

---

## Tools & Technologies Used

Ansible
Docker
NGINX
Ubuntu Linux
YAML

## Project Structure

.
├── LICENSE
├── README.md
├── ansible.cfg
├── site.yml
├── inventory
│   └── hosts
├── group_vars
│   └── web.yml
├── roles
│   ├── docker
│   │   └── tasks
│   │       └── main.yml
│   └── nginx
│       ├── tasks
│       │   └── main.yml
│       ├── handlers
│       │   └── main.yml
│       └── templates
│           └── nginx.conf.j2
├── screenshots
│   ├── ansible-automation-architecture.drawio
│   └── ansible-automation-architecture.png

## Prerequisites
- Linux system (Ubuntu recommended)
- Ansible installed
- Sudo access
- Internet connectivity


## Inventory Configuration
The project uses Ansible inventory for host targeting.

[web]
localhost ansible_connection=local


---

## How to Run the Project

1. Clone the repository
git clone https://github.com/rahulrana16112005-design/ansible-automation-project.git
cd ansible-automation-project


2. Execute the Ansible playbook
ansible-playbook site.yml --ask-become-pass


---

## Architecture Diagram
screenshots/ansible-automation-architecture.png


### Automation Flow Explanation
- Developer runs the Ansible playbook
- Ansible control node reads inventory and variables
- Docker role installs and configures Docker
- NGINX role installs NGINX
- NGINX configuration is applied using Jinja2 templates
- Handlers restart NGINX only when configuration changes
- Services reach the desired state idempotently

---

## Verification Steps

### Verify Docker Installation
docker --version
docker info


### Verify NGINX Service
systemctl status nginx


### Application Access
http://localhost


---

## Idempotency Validation
Run the playbook multiple times:
ansible-playbook site.yml
ansible-playbook site.yml


Expected result:
- First run applies changes
- Subsequent runs show no changes

This confirms idempotent infrastructure automation.

---

## What This Project Demonstrates
- Infrastructure automation using Ansible
- Role-based configuration management
- Separation of concerns using Ansible roles
- Template-driven configuration using Jinja2
- Handler-based service restarts
- Idempotent playbook execution
- Real-world DevOps automation practices

---

## Interview Explanation
This project automates Docker and NGINX setup using Ansible roles.
It uses inventory-based host targeting, Jinja2 templates for configuration management,
handlers for controlled service restarts, and ensures idempotent execution.
The structure reflects production-style DevOps automation rather than ad-hoc scripting.

---

## Author
Rahul Rana 
Aspiring DevOps / Cloud Engineer

---

## License
This project is licensed under the MIT License.
