\# Network Traffic Analysis & Security Investigation Lab

\#\# Overview

This project is a hands-on network traffic analysis lab built using  
Kali Linux and Ubuntu Server. The goal was to capture, analyze, and  
investigate network traffic using tcpdump and Wireshark.

The lab focused on identifying communicating hosts, analyzing TCP  
connections, examining encrypted SSH traffic, and investigating  
network reconnaissance through an Nmap port scan.

\#\# Objectives

\- Capture network traffic using tcpdump  
\- Analyze packets using Wireshark  
\- Identify source and destination IP addresses  
\- Analyze TCP connections and the three-way handshake  
\- Understand how SSH traffic appears in a packet capture  
\- Identify TCP port scanning activity  
\- Determine how open and closed ports can be identified from TCP responses  
\- Document findings using an analyst-style investigation process

\#\# Lab Environment

| Component | Purpose |  
|---|---|  
| Kali Linux | Security testing and analysis workstation |  
| Ubuntu Server 24.04.4 LTS | Target/server |  
| tcpdump | Command-line packet capture |  
| Wireshark | Packet analysis |  
| Nmap | Network reconnaissance and port scanning |

\#\# Network

| Host | IP Address |  
|---|---|  
| Kali Linux | 192.168.1.81 |  
| Ubuntu Server | 192.168.1.245 |

\> These IP addresses were assigned to the lab environment and are not  
\> intended to represent production systems.

\#\# Investigations

\#\#\# 1\. SSH Traffic Analysis

An SSH connection was established from Kali Linux to the Ubuntu server.

The investigation identified:

\- Source IP  
\- Destination IP  
\- Source port  
\- Destination port 22  
\- TCP three-way handshake  
\- Encrypted SSH application traffic

The packet capture demonstrated that network metadata such as IP  
addresses, ports, and packet information remained visible while the  
actual SSH session contents were encrypted.

\#\#\# 2\. Nmap Port Scan Analysis

An Nmap scan was performed against the Ubuntu server while tcpdump  
captured the resulting network traffic.

The capture showed a single source host sending TCP SYN requests to  
multiple destination ports on the Ubuntu server.

Examples included:

\- TCP 22 — Open  
\- TCP 80 — Closed  
\- TCP 8888 — Closed

Packet-level analysis was used to determine how the server responded  
to the connection attempts.

For TCP port 22, the capture showed:

SYN → SYN/ACK → RST

This behavior is consistent with an Nmap TCP SYN/half-open scan and  
indicates that a service was listening on port 22\.

\#\# Tools Used

\- Kali Linux  
\- Ubuntu Server  
\- Wireshark  
\- tcpdump  
\- Nmap  
\- VMware / VirtualBox  
\- Git / GitHub

\#\# Key Takeaways

This project helped me develop hands-on experience with:

\- TCP/IP networking  
\- Packet capture and analysis  
\- TCP connection establishment  
\- SSH  
\- Network reconnaissance  
\- Port scanning  
\- Wireshark filtering  
\- Basic security investigation and documentation

\#\# Future Improvements

Future versions of this lab will include:

\- DNS traffic investigation  
\- HTTP traffic analysis  
\- Detection of additional reconnaissance techniques  
\- Integration with a SIEM  
\- Creation of detection rules and security alerts  
