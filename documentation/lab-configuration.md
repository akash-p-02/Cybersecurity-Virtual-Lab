# Lab Configuration

## 1. System Requirements

The cybersecurity lab was configured using the following environment:

| Component | Details |
|---|---|
| Host Operating System | Windows 11 |
| Virtualization Platform | Oracle VirtualBox |
| Guest Operating System | Kali GNU/Linux Rolling |
| Kali Version | 2026.3 |
| Virtual Machine Name | kali-linux-2026.3-virtualbox-amd64 |
| Allocated RAM | 2048 MB |
| Processor Cores | 2 |
| Video Memory | 128 MB |

## 2. Virtual Network Configuration

The Kali Linux virtual machine uses a NAT Network adapter.

| Parameter | Configuration |
|---|---|
| Adapter | Adapter 1 |
| Network Mode | NAT Network |
| Network Name | NatNetwork |
| Adapter Type | Intel PRO/1000 MT Desktop |
| Network Interface | eth0 |
| IPv4 Address | 10.0.0.2 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 10.0.0.1 |
| DNS Server | 10.0.0.1 |

## 3. IP Configuration

The following command was used to inspect the network interfaces:

```bash
ip addr
```

The `eth0` interface was active and configured with IPv4 address `10.0.0.2/24`.

## 4. Routing Configuration

Command:

```bash
ip route
```

Observed routing information:

```text
default via 10.0.0.1 dev eth0
10.0.0.0/24 dev eth0
```

## 5. Network Connectivity Test

Command:

```bash
ping -c 4 8.8.8.8
```

Results:

- Packets transmitted: 4
- Packets received: 4
- Packet loss: 0%
- Average latency: 7.066 ms

The test confirmed successful connectivity to the external IP address.

## 6. DNS Resolution Test

Command:

```bash
nslookup google.com
```

DNS server: `10.0.0.1`

Observed IPv4 response: `142.250.70.46`

Result: DNS resolution successful.

## 7. Security Tools

### Wireshark

Used for capturing and analyzing network packets to understand network communication and protocols.

### Nmap

Included as a network discovery and security assessment tool for authorized lab exercises.

Note: Detailed Nmap testing results will be documented after practical testing.

## 8. Configuration Summary

The Kali Linux virtual machine was successfully configured using VirtualBox NAT Network mode. IP configuration, routing, external connectivity, and DNS resolution were verified.

The environment is ready for further educational network analysis and authorized security testing.

## 9. Security Considerations

NAT Network provides a private virtual network with outbound connectivity. It does not provide complete isolation from external networks.

Security testing should be restricted to systems owned by the user or systems for which explicit authorization has been obtained.