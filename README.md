# Windows 10 Internal Penetration Test & Incident Response Report

Welcome to my first hands-on cybersecurity project, where I built a safe, virtual lab environment to simulate ethical hacking attacks and defense techniques. This was a deep dive into the world of red teaming, blue teaming, and digital forensics, all from a beginner’s perspective.

---

## Project Objective

To understand both the attack and defense sides of cybersecurity by:
- Creating a virtual ethical hacking lab
- Executing simulated cyberattacks (red team)
- Detecting and mitigating those attacks (blue team)
- Implementing basic system hardening techniques

---

## Lab Setup

- **Kali Linux** — Attacker machine
- **Windows 10** — Target machine
- **Virtualization** — Isolated network using VirtualBox
- **No internet connectivity** — For safe testing

---

## Tools-Set

- 🔍 Nmap – Port scanning & reconnaissance  
- 🛠️ Metasploit – Payload generation and handler setup   
- 📋 Event Viewer, Sysmon, Task Manager – Blue team forensics  
- 🧱 AppLocker, Windows Firewall, Sysmon – Defensive hardening  

---

## Red Team Activities (Attacker Perspective)

- Network scanning using `arp-scan` and Nmap
- Identified firewall-blocked targets
- Created a reverse HTTPS payload with `msfvenom`
- Used social engineering (fake salary pdf.exe double extension) to deliver the payload
- Hosted the payload via a local Python HTTP server
- Gained remote shell access via Metasploit
- Performed basic post-exploitation and system enumeration

---

## Blue Team Activities (Defender Perspective)

- Analyzed Windows logs (Event IDs 4624, 4672) to identify intrusions
- Detected unusual network activity using `netstat`
- Identified and killed malicious processes
- Investigated suspicious files in `%TEMP%` and `%AppData%`
- Discovered payload disguising as `svchost.exe`

---

## Hardening and Prevention

- Configured AppLocker to block executables from `%TEMP%`, `%AppData%`, and `Downloads`
- Set custom Windows Firewall outbound rules to stop payload communications
- Enabled and updated Windows Defender
- Installed **Sysmon** for deeper system logging
- Regularly monitored startup items and scheduled tasks

---


## What I Learned

- Firewalls can be extremely effective—even basic ones
- Social engineering often beats brute force
- Post-exploitation requires caution and persistence
- Defenders have to catch **everything**, attackers only need to succeed **once**
- Small things (like logins, file size, or hidden paths) can be major clues

---



## Let’s Connect!

If you have feedback, suggestions, or want to collaborate, feel free to reach out. I’m always learning and open to ideas!

---
