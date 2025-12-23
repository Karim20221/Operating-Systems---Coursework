# Week 3 – Application Selection for Performance Testing

## Overview

The objective of this phase was to select applications that generate different types of workloads on the Ubuntu Server system configured in Weeks 1 and 2. These applications are used to evaluate how the operating system manages CPU, memory, disk I/O, and network resources under varying conditions.

The selected applications represent realistic server workloads that are commonly encountered in professional environments and are suitable for testing on a headless Linux server.

---

## Application Selection Matrix

The following applications were selected to cover a range of workload types:

- **stress-ng**  
  Used for CPU and memory intensive testing. This tool generates controlled workloads to analyse CPU scheduling behaviour, CPU utilisation, and memory management.

- **fio**  
  Used for disk I/O intensive testing. It simulates read and write operations to evaluate filesystem and disk performance under load.

- **iperf3**  
  Used for network intensive testing. It measures network throughput and latency between the workstation and the server.

- **nginx**  
  A lightweight web server used to simulate a real-world server and network service workload.

- **sysbench**  
  A benchmarking tool used for controlled performance comparisons across CPU, memory, and disk operations.

This selection ensures coverage of multiple workload types while remaining manageable within a headless server environment.

---

## Installation Documentation

All applications were installed remotely on the server via SSH using the system package manager. This maintains consistency with the SSH-only administration requirement.

Example installation commands:

```bash
sudo apt update
sudo apt install stress-ng fio iperf3 nginx sysbench -y
