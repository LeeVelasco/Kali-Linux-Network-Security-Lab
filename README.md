# Kali Linux Network Security Lab

**Tools:** Kali Linux | Nmap | Bash  
**Platform:** Virginia Cyber Range  
**Course:** MIS 420 – Information Security & Assurance  
**Institution:** George Mason University – Costello College of Business

---

## Overview

This hands-on lab was completed using the Virginia Cyber Range — a 
state-funded cybersecurity training platform. Using Kali Linux and Nmap, 
the lab covers practical network reconnaissance techniques including host 
discovery, port scanning, service detection, and OS fingerprinting.

---

## Lab Objectives

- Navigate the Kali Linux terminal environment
- Identify active hosts on a network subnet
- Perform TCP SYN and service version scans
- Detect operating systems and open services
- Interpret Nmap scan output for security analysis

---

## Commands Performed

### 1. Network Interface Discovery
```bash
ip addr show
```
Identified active network interfaces and IP address assignments 
on the Kali Linux host.

### 2. Host Discovery (Ping Sweep)
```bash
nmap -sn 10.1.174.252/20
```
Scanned the /20 subnet to identify all live hosts. 
Discovered 6 active hosts across 4,096 IP addresses scanned.

### 3. SYN Scan (Stealth Scan)
```bash
nmap -sS -T4 10.1.160.1
```
Performed a fast TCP SYN scan on a target host to identify 
open, closed, and filtered ports without completing the handshake.

### 4. Service Version Detection
```bash
nmap -sV 10.1.160.1
```
Probed open ports to identify running services and their versions — 
critical for identifying known vulnerabilities.

### 5. Aggressive Scan (OS + Traceroute)
```bash
nmap -A 10.1.160.1
```
Combined OS detection, version scanning, script scanning, and 
traceroute to build a full profile of the target host.

### 6. Nmap Service Database
```bash
cd /usr/share/nmap
xdg-open serviceversionsOS.xml
```
Explored Nmap's built-in service and OS fingerprint database 
used to match scan results to known services.

---

## Key Findings

| Scan Type | Target | Result |
|---|---|---|
| Ping Sweep | 10.1.174.252/20 | 6 hosts discovered |
| SYN Scan | 10.1.160.1 | 1000 ports filtered |
| Service Scan | 10.1.160.1 | Services identified |
| OS Detection | 10.1.160.1 | Fingerprint attempted |

---

## Skills Demonstrated

- Kali Linux command-line navigation
- Network reconnaissance with Nmap
- TCP SYN scanning and stealth techniques
- Service version and OS fingerprinting
- Interpreting scan output for vulnerability assessment
- Working in a sandboxed cybersecurity lab environment

---

## Platform

This lab was conducted on the **Virginia Cyber Range** — a 
cybersecurity training environment provided by the Commonwealth 
of Virginia for higher education institutions.

---

## Author

**Ruszel Lee Velasco**  
B.S. Business – Management Information Systems  
George Mason University, 2025
