# Week 2 – Security Planning and Testing Methodology

## 1. Performance Testing Plan

The objective of this performance testing plan was to evaluate the performance and behaviour of a Linux server operating system configured in Week 1. The system runs Ubuntu Server and is administered remotely via SSH from a Linux workstation.

The testing in this phase mainly focused on CPU usage, memory usage, disk activity, and network performance under different workloads, while ensuring that security controls remained active and enforced throughout testing.

---

## Testing Environment

The system configuration used for testing was based on the setup completed in Week 1:

- Operating System: Ubuntu Server (headless)
- Kernel: Linux
- Memory: 8 GB RAM
- Storage: 25 GB virtual disk
- Virtualisation Platform: VirtualBox
- Administration Method: SSH (command-line only)

This environment reflects a realistic server setup and enforces professional remote administration practices.

---

## Network Context

The server operates within a VirtualBox virtual network and uses two network interfaces. This allows the workstation to connect remotely to the Ubuntu Server while keeping the environment isolated.

The `ip addr` command was used to verify network interfaces and IP addresses, ensuring that the system could be accessed and monitored securely via SSH.

---

## Performance Metrics

The following metrics were monitored during performance evaluation:

- CPU utilisation
- Memory usage
- Disk usage and I/O activity
- Network throughput and latency
- System responsiveness under heavy load

These metrics provide a clear view of how the operating system behaves under different workload conditions.

---

## Testing Methodology

Performance testing was conducted using a structured approach:

- **Baseline Measurement**  
  Capturing default system metrics immediately after boot to establish a reference point.

- **Workload Testing**  
  Running multiple applications that stress different system resources, including CPU, memory, disk, and network.

- **Bottleneck Identification**  
  Analysing collected data to identify resource constraints or inefficiencies.

- **Optimisation Testing**  
  Applying configuration changes and measuring performance improvements using comparative results.

---

## 2. Security Configuration Checklist

The following checklist defines the security baseline that will be implemented on the Ubuntu Server configured in Week 1.

### SSH Hardening
- Enforce SSH-only remote administration
- Disable password-based SSH authentication
- Enable SSH key-based authentication
- Restrict SSH access to authorised users
- Disable direct root login via SSH

### Firewall Configuration
- Enable the firewall using the `ufw` command
- Allow SSH access only from the authorised workstation
- Deny all other inbound traffic by default

### Mandatory Access Control (MAC)
- Enable AppArmor
- Verify that enforcement mode is active
- Review applied security profiles

### Automatic Security Updates
- Enable unattended security updates
- Verify update scheduling and configuration

### User and Privilege Management
- Create a non-root administrative user
- Apply least-privilege principles using `sudo`
- Audit user permissions regularly

### Network Security
- Operate the server within an isolated VirtualBox network
- Verify that only required network services are active
- Perform regular service and port audits

---

## 3. Threat Model

### Threat 1 – Brute-Force SSH Attacks

Exposed SSH services may be targeted by attackers attempting repeated login attempts.

**Mitigation:**
- Disable password-based authentication
- Enforce SSH key-based authentication
- Restrict SSH access to a single authorised workstation
- Implement intrusion prevention mechanisms such as fail2ban

---

### Threat 2 – Unauthorised Network Access

Open ports or unnecessary services could expose the server to network-based attacks.

**Mitigation:**
- Apply a default-deny firewall policy
- Allow only essential services (SSH)
- Regularly audit open ports and active services

---

### Threat 3 – Privilege Escalation

Improper privilege separation could allow users or attackers to gain elevated access.

**Mitigation:**
- Disable root SSH login
- Enforce controlled `sudo` access
- Apply mandatory access control mechanisms such as AppArmor
- Review user permissions regularly

---

## Reflection

Week 2 focused on planning security controls and performance evaluation strategies before implementation. By defining a clear security baseline and structured testing methodology, later configuration decisions can be measured objectively.

This approach ensures that performance results and security trade-offs are intentional, measurable, and aligned with professional system administration practices.
