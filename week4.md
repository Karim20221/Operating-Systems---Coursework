# Week 4 – Initial System Configuration & Security Implementation

## SSH Key-Based Authentication
SSH keys were generated on the workstation and copied to the server. Password authentication and root login were disabled in `sshd_config`.

## Firewall Configuration
UFW was enabled with SSH access allowed only from the workstation IP. All other inbound traffic was denied.

## User Management
A non-root administrative user was created and granted sudo privileges.

## Remote Administration
All configuration tasks were performed remotely via SSH.

## Evidence
![SSH login](images/week4/ssh-login.png)
![sshd config](images/week4/sshd-config.png)
![UFW rules](images/week4/ufw-status.png)
