# NETWORKWALKS-B084-WK2-PM-FOOTPRINTING-AND-NETWORK-SCANNING

![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Penetration%20Testing-red?style=flat-square)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-Reconnaissance-blue?style=flat-square&logo=kalilinux)
![Zenmap](https://img.shields.io/badge/Zenmap-Network%20Scanning-green?style=flat-square)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-B084-black?style=flat-square)

# Penetration Testing Report
## Footprinting & Network Scanning Phases

**Week 02 Project — NetworkWalks Cybersecurity Internship**

## Project Overview

This repository documents my Week 2 practical cybersecurity activities as part of the **NetworkWalks Cybersecurity Internship Program (Batch B084)**.

The project focuses on two important phases of penetration testing:

1. **Reconnaissance & Footprinting**
2. **Scanning & Network Discovery**

The first activity involved gathering publicly available information about the NetworkWalks.com domain using multiple Kali Linux reconnaissance tools.

The second activity involved discovering live hosts on my own local network using Zenmap (Nmap GUI), identifying IP and MAC addresses, and generating a network topology.

Additionally, I used **theHarvester** to collect publicly available information associated with a target domain through passive reconnaissance techniques.

All activities were performed within the authorized scope.

## Project Objectives

- Gather domain registration information using WHOIS.
- Identify website technologies using WhatWeb.
- Resolve domain names and IP addresses using Nslookup.
- Analyze HTTP response headers using cURL.
- Identify Web Application Firewall (WAF) indicators using WAFW00F.
- Enumerate DNS records using DNSRecon.
- Gather publicly available information using theHarvester.
- Discover live hosts on my local network using Zenmap.
- Identify local IP and MAC addresses using Windows CMD.
- Generate a network topology.
- Understand the importance of reconnaissance and scanning in penetration testing.

## Modules Completed

| Module | Activity |
|---|---|
| W2-PM1 | Footprinting using Multiple Kali Linux Tools |
| W2-PM4 | Footprinting with theHarvester |
| W2-PM5 | Network Scanning using Zenmap |

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration testing and reconnaissance environment |
| WHOIS | Domain registration information gathering |
| WhatWeb | Website technology fingerprinting |
| Nslookup | DNS resolution |
| cURL | HTTP response header inspection |
| WAFW00F | Web Application Firewall detection |
| DNSRecon | DNS record enumeration |
| theHarvester | Passive information gathering |
| Zenmap | Network scanning and host discovery |
| Nmap | Network discovery engine |
| Windows CMD | Local network configuration and MAC identification |

## Lab Environment

| Component | Configuration |
|---|---|
| Operating System | Kali Linux |
| Secondary System | Windows PC |
| Target Domain | NetworkWalks.com |
| Local Network | Own LAN |
| Reconnaissance Tools | Kali Linux utilities |
| Network Scanning | Zenmap / Nmap |
| Project Date | 12 November 2026 |
| Training Batch | B084 |

## Methodology

### 1. WHOIS – Domain Information Gathering

Used WHOIS to collect publicly available domain registration information.

Information reviewed:

- Domain registrar
- Registration details
- Domain status
- Name servers
- Updated and expiration dates

### 2. WhatWeb – Website Fingerprinting

Used WhatWeb to identify technologies used by the target website.

**Observed findings included:**

- WordPress 7.1.4
- WP Download Manager 3.3.76
- Other publicly observable website technology information

### 3. Nslookup – DNS Resolution

Used Nslookup to resolve the target domain and identify its associated IP address.

**Observed IP address:**

`192.232.216.135`

### 4. cURL – HTTP Response Header Analysis

Used the cURL `-I` option to inspect HTTP response headers.

The activity provided information about:

- HTTP response behavior
- Server-related headers
- Web application information
- WordPress REST API endpoint: `/wp-json/`

### 5. WAFW00F – WAF Detection

Used WAFW00F to identify indicators of Web Application Firewall protection.

**Observed result:**

ModSecurity (SpiderLabs).

### 6. DNSRecon – DNS Enumeration

Used DNSRecon to gather publicly available DNS information.

Records examined included:

- NS records
- MX records
- TXT records
- SPF information
- SRV records
- DNS infrastructure information

### 7. theHarvester – Passive OSINT Reconnaissance

Used theHarvester to collect publicly available information associated with a target domain.

The exercise focused on identifying:

- Email addresses
- Subdomains
- Hostnames
- Publicly indexed domain-related information

**Command documented in the report:**

`theHarvester -d Microsoft.com -l 50 -b all`

This activity demonstrated how passive reconnaissance can help security professionals understand an organization's publicly visible footprint.

### 8. Zenmap – Network Scanning and Host Discovery

Used Zenmap (Nmap GUI) to perform network discovery on my own local network.

Activities included:

- Identifying local IP configuration using Windows CMD.
- Identifying the network subnet.
- Performing Ping Scan.
- Discovering active hosts.
- Reviewing IP and MAC address information.
- Generating network topology.
- Exporting the topology in PDF format.

### 9. Windows CMD – Network Configuration

Used Windows Command Prompt to identify:

- IPv4 address
- Subnet mask
- Default gateway
- Physical MAC address

## Risk Analysis and Observations

The practical activities revealed several security-relevant observations.

| No. | Finding | Potential Impact | Risk Level |
|---|---|---|---|
| 1 | Website technology information exposed | Helps identify technologies requiring security review | Medium |
| 2 | Server IP address identifiable | Provides information about hosting infrastructure | Low |
| 3 | HTTP technical information exposed | May assist technology fingerprinting | Low |
| 4 | WAF technology identifiable | Reveals information about security architecture | Low |
| 5 | DNS infrastructure information exposed | Helps build an infrastructure profile | Medium |
| 6 | Multiple live hosts visible on local network | Unknown devices may require investigation | Medium |

**Important:** These are reconnaissance observations, not confirmed vulnerabilities. No exploitation or vulnerability validation was performed during these modules.

## Security Recommendations

Based on the observations, the following improvements are recommended:

1. Regularly review publicly exposed website technology information.
2. Keep CMS platforms, plugins, and server software updated.
3. Review HTTP response headers for unnecessary information disclosure.
4. Periodically audit DNS records.
5. Properly configure and monitor the Web Application Firewall.
6. Perform regular internal network discovery.
7. Investigate unexpected devices on the network.
8. Maintain updated network topology documentation.
9. Conduct security testing only within an authorized scope.

## Learning Outcomes

Through this project, I gained practical experience in:

- Passive reconnaissance and OSINT.
- Domain registration information gathering.
- Website technology fingerprinting.
- DNS enumeration and analysis.
- HTTP response header inspection.
- Web Application Firewall identification.
- Information gathering using theHarvester.
- Network scanning and live host discovery.
- IP and MAC address identification.
- Network topology generation.
- Security risk analysis and technical documentation.

The project helped me understand how reconnaissance and scanning contribute to the initial stages of a penetration testing engagement.

## Project Documentation

The complete penetration testing report includes:

- Detailed commands and execution steps.
- Tool outputs and observations.
- Screenshots and evidence.
- Risk analysis.
- Security recommendations.
- Project conclusion.

**Report:** `W2-PM-FINAL-Report.docx`

## Repository Structure

```text
NETWORKWALKS-B084-WK2-PM-FOOTPRINTING-AND-NETWORK-SCANNING/
│
├── README.md
│
├── Screenshots/
│   ├── 01-whois.png
│   ├── 02-whatweb.png
│   ├── 03-nslookup.png
│   ├── 04-curl-headers.png
│   ├── 05-wafw00f.png
│   ├── 06-dnsrecon.png
│   ├── 07-theharvester.png
│   ├── 08-zenmap-scan.png
│   ├── 09-network-topology.png
│   └── 10-windows-network-config.png
│
├── Report/
│   ├── W2-PM-FINAL-Report.docx
│   
│
└── LICENSE
```

## Author

**Bigyan Tamang**

Cybersecurity Intern – NetworkWalks  
Batch: **B084**

LinkedIn: [Bigyan Tamang](https://www.linkedin.com/in/bigyan-tamang-776613200/)

## Project Information

- **Program:** Cybersecurity Program at NetworkWalks
- **Week:** 02
- **Project:** Footprinting & Network Scanning
- **Modules:** W2-PM1, W2-PM4, W2-PM5
- **Date:** 12 November 2026

---

**Disclaimer:** This project was conducted for educational and research purposes within an authorized scope. Reconnaissance and scanning activities were performed only against systems with permission or systems owned by me. The observations do not establish the existence of exploitable vulnerabilities.
