# Week 6 – Performance Evaluation and Analysis

## Methodology
Baseline performance was measured before applying workloads.

## Load Testing
- CPU and memory stress testing
- Disk I/O testing
- Network throughput testing

## Bottleneck Analysis
Memory pressure and disk I/O latency were identified as primary constraints.

## Optimisations
- Reduced VM swappiness
- Disabled unnecessary background services

## Results
Post-optimisation testing showed reduced swap usage and improved responsiveness.

## Evidence
![CPU stress](images/week6/cpu.png)
![Memory stress](images/week6/memory.png)
![Disk I/O](images/week6/disk.png)
![Network test](images/week6/iperf.png)
