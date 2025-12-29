# Week 2 – Security Planning and Testing Methodology

## Overview

In Week 2 I focused on planning how the server would be tested and secured before carrying out any major performance or stress testing. The goal was to make sure the system was configured safely while still being able to monitor and evaluate its behaviour under different workloads.

Most of this planning was based around understanding how the server might be used in a real environment and what security risks it could face, especially since all administration is done remotely through SSH.

## Performance Testing Plan

The performance testing was designed to look at how the server behaves under different levels of load, while still keeping security controls enabled in the background.

The main areas I planned to test were:

- CPU performance under stress
- Memory usage and behaviour under pressure
- Disk usage and I/O activity
- Network performance and throughput
- General system responsiveness

All of this was monitored remotely over SSH so the system stayed headless and realistic to a server environment.

## Testing Environment

The testing environment from Week 1 was kept the same to ensure consistency:

- Ubuntu Server (headless, CLI-only)
- Linux kernel
- 8 GB RAM
- 25 GB virtual disk
- Running inside VirtualBox
- Managed fully through SSH

This setup keeps a clear separation between the workstation and server, which also reduces unnecessary risk.

## Network Context

The server runs inside a VirtualBox virtual network and is accessed only by the workstation system.

The network configuration and IP addressing were checked using `ip addr` to make sure the connection was stable and predictable before running any tests.

Keeping the server inside a virtual network also reduces exposure, since it is not directly reachable from the public internet.

## Performance Metrics

The plan was to monitor the following values during testing:

- CPU utilisation
- Memory usage and swap behaviour
- Disk usage and I/O activity
- Network throughput and stability
- Overall system responsiveness

These metrics help build a clearer picture of how the operating system reacts when workloads increase.

## Testing Methodology

To keep the testing structured, I followed a simple step-by-step approach:

1. Record a baseline after boot
2. Apply different workloads
3. Identify bottlenecks or weak areas
4. Apply optimisations and re-test

This makes it easier to compare behaviour before and after changes.

## Security Configuration Checklist

Before running tests, I planned out the main security controls that needed to be in place.

### SSH Hardening
- Key-based authentication instead of passwords
- Disable password login
- Disable root login over SSH
- Restrict SSH access to specific users

### Firewall Configuration
- Enable UFW
- Allow SSH only from the workstation IP
- Deny other inbound traffic

### Mandatory Access Control
- Enable AppArmor
- Check that it is running in enforced mode

### Automatic Security Updates
- Enable unattended security updates to reduce risk

### User Management
- Use a non-root admin account
- Apply least-privilege through sudo

### Network Security
- Keep server isolated within the virtual network
- Review running services to reduce attack surface

## Threat Model

The threat model was kept simple and focused on realistic risks for a small remote server.

### Brute-force SSH attacks
This is reduced by using key-based authentication and firewall restrictions, instead of allowing password logins from anywhere.

### Unauthorised network access
This is mitigated with a default-deny firewall and regular service checks.

### Privilege escalation risks
This is reduced by disabling root login and enforcing access-control policies.
