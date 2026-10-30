# Cybersecurity Virtual Lab Environment

**Building a controlled virtual environment for cybersecurity learning, network analysis, and authorized penetration testing.**

![Kali Linux](https://img.shields.io/badge/OS-Kali%20Linux-557C94?logo=kalilinux&logoColor=white)
![VirtualBox](https://img.shields.io/badge/Virtualization-VirtualBox-183A61?logo=virtualbox&logoColor=white)
![Wireshark](https://img.shields.io/badge/Network%20Analysis-Wireshark-1679A7?logo=wireshark&logoColor=white)
![Nmap](https://img.shields.io/badge/Scanning-Nmap-4682B4)
![Platform](https://img.shields.io/badge/Host-Windows%2011-blue)

---

## Project Overview

This project focuses on setting up a virtual cybersecurity laboratory using Oracle VirtualBox and Kali Linux.

The objective is to establish a controlled environment for learning cybersecurity concepts, understanding network communication, analyzing network traffic, and practising authorized security testing.

The lab uses VirtualBox NAT Network configuration to provide virtual network connectivity.

## Lab Environment

| Component | Configuration |
|---|---|
| Host OS | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Guest OS | Kali GNU/Linux Rolling |
| Kali Version | 2026.3 |
| RAM | 2 GB |
| Processors | 2 |
| Network Mode | NAT Network |
| Network Interface | eth0 |
| IP Address | 10.0.0.2/24 |
| Default Gateway | 10.0.0.1 |

## Tools and Technologies

| Tool | Purpose |
|---|---|
| VirtualBox | Virtual machine management |
| Kali Linux | Cybersecurity testing environment |
| Wireshark | Network packet capture and analysis |
| Nmap | Network discovery and authorized security assessment |

## Lab Configuration

### 1. Virtual Machine Setup

Kali Linux was installed as a guest operating system inside Oracle VirtualBox running on Windows 11.

![VirtualBox Manager](screenshots/01-virtualbox-manager.png)

### 2. System Configuration

The virtual machine was configured with:

- Base Memory: 2048 MB
- Processors: 2
- Video Memory: 128 MB
- Graphics Controller: VMSVGA

![Virtual Machine Settings](screenshots/02-virtual-machine-system-settings.png)

### 3. Network Configuration

The virtual machine uses a NAT Network adapter named `NatNetwork`.

- Adapter: Intel PRO/1000 MT Desktop
- Network Mode: NAT Network
- Interface: eth0
- IP Address: 10.0.0.2
- Gateway: 10.0.0.1

![Network Configuration](screenshots/03-virtual-network-settings.png)

## Network Verification

The following commands were executed to verify the lab configuration.

**IP configuration**

```bash
ip addr
```

**Routing information**

```bash
ip route
```

**Internet connectivity**

```bash
ping -c 4 8.8.8.8
```

Result:
- Packets transmitted: 4
- Packets received: 4
- Packet loss: 0%
- Average latency: 7.066 ms

**DNS resolution**

```bash
nslookup google.com
```

Result: Successful DNS resolution through 10.0.0.1.

## Network Traffic Analysis

Wireshark is included in the lab for capturing and analyzing network traffic.

The analysis focuses on understanding network protocols, packet communication, and traffic behaviour.

A packet-capture demonstration will be added as practical evidence.

## Project Structure

```text
Cybersecurity-Virtual-Lab/
│
├── README.md
│
├── screenshots/
│   ├── 01-virtualbox-manager.png
│   ├── 02-virtual-machine-system-settings.png
│   └── 03-virtual-network-settings.png
│
└── documentation/
    └── lab-configuration.md
```

## Learning Outcomes

- Virtual machine creation and configuration.
- Kali Linux environment setup.
- Virtual network configuration using NAT Network.
- IP addressing and routing fundamentals.
- Network connectivity and DNS troubleshooting.
- Practical exposure to network traffic analysis.
- Familiarity with cybersecurity assessment tools.

## Future Improvements

- Perform authorized Nmap network discovery exercises.
- Document Wireshark packet analysis.
- Introduce additional virtual machines for controlled testing.
- Perform basic vulnerability assessment within the lab.
- Document practical security testing results.

## Disclaimer

This project is intended for educational purposes and authorized security testing only. Testing must be performed exclusively on systems owned by the user or for which explicit permission has been obtained.

---

**Author:** Akash P

**Domain:** Cybersecurity
