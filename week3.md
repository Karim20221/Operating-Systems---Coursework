# Week 3 – Application Selection for Performance Testing

## Overview

In Week 3 I focused on selecting the applications and tools that would be used to generate different types of workloads on the server. The idea was to choose tools that could stress specific parts of the system such as CPU, memory, disk, and network, so that the behaviour of the operating system could be observed more clearly under load.

All tools were chosen with the goal of keeping the setup realistic to how servers are tested and monitored in practice, while still being simple enough to run and control remotely through SSH.

## Application Selection

Different tools were selected so that each one targeted a particular system resource. This made it easier to understand which component was being stressed at any given time and how the operating system responded.

The main applications selected were:

- **stress-ng** – used for CPU and memory stress testing to simulate heavy processing or workload spikes
- **fio** – used for disk I/O testing to generate read and write activity on the storage device
- **iperf3** – used for network throughput testing between the workstation and server
- **nginx** – used as a lightweight web server to simulate a small real-world service workload
- **sysbench** – used as a simple and controlled benchmarking tool

Each of these tools serves a different purpose and together they provide a broader view of overall system performance instead of focusing on just one area.

## Installation

All applications were installed remotely over SSH to remain consistent with the headless administration approach used throughout the coursework.

The tools were installed using the package manager with the following commands:

```bash
sudo apt update
sudo apt install stress-ng fio iperf3 nginx sysbench -y
