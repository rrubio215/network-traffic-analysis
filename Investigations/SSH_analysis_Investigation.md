# Investigation 01 — SSH Traffic Analysis

## Objective

Analyze an SSH connection between Kali Linux and Ubuntu Server and  
identify the hosts, ports, TCP connection process, and visibility of  
encrypted application traffic.

## Network Information

**Source Host:** Kali Linux    
**Source IP:** 192.168.1.81    
**Source Port:** 58230  

**Destination Host:** Ubuntu Server    
**Destination IP:** 192.168.1.245    
**Destination Port:** 22  

**Protocol:** TCP    
**Application:** SSH

## TCP Three-Way Handshake

The SSH connection began with the standard TCP three-way handshake:

```text  
Kali → Ubuntu     SYN  
Ubuntu → Kali     SYN, ACK  
Kali → Ubuntu     ACK  
