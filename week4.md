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

### SSH Key-Based Authentication
![SSH key generation](images/week4/ssh-key-gen.png)
![SSH key copied to server](images/week4/ssh-copyid.png)
![Password authentication disabled](images/week4/passauth-disabled.png)
![SSH authentication config](images/week4/auth-status-file.png)

### SSH Access Verification
![SSH login](images/week4/ssh-login.png)
![SSH login after configuration](images/week4/ssh-login-after-config.png)
![SSH service status](images/week4/status-ssh.png)

### User and Privilege Management
![Create admin user](images/week4/add-adminuser.png)
![Add user via SSH](images/week4/ssh-adduser.png)
![Grant sudo privileges](images/week4/usermod.png)
![Admin user status](images/week4/adminuser-status_server.png)
![Admin user status (server)](images/week4/adminuser-status-server2.png)

### Firewall Configuration
![UFW configuration](images/week4/ufw-config.png)
