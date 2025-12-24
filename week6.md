# Week 6 – Performance Evaluation and Analysis

## Overview
This week focused on evaluating the performance of the Ubuntu Server under different workload conditions. The objective was to observe operating system behaviour, identify performance bottlenecks, and apply optimisations to improve efficiency and responsiveness.

All tests were conducted remotely via SSH, with system metrics monitored in real time.

---

## Methodology

Performance evaluation followed a structured approach:

1. **Baseline Measurement**  
   System metrics were captured while the server was idle to establish a reference point.

2. **Load Testing**  
   CPU, memory, disk, and network workloads were applied individually to isolate resource behaviour.

3. **Bottleneck Analysis**  
   Collected data was analysed to identify resource constraints.

4. **Optimisation**  
   System configuration changes were applied and performance was re-evaluated.

---

## Load Testing

### CPU and Scheduling
CPU utilisation and scheduling behaviour were observed using tools such as `mpstat` and `vmstat` while workloads were applied.

### Memory Usage
Memory behaviour was analysed under load using `vmstat`, focusing on memory pressure and swap activity.

### Disk I/O
Disk performance and I/O wait were monitored using `iostat` during sustained disk activity.

### Network Throughput
Network performance was evaluated using `iperf3` between the workstation and the server. Connectivity was also verified using `ping`.

---

## Bottleneck Analysis

The primary bottlenecks identified were:
- **Memory pressure**, leading to increased swap usage under load
- **Disk I/O latency**, particularly during sustained write operations

These issues reduced responsiveness and increased I/O wait times.

---

## Optimisations

The following optimisations were applied:
- Reduced virtual memory swappiness to prioritise RAM usage
- Disabled unnecessary background services to reduce overhead

These changes aimed to improve performance stability and recovery under load.

---

## Results

After optimisation:
- Swap usage was reduced
- System responsiveness improved
- CPU and memory utilisation stabilised more quickly after load
- Disk I/O wait times showed improvement

---

## Evidence

### Baseline System State
![System information](images/week6/system-information.png)
![System information (detailed)](images/week6/system-information2.png)
![Uptime](images/week6/uptime.png)

### CPU and Memory Monitoring
![mpstat output](images/week6/mpstat.png)
![vmstat output](images/week6/vmstat.png)
![vmstat (extended)](images/week6/vmstat2.png)

### Disk I/O Testing
![iostat output](images/week6/iostat.png)
![Device idle statistics](images/week6/device-idle-stat.png)

### Network Testing
![Ping test](images/week6/ping.png)
![iperf server](images/week6/iperf3-server.png)
![iperf workstation](images/week6/iperf3-workstation.png)

### System Configuration and Services
![System services](images/week6/systemctl.png)
![File configuration](images/week6/file-config.png)
![Workstation VM setup](images/week6/workstation-vmswap.png)
![Workstation config edit](images/week6/nano-workstation.png)
