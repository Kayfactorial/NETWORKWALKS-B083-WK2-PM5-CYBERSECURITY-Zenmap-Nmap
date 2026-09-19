<div align="center">

# 🔐 Zenmap / Nmap Network Discovery

**Network scanning using Zenmap/Nmap**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Zenmap-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.11.12.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Adio%20Kabiru-C00000?style=flat-square" />
</p>

---

## 📌 Project Overview

This project documents a practical network-discovery exercise performed with **Zenmap/Nmap 7.95** as part of the Networkwalks W2-PM4 cybersecurity assignment.

The exercise used a Ping Scan to identify active hosts on an authorized local `/24` network and then reviewed the results through Zenmap's Topology view.

> **Authorization and Ethics:** This repository is for cybersecurity education and authorized security assessment only. Scan only networks that you own or have explicit permission to assess.

## 🎯 Objectives

- Perform host discovery with Nmap.
- Use Zenmap as a graphical interface for Nmap.
- Identify active hosts on a local network.
- Record IP, MAC, and vendor information where available.
- Visualize discovered hosts using the Zenmap Topology view.
- Distinguish host discovery from vulnerability assessment.

## 🏗️ Tool and Environment

- **Zenmap / Nmap:** 7.95
- **Platform:** Kali Linux
- **Network scanned:** `10.11.12.0/24`
- **Scan type:** Ping Scan / host discovery

## 🔎 Command

```bash
nmap -sn 10.11.12.1/24
```

The `/24` prefix represents the `10.11.12.0/24` address space, covering 256 IPv4 addresses.

## ⚙️ Scan Summary

| Parameter | Result |
|---|---|
| Addresses scanned | 256 |
| Hosts reported up | 7 |
| Scan duration | 9.48 seconds |
| Scan type | Ping Scan |

## 🔎 Discovered Hosts

| IP Address | Status | MAC Address | Vendor |
|---|---|---|---|
| `10.11.12.1` | Up | `78:9A:18:61:35:19` | Routerboard.com |
| `10.11.12.245` | Up | `5A:3D:A7:46:AA:DC` | Unknown |
| `10.11.12.246` | Up | `4E:39:6B:F9:E4:5C` | Unknown |
| `10.11.12.247` | Up | `38:BA:F8:6B:9A:A4` | Intel Corporate |
| `10.11.12.248` | Up | `9A:62:6E:C0:95:BD` | Unknown |
| `10.11.12.249` | Up | 34:02:86:B9:11:A8 | Unknown |
| `10.11.12.254` | Up | `BC:5C:17:F5:1F:34` | Qingdao Intelligent&Precise Electronics |

## 🔎 Zenmap Topology

![Zenmap Topology](https://github.com/adkasu/NETWORKWALKS-B083-WK2-PM5-CYBERSECURITY-Zenmap-Nmap/blob/1f4fe23b459a30a071cf32790782130b154dfaed/Zenmap03.jpg)

*Figure 1: Zenmap Ping Scan and Topology view.*

The captured topology view visibly shows six hosts around `localhost`:

- `10.11.12.1`
- `10.11.12.246`
- `10.11.12.247`
- `10.11.12.248`
- `10.11.12.249`
- `10.11.12.254`

## Evidence Discrepancy

The command-line Nmap output reports **7 hosts up**, including `10.11.12.245`. The supplied Zenmap topology screenshot visibly shows **6 hosts** and does not display `10.11.12.245`.

This discrepancy is documented rather than silently corrected. The CLI output is used as the source for the total host count, while the topology description is limited to the hosts visible in the screenshot.

## Security Interpretation

Host discovery provides visibility into active systems but does **not** by itself prove that a host is vulnerable.

The four hosts with an unknown MAC vendor should be identified through authorized administrative or network-management records.

## Recommendations

- Maintain an accurate network asset inventory.
- Investigate unidentified devices.
- Periodically perform authorized host discovery.
- Preserve command-line and graphical evidence.
- Perform deeper port/service assessment only when explicitly authorized.

## 💡 Lessons Learned

1. Host discovery is an important early network-security activity.
2. Nmap output can provide useful IP and MAC/vendor information.
3. Zenmap can make scan results easier to visualize.
4. Evidence from different views should be compared for consistency.
5. Discovery is not the same as vulnerability assessment.

## 👤 Author

**Adio Kabiru**  
Network Engineer | Telecommunications Engineer | Cybersecurity Learner

#Cybersecurity #NetworkSecurity #Zenmap #Nmap #NetworkDiscovery #KaliLinux #EthicalHacking
