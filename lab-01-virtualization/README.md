# Lab 1 — Virtualisation Fundamentals

## Lab Metadata
- **Category:** System Administration
- **Subdomain:** Virtualisation
- **Difficulty:** Beginner
- **Status:** Completed
- **Estimated Time:** 2–3 hours

---

## Objective
The goal of this lab was to gain hands-on experience with virtualisation fundamentals by creating and managing a Linux virtual machine. The lab focuses on understanding how virtual machines are provisioned, isolated, and recovered using snapshots.

This lab establishes a foundation for later System Administration and Cybersecurity labs by providing a safe, repeatable environment for testing and experimentation.

---

## Environment
- **Host OS:** Windows 11
- **Hypervisor:** VirtualBox
- **Guest OS:** Ubuntu Server 22.04 LTS
- **Networking Mode:** NAT
- **Hardware Allocation:**
  - CPU: 2 cores
  - RAM: 4 GB
  - Storage: 30 GB (VDI)

---

## Tasks Performed

1. Installed VirtualBox on the host system  
2. Created a new virtual machine  
3. Installed Ubuntu Server using manual configuration  
4. Configured networking using NAT  
5. Enabled and tested SSH access  
6. Took and restored VM snapshots  
7. Verified system status using basic Linux commands  

---

## Evidence
Screenshots are provided to demonstrate:
- Virtual machine configuration  
- Ubuntu Server installation progress  
- Successful login and system information  
- SSH connectivity confirmation  
- Snapshot creation and restore  

📁 **Screenshots:** `./screenshots/`

---

## Key Concepts Learned
- **Virtual Machines (VMs):** Isolated environments running on shared hardware  
- **Hypervisors:** Software used to create and manage VMs  
- **NAT Networking:** Provides outbound connectivity while maintaining isolation  
- **Snapshots:** Point-in-time VM states for quick recovery  
- **SSH:** Secure remote access to a server  

---

## Security Considerations
- SSH access was enabled only when required  
- Default credentials were avoided  
- Network isolation was maintained using NAT  
- Snapshot usage helps recover from misconfiguration or compromise  

---

## Reflection
This lab helped build my confidence working with virtual machines and Linux servers. Doing a manual installation gave me a better understanding of system configuration compared to automated setups, and managing snapshots highlighted how important backups and recovery are in system administration.

The lab also felt a bit easier because I’ve worked with Hyper-V before during my Certificate in Information Technology. I had prior experience creating both host and local virtual machines, including Windows Server 2022 environments, which made the concepts easier to follow this time around.

Compared to the sandbox labs I used previously—which were often slow and restrictive—running everything locally in VirtualBox was a much smoother experience. Things clicked faster, and the overall process made more sense.

This lab also helped me properly understand snapshots. I can now see how VirtualBox snapshots are essentially the same concept as Hyper-V checkpoints, just implemented on a different platform.

---

## Quick Glossary

**Virtual Machine (VM)** — A software-based computer that runs inside your host system using virtual hardware (CPU/RAM/disk/network). Used to test and learn safely in an isolated environment.

**Hypervisor** — The software layer that creates and runs virtual machines (e.g., VirtualBox). It manages the VM’s virtual hardware and isolates it from the host.

**LVM (Logical Volume Manager)** — A Linux storage system that lets you create flexible “logical” disks on top of physical/virtual disks, making resizing and management easier than fixed partitions.

**NAT (Network Address Translation)** — A networking mode where the VM can access the internet through the host while staying hidden from the local network. Good default for safer lab setups.

**SSH (Secure Shell)** — An encrypted remote access protocol used to securely log into and manage Linux servers from another machine (e.g., from Windows PowerShell/Terminal).


## Next Steps
- Prepare for Lab 2: Linux User & Group Management 
