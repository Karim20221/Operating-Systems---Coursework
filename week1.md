# Week 1 – System Planning and Setup

## System Architecture
This coursework uses a dual-system architecture consisting of a headless Linux server and a separate workstation. The server runs without a graphical interface and is administered entirely through SSH from the workstation.

This approach enforces command-line proficiency and mirrors real-world server administration practices.

## Distribution Selection
Ubuntu Server was selected due to its stability, long-term support, and extensive documentation. Compared to desktop distributions, Ubuntu Server provides a minimal environment suitable for secure and efficient server deployment.

## Workstation Configuration
A Linux-based workstation was used to administer the server via SSH. This allows secure remote access while maintaining separation between client and server environments.

## Network Configuration
The systems communicate using a VirtualBox virtual network. IP addressing and network interfaces were verified using CLI tools to ensure reliable and secure connectivity.

## System Specifications
System information was documented using standard command-line tools.

## Evidence
![IP configuration](images/week1/ip-addr.png)
![Kernel info](images/week1/uname.png)
![Memory usage](images/week1/free.png)
![Disk usage](images/week1/df.png)
