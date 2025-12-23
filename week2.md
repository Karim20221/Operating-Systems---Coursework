# Week 2 – Security Planning and Testing Methodology

## Performance Testing Plan
The objective was to evaluate the performance and behaviour of the Ubuntu Server system configured in Week 1 while maintaining active security controls.

Testing focused on CPU, memory, disk, and network performance under varying workloads using remote monitoring via SSH.

## Testing Environment
- Ubuntu Server (headless)
- Linux kernel
- 8 GB RAM
- 25 GB virtual disk
- VirtualBox virtualisation
- SSH-only administration

## Network Context
The server operates within a VirtualBox virtual network and is accessed remotely by the workstation. Network configuration and IP addressing were verified using `ip addr`.

## Performance Metrics
- CPU utilisation
- Memory usage
- Disk usage and I/O
- Network throughput
- System responsiveness

## Testing Methodology
- Baseline measurement after boot
- Workload testing
- Bottleneck identification
- Optimisation testing

## Security Configuration Checklist
### SSH Hardening
- Disable password authentication
- Enable key-based authentication
- Disable root login
- Restrict SSH users

### Firewall Configuration
- Enable UFW
- Allow SSH from workstation only
- Deny all other inbound traffic

### Mandatory Access Control
- Enable AppArmor
- Verify enforcement mode

### Automatic Updates
- Enable unattended security updates

### User Management
- Non-root admin user
- Least privilege via sudo

### Network Security
- Isolated VirtualBox network
- Regular service audits

## Threat Model
### Brute-force SSH attacks
Mitigated by key-based authentication, firewall restrictions, and intrusion prevention.

### Unauthorised network access
Mitigated through firewall rules and service auditing.

### Privilege escalation
Mitigated by disabling root login and enforcing MAC policies.
