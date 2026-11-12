# Penetration Testing & Reconnaissance – Week 2

<p align="center">
  <strong>Cybersecurity Internship | Networkwalks</strong><br>
  <em>Footprinting • OSINT • Network Scanning</em>
</p>

<p align="center">
  ![Week](https://img.shields.io/badge/Week-02-blue)
  ![Program](https://img.shields.io/badge/Program-Networkwalks-red)
  ![Status](https://img.shields.io/badge/Status-Completed-success)
  ![Focus](https://img.shields.io/badge/Focus-Cybersecurity-black)
</p>

## Project Details

| Field | Details |
|---|---|
| **Name** | Prajapati Meet Ghanshyam |
| **Program** | Cybersecurity Internship – Networkwalks |
| **Batch** | B804 |
| **Date** | 12-11-2026 |
| **Week** | Week 2 |
| **Modules Completed** | W2-PM1, W2-PM2, W2-PM5 |
| **Project Status** | Completed |

---

## About This Project

This repository documents my Week 2 practical work during the Cybersecurity Internship at **Networkwalks**. The work focuses on the initial stages of penetration testing: collecting publicly available information, understanding search-engine exposure, and discovering active hosts on an authorized local network.

I completed three modules using Kali Linux tools, Google Hacking Database (GHDB) techniques, and Zenmap (Nmap GUI). This hands-on practice helped me understand how reconnaissance and network discovery support a security assessment.

## Table of Contents

1. [W2-PM1 – Footprinting with Multiple Kali Linux Tools](#w2-pm1--footprinting-with-multiple-kali-linux-tools)
2. [W2-PM2 – Google Hacking Database (GHDB)](#w2-pm2--google-hacking-database-ghdb)
3. [W2-PM5 – Network Scanning with Zenmap](#w2-pm5--network-scanning-with-zenmap)
4. [Tools & Technologies](#tools--technologies)
5. [Key Learnings](#key-learnings)
6. [Security Recommendations](#security-recommendations)
7. [Project Structure](#project-structure)
8. [Disclaimer](#disclaimer)

---

## W2-PM1 – Footprinting with Multiple Kali Linux Tools

**Objective:** Perform passive footprinting and gather publicly available information about the in-scope website and its DNS configuration.

### Tasks Performed

| No. | Tool | Purpose |
|---:|---|---|
| 1 | `whois` | Checked domain registration details and name servers. |
| 2 | `whatweb` | Identified visible website technologies and web-server information. |
| 3 | `nslookup` | Checked domain name resolution. |
| 4 | `curl -I` | Inspected HTTP response headers. |
| 5 | `wafw00f` | Checked for Web Application Firewall detection. |
| 6 | `dnsrecon` | Enumerated publicly available DNS records. |

### Commands Used

```bash
whois <authorized-domain>
whatweb <authorized-domain>
nslookup <authorized-domain>
curl -I https://<authorized-domain>
wafw00f <authorized-domain>
dnsrecon -d <authorized-domain>
```

### Learning Outcomes

- Understood how WHOIS can reveal domain registration information.
- Practised identifying web technologies with WhatWeb.
- Learned how to resolve domain names and review DNS information.
- Inspected HTTP response headers using cURL.
- Understood the role of a Web Application Firewall.
- Practised DNS enumeration and interpreting DNS records.

**Evidence:** See the `Screenshots` folder for W2-PM1 terminal outputs.

---

## W2-PM2 – Google Hacking Database (GHDB)

**Objective:** Learn how Google search operators and GHDB entries can identify information that has been publicly indexed.

### Tasks Performed

- Reviewed relevant Google Hacking Database entries from Exploit-DB.
- Studied a GHDB search technique related to publicly indexed webcam interfaces.
- Reviewed search results that exposed camera web interfaces.
- Explored directory-listing search results containing mathematics PDF ebooks.
- Recorded observations for security-awareness and defensive learning.

### Learning Outcomes

- Understood the purpose of Google Dorking and GHDB.
- Learned how search engines can index exposed web pages and directory listings.
- Recognized the importance of securing camera interfaces and restricting directory listing.
- Practised documenting findings while avoiding interaction with third-party devices.

**Safety note:** No login attempts were made and no camera controls were operated. Third-party camera URLs and identifying details are intentionally not published in this repository.

**Evidence:** See the `Screenshots` folder for sanitized W2-PM2 screenshots.

---

## W2-PM5 – Network Scanning with Zenmap

**Objective:** Discover active hosts and view basic network topology on the tester's own authorized local network.

### Tasks Performed

1. Installed Zenmap from the official Nmap download source.
2. Checked the local IP configuration and subnet using Windows `ipconfig`.
3. Selected the **Ping Scan** profile in Zenmap.
4. Performed host discovery on the authorized local subnet.
5. Reviewed the live-host results.
6. Examined the network topology view.

### Command Used

```bash
nmap -sn <your-authorized-local-subnet>
```

### Result Summary

- The ping scan identified **2 live hosts** on the tested local subnet.
- The results included the tester's own computer and the local default gateway.
- The topology view displayed the scanning computer and discovered live hosts.

### Learning Outcomes

- Understood IP address and subnet identification.
- Practised host discovery using Zenmap/Nmap.
- Learned how to interpret ping-scan results.
- Explored basic network topology visualization.
- Understood why network scanning must stay within an authorized scope.

**Evidence:** See the `Screenshots` folder for sanitized W2-PM5 screenshots.

---

## Tools & Technologies

| Tool / Technology | Area |
|---|---|
| Kali Linux | Security testing environment |
| WHOIS | Domain information gathering |
| WhatWeb | Website technology fingerprinting |
| NSLookup | DNS lookup |
| cURL | HTTP header inspection |
| WAFW00F | WAF detection |
| DNSRecon | DNS enumeration |
| Google Search | Search-engine research |
| Exploit-DB GHDB | Google dork reference database |
| Zenmap / Nmap | Network host discovery |
| Windows `ipconfig` | Local network configuration |

## Key Learnings

- Reconnaissance is an important early stage of a penetration test.
- Publicly available information can reveal details about a website's technologies and DNS configuration.
- Search engines may expose resources that were unintentionally made public.
- Network scanning helps identify active hosts within an authorized network.
- Screenshots, notes, and clear reporting are essential parts of professional security work.
- Ethical testing requires a clearly defined scope and permission.

## Security Recommendations

Based on the types of information reviewed during these exercises:

- Keep website platforms, themes, and plugins updated.
- Avoid unnecessary disclosure of software versions and server details.
- Review HTTP security headers and apply suitable protections.
- Review DNS configuration and email-authentication policies.
- Restrict directory listing where it is not required.
- Protect camera interfaces and administrative panels with strong authentication and restricted access.
- Periodically review publicly indexed information about assets you own.

## Project Structure

```text
NETWORKWALKS-WEEK2-CYBERSECURITY/
│
├── README.md
│
├── Screenshots/
│   ├── whois.png
│   ├── whatweb.png
│   ├── nslookup.png
│   ├── curl.png
│   ├── wafw00f.png
│   ├── dnsrecon.png
│   ├── ghdb.png
│   ├── google-search.png
│   ├── ipconfig.png
│   ├── ping-scan.png
│   └── topology.png
│
└── Report/
    └── Week2-Pentest-Report.pdf
```

*The screenshot filenames above are suggested examples. Use the actual filenames of your uploaded evidence.*

## Disclaimer

This repository is intended for educational and defensive cybersecurity learning. All active scanning must be restricted to systems owned by the tester or covered by explicit written authorization. The GHDB exercise was limited to viewing public search results; no third-party camera controls were used and no login attempts were made. Sensitive information, third-party URLs, credentials, and identifying network details should not be published.

---

<p align="center">
  <strong>Week 2 – Learning • Practising • Improving</strong><br>
  <em>Prajapati Meet Ghanshyam | Networkwalks | Batch B804</em>
</p>
