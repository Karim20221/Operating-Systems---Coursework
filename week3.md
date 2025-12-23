# Week 3 – Application Selection for Performance Testing

## Overview
Applications were selected to generate representative workloads affecting different system resources.

## Application Selection Matrix
- **stress-ng** – CPU and memory stress testing
- **fio** – Disk I/O testing
- **iperf3** – Network throughput testing
- **nginx** – Lightweight server workload
- **sysbench** – Controlled benchmarking

## Installation
All applications were installed remotely via SSH:

```bash
sudo apt update
sudo apt install stress-ng fio iperf3 nginx sysbench -y
