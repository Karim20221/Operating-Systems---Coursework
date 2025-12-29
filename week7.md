### Week 7 – Security Audit and System Evaluation

## Overview

In Week 7 the focus was on reviewing and evaluating the overall security posture of the Ubuntu Server after all of the configuration and security work completed in the previous weeks.

The aim of this week was to verify that the security controls were still in place, check how well the system aligns with best-practice server security, and identify any remaining risks that may need ongoing monitoring rather than immediate changes.

# Lynis Security Audit

A security audit was carried out using Lynis to analyse the server configuration and evaluate the strength of the applied security controls.

Lynis runs a large number of automated checks that cover areas such as authentication settings, network configuration, file permissions, system hardening and exposed services. This makes it useful for highlighting potential weaknesses or configuration issues that may not be obvious during normal use.

The audit results were reviewed and the warnings and suggestions provided by Lynis were treated as guidance for future improvement and maintenance of the system, rather than as critical failures.

# Security Evaluation

From the audit review, it was confirmed that major security controls remained active and correctly configured. These included:

# Hardened SSH configuration

Restricted and controlled network access

Enforced access control and security policies

A minimal set of exposed and running services

This indicates that the system is configured in a secure and intentional way, rather than being left in a default or open state.

Most of the remaining risks identified were not immediate vulnerabilities, but areas that require continued awareness over time.

# Risk Assessment

The main residual risks relate to:

- Possible unknown or future software vulnerabilities
- Human error during future configuration changes
- These risks are mitigated through:
- Regular system updates and patching
- Periodic security audits and reviews
- Monitoring system behaviour and configuration changes

This approach allows the system to remain secure over time, even as software and workloads evolve.

## Evidence

### Lynis Audit Execution and Results
![Lynis security audit](images/week7/lynis-security.png)
![Lynis audit results](images/week7/lynis-results.png)
