# Week 5 – Advanced Security and Monitoring Infrastructure

## Mandatory Access Control
AppArmor was enabled and enforcement status verified.

## Intrusion Detection
fail2ban was configured to protect SSH from brute-force attempts.

## Security Baseline Script
A script (`security-baseline.sh`) was created to verify SSH, firewall, MAC, and update configurations.

## Monitoring Script
A workstation-based script (`monitor-server.sh`) connects via SSH and collects system metrics.

## Evidence
![AppArmor status](images/week5/aa-status.png)
![fail2ban status](images/week5/fail2ban.png)
![Monitoring script output](images/week5/monitor-output.png)
