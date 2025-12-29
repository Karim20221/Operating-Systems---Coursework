# Week 1 – System Planning and Setup

## System Architecture

For this coursework I set up two systems — a headless Linux server and a separate workstation that I used to control it. The server does not have a graphical interface and everything is done through the terminal.

All administration is carried out over SSH from the workstation. I chose this approach because it forces the use of the command line instead of relying on a desktop environment. It also feels closer to how real servers are normally managed in industry, where remote access is standard.

## Distribution Selection

I decided to use Ubuntu Server for the operating system. The main reasons were that it is stable, has long-term support, and there is a lot of documentation and community support available online.

Another reason for choosing Ubuntu Server over a desktop distribution is that it is more minimal and lightweight. Since this machine is intended to function as a server rather than a normal PC, it makes sense to use a stripped-down environment without unnecessary background applications.

## Workstation Configuration

A separate Linux workstation was used to connect to the server remotely. The workstation acts as the client, and the server remains isolated and managed only through SSH.

This setup helps build a proper understanding of the difference between a client system and a server system, rather than running everything on a single machine. It also keeps the environment cleaner and easier to manage.

## Network Configuration

Both systems were run inside VirtualBox using a virtual network so that they could communicate with each other securely. This prevents the server from being exposed directly to the public internet.

Network details were checked using basic command-line tools such as `ip addr` to confirm that the interfaces and IP addresses were configured correctly. This step was important to make sure SSH connectivity worked properly before moving on.

## System Specifications

Before carrying out further tasks, I collected basic system information from the server such as kernel version, memory usage and disk storage.

These details were recorded using simple terminal commands so that I had a clear understanding of the system I was working with at the start of the coursework.

## Evidence

The following screenshots show the commands used to display system and network information:

![IP configuration](images/week1/ip-addr.png)
![Kernel info](images/week1/uname.png)
![Memory usage](images/week1/free.png)
![Disk usage](images/week1/df.png)
