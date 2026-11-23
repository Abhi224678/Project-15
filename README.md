# Project 15: Automate Server Configuration with Ansible

## Objective

To automate remote server configuration using Ansible and install a web server through an Ansible playbook.

## Tools Used

- Linux VM (Ubuntu 24.04)
- Ansible Core 2.16.3
- SSH
- Nginx
- YAML

## Server Details

| Machine | Role | IP Address |
|---|---|---|
| Linux VM | Ansible Controller | AZLTT0222435e27 |
| SRE Foundation VM | Target Server | 10.5.1.237 |

## Implementation Steps

1. Installed Ansible Core on the Linux controller VM.
2. Created a separate project directory.
3. Configured the Ansible inventory file (`inventory.ini`) with the target server IP.
4. Established SSH connectivity between the controller and target VM.
5. Installed `sshpass` for password-based SSH authentication.
6. Tested Ansible connectivity using the ping module.
7. Created an Ansible playbook named `install-nginx.yml`.
8. Configured the playbook to install Nginx on the target server.
9. Used Ansible to start and enable the Nginx service.
10. Verified that the Nginx service was running successfully.

## Ansible Playbook

The playbook performs the following tasks:

- Gathers target server information.
- Installs Nginx using the APT package manager.
- Starts the Nginx service.
- Enables Nginx to start automatically during system boot.

## Commands Used

### Check Ansible Version

```bash
ansible --version
