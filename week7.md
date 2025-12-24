# Week 7 – Security Audit and System Evaluation

## Overview
This week focused on evaluating the overall security posture of the Ubuntu Server after implementing security controls in previous weeks. The objective was to verify that the system configuration aligns with best practices and to identify any remaining risks.

---

## Lynis Security Audit

A Lynis security audit was conducted to assess the server’s configuration, security controls, and potential vulnerabilities. Lynis provides automated checks covering system hardening, authentication, network configuration, and service exposure.

The audit results were reviewed to identify warnings and suggestions that could be addressed through further configuration or ongoing maintenance.

---

## Security Evaluation

The audit confirmed that key security controls were in place, including:
- Hardened SSH configuration
- Restricted network access
- Enforced security policies
- Minimal exposed services

Any remaining risks primarily relate to zero-day vulnerabilities and future misconfiguration rather than immediate weaknesses.

---

## Risk Assessment

Residual risks include:
- Unknown vulnerabilities in system packages
- Human error during future configuration changes

These risks are mitigated through:
- Regular system updates
- Periodic security audits
- Ongoing monitoring and review of system settings

---

## Evidence

### Lynis Audit Execution and Results
![Lynis security audit](images/week7/lynis-security.png)
![Lynis audit results](images/week7/lynis-results.png)
