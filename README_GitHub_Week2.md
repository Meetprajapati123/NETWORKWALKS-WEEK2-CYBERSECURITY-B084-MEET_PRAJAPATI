# Footprinting, OSINT & Network Scanning Lab

![Cybersecurity](https://img.shields.io/badge/Focus-Cybersecurity-red)
![Program](https://img.shields.io/badge/Program-Networkwalks-blue)
![Week](https://img.shields.io/badge/Week-2-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

A practical cybersecurity lab documenting three Week 2 modules: **W2-PM1, W2-PM2 and W2-PM5**. The work covers passive footprinting, Google Hacking Database (GHDB) research, and host discovery on an authorized local network.

> **Responsible-use note:** Test only systems you own or have explicit written permission to assess. Do not publish exposed camera URLs, credentials, personal data, or other people's network details.

## Project Information

| Field | Details |
|---|---|
| Author | `Your Name` |
| Program | Cybersecurity Internship – Networkwalks |
| Modules | W2-PM1, W2-PM2, W2-PM5 |
| Date | `Add completion date` |
| Status | Completed |
| Environment | Kali Linux, Zenmap/Nmap, Google Search |

## Table of Contents

1. [Objectives](#objectives)
2. [Lab Environment and Tools](#lab-environment-and-tools)
3. [W2-PM1 – Footprinting with Kali Linux Tools](#w2-pm1--footprinting-with-kali-linux-tools)
4. [W2-PM2 – Google Hacking Database (GHDB)](#w2-pm2--google-hacking-database-ghdb)
5. [W2-PM5 – Network Scanning with Zenmap](#w2-pm5--network-scanning-with-zenmap)
6. [Key Learnings](#key-learnings)
7. [Recommendations](#recommendations)
8. [Evidence and Screenshots](#evidence-and-screenshots)
9. [Disclaimer](#disclaimer)

## Objectives

- Understand how public information can reveal a website's technology and DNS footprint.
- Practice GHDB/Google dork research using search results only.
- Discover live hosts on an authorized local network using a ping scan.
- Record observations and recommend defensive improvements.

## Lab Environment and Tools

| Tool | Purpose | Module |
|---|---|---|
| `whois` | Domain registration and name-server information | W2-PM1 |
| `whatweb` | Website technology fingerprinting | W2-PM1 |
| `nslookup` | DNS resolution | W2-PM1 |
| `curl -I` | HTTP response-header inspection | W2-PM1 |
| `wafw00f` | Web Application Firewall detection | W2-PM1 |
| `dnsrecon` | DNS record enumeration | W2-PM1 |
| Google Search + Exploit-DB GHDB | Search-engine footprinting research | W2-PM2 |
| Zenmap / Nmap | Local host discovery and topology view | W2-PM5 |
| `ipconfig` | Local IP and subnet identification | W2-PM5 |

## W2-PM1 – Footprinting with Kali Linux Tools

**Goal:** Collect publicly available information about an authorized domain using six Kali Linux tools.

Commands used (replace the example domain with an authorized target):

```bash
whois example.com
whatweb example.com
nslookup example.com
curl -I https://example.com
wafw00f example.com
dnsrecon -d example.com
```

**What I practised:**
- Reviewing domain registration and name-server information with WHOIS.
- Identifying visible web technologies with WhatWeb.
- Resolving domain names with NSLookup.
- Reviewing HTTP response headers with cURL.
- Checking WAF detection with WAFW00F.
- Enumerating public DNS records with DNSRecon.

**Evidence:** Add sanitized screenshots in `screenshots/w2-pm1/`.

## W2-PM2 – Google Hacking Database (GHDB)

**Goal:** Understand how search operators can reveal information that has been unintentionally made public.

**Activities documented:**
- Reviewed relevant GHDB entries from Exploit-DB.
- Studied search queries for publicly indexed camera interfaces.
- Studied directory-listing search results containing mathematics PDF files.
- Recorded observations without attempting logins or operating devices.

**Safety and privacy:** Do not upload third-party camera links, identifiable locations, exposed personal information, credentials, or direct links to sensitive files. Use cropped/redacted evidence and describe findings at a high level.

**Evidence:** Add sanitized screenshots in `screenshots/w2-pm2/`.

## W2-PM5 – Network Scanning with Zenmap

**Goal:** Identify live devices on a network that you own or are explicitly authorized to test.

**Activities documented:**
1. Installed Zenmap from the official Nmap download page.
2. Checked the local IP address and subnet using `ipconfig`.
3. Selected the **Ping scan** profile in Zenmap.
4. Scanned the authorized local subnet.
5. Reviewed live-host results and the topology view.

Example command for an authorized lab subnet only:

```bash
nmap -sn <YOUR_AUTHORIZED_SUBNET>
```

Replace the placeholder with your own authorized lab subnet.

**Evidence:** Add sanitized screenshots in `screenshots/w2-pm5/`. Redact IPs, MAC addresses, device names, and details you do not want publicly indexed.

## Key Learnings

- Footprinting builds an initial picture of a system before deeper security testing.
- DNS records and HTTP headers can disclose infrastructure information.
- GHDB demonstrates why organizations should review what search engines index.
- A ping scan helps identify active hosts on an authorized local network.
- Clear documentation and responsible handling of findings are essential cybersecurity skills.

## Recommendations

- Keep website platforms, themes, and plugins updated.
- Review public information and remove unnecessary technical disclosures.
- Apply suitable HTTP security headers.
- Review DNS and email-authentication configurations.
- Restrict directory listings and protect administrative interfaces.
- Keep cameras and IoT devices behind appropriate access controls.
- Periodically review assets within the organization's authorized scope.

## Evidence and Screenshots

Add your own screenshots to these folders:

| Module | Evidence folder |
|---|---|
| W2-PM1 | `screenshots/w2-pm1/` |
| W2-PM2 | `screenshots/w2-pm2/` |
| W2-PM5 | `screenshots/w2-pm5/` |

## Disclaimer

This repository is for educational purposes and documents controlled learning activities. Perform scans and security testing only on systems you own or where you have explicit written authorization. Do not access, monitor, or collect information from third-party systems without permission.
