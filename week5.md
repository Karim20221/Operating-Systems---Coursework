### Week 5 – Advanced Security and Monitoring Infrastructure

## Overview

In Week 5 the focus was on strengthening the security of the server and introducing monitoring features that help with ongoing system administration. The idea was to make the system more resilient against attacks while also improving visibility over what is happening on the server.

All work continued to be carried out remotely over SSH, keeping the headless server approach consistent throughout the project.

The main areas in this week were mandatory access control, intrusion prevention, verification of security controls, and the creation of a monitoring script.

# Mandatory Access Control (AppArmor)

AppArmor was enabled to provide mandatory access control at the operating system level. This adds another layer of security by restricting what applications are able to do, even if they are exploited or behave unexpectedly.

The enforcement status and loaded AppArmor profiles were checked to confirm that it was active and protecting system processes as intended.

This helps reduce the potential impact of compromised software and limits the actions that applications are able to perform on the system.

# Intrusion Detection and Prevention (fail2ban)

fail2ban was installed and configured in order to protect the SSH service from repeated failed login attempts and automated brute force attacks.

The service works by monitoring authentication logs and automatically blocking IP addresses that generate suspicious login behaviour. This improves security while still allowing legitimate access to the server.

Service status and configuration were verified to ensure that fail2ban was running correctly and actively monitoring SSH activity.

# Security Baseline Verification

As part of this week, previously configured security settings were re-checked to make sure they were still active and functioning as expected.

This included verifying:

- SSH service status
- Firewall configuration
- fail2ban service state
- General system status

This step helps confirm that earlier security work remains effective and has not been changed or reverted during later configuration tasks.

# Monitoring Script

A monitoring script called monitor-server.sh was created to provide a quick way to check important system information.

The script gathers and displays key metrics such as:

- Hostname and uptime
- CPU load
- Memory usage
- Disk usage
- Currently logged-in users

The script was made executable using chmod and tested to ensure it ran correctly. This makes it easier to get an overview of system health during administration work.

## Evidence

### System & Security Setup
![Install sudo and apt tools](images/week5/install-sudo-apt.png)
![Server status](images/week5/server-status.png)
![UFW configuration](images/week5/ufw-config.png)

### fail2ban Configuration
![Install fail2ban](images/week5/install-fail2ban.png)
![fail2ban information](images/week5/fail2ban-information.png)
![fail2ban active service](images/week5/fail2ban-active-service.png)
![Restart fail2ban](images/week5/restart-fail2ban.png)

### Monitoring Script
![Set script permissions](images/week5/chmod.png)
![Monitor script permissions](images/week5/chmod-monitor.png)
