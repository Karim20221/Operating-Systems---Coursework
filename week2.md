Week 2 - Security Planning and Testing Methodology

1. Performance testing plan

The objective of performance testing plan was to check the performance and behaviour of a linux server opeating system that we previously configured in week 1. This system runs a ubuntu server and was remotely adminitered via SSH from a linux workstation.
The testing in this part mainly focussed on cpu usage, memory usage, disk and network activity under different workloads while making sure security controls are active and in place.

Testing Enviroment

The configureation was based on week 1

- Ubuntu Server
- Linux
- Memoory was 8 gb
- Storage 25 gb virtual disk
- Virtualbox to run vms
- Admin method was SSH

Network Context

The server was operated by virtualbox was using a virtual network with two assigned ip addresses so we could have the workstation remotely connect with the ubuntu server and vice versa, ip addr was used to ensure the system can be securely accessed and monitored remotely.

Performance metrics

The following were activity monitored during the performance evaulation

- CPU utilistation
- Memory usage
- Disk usage and I/O activity
- Network
- System responsiveness under heavy load

Testing Methodolgy

Baseline measurement, used to capture the default system metrics immedaitely after booting the workstation.
Workload testing, running multiple applications that each affect a different part of the system such as CPU, memory, disk and network.
Bottleneck identification, identifying whether there was enough data to identify resource constraints.
Optimisation testing, applying configuration changes and meassuring performance improvements

2. Security Configuration Checklist

The following checklist define baseline that will be implmented on the ubunti server that we configured in week 1

SSH Hardening
- Used to enforce ssh only remote admin
- Used to disable password based authentication
- Used to enable key based authentication
- Used to restrict ssh access to auth users
- Used to disable root login via ssh

Firewall configuation
- Enable firewall using ufw command
- Allow ssh access from the workstation only
- Deny all other traffic thats inbound by default

MAC or Mandotory Access Control
- Enable apparmour
- verify enforcement mode is activated
- security profiles

Automatic Security Updates
- Enable unattended security updates
- Vreify update schedule

User and Privilege Management
- Create a non root admin user
- Apply low priv settings using sudo
- Audit user permissions

Network Security
- Operate the server using an isolated virtualbox network
- verify only required network servers are activated
- perform regular service and port audits

3. Threat Model

Threat 1 - Brute Force SSH Attacks

Exposed SSH services may be targetted by attacks attempting multiple login attempts

To fix this,

- Disable Password authentication
- Enforce ssh key based authentication
- Restrict ssh access to one workstation only
- 
