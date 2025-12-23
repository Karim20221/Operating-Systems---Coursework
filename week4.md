# Week 4 – Initial System Configuration & Security Implementation

## Overview

This week focused on deploying the Ubuntu Server system configured in Week 1 and implementing foundational security controls. All administrative tasks were carried out remotely via SSH from a separate Linux workstation, reinforcing professional command-line system administration practices.

The aim of this phase was to establish secure remote access, restrict network exposure, and enforce controlled user privilege management on the server.

---

## 1. SSH Configuration with Key-Based Authentication

### Objective
The objective of this step was to secure remote access to the server by replacing password-based authentication with SSH key-based authentication.

### Implementation
An SSH key pair was generated on the workstation system using:

```bash
ssh-keygen -t ed25519 -C "admin@workstation"
