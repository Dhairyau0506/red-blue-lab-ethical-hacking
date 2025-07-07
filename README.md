# Digital Hide & Seek: A Cybersecurity Lab Adventure

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
- **Ubuntu Linux** — Target machine (Linux-based)
- **Windows 7** — Target machine (vulnerable legacy OS)
- **Virtualization** — Isolated network using VirtualBox
- **No internet connectivity** — For safe testing

---

## Tools-Set

- 🔍 Nmap – Port scanning & reconnaissance  
- 🦈 Wireshark – Packet sniffing  
- 🛠️ Metasploit – Payload generation and handler setup  
- 💉 SQLmap – SQL injection testing  
- 🔐 Hydra – Password brute-forcing  
- 🕷️ Burp Suite – Web proxy and vulnerability analysis  
- 📋 Event Viewer, Netstat, Task Manager – Blue team forensics  
- 🧱 AppLocker, Windows Firewall, Sysmon – Defensive hardening  

---

## Red Team Activities (Attacker Perspective)

- Network scanning using `arp-scan` and Nmap
- Identified firewall-blocked targets
- Created a reverse HTTPS payload with `msfvenom`
- Used social engineering (fake installer + README) to deliver the payload
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

## Full Report

[Download the full report (PDF)](./report.pdf)

This detailed write-up covers all steps taken, mistakes made, and lessons learned in the lab environment.

---

## What I Learned

- Firewalls can be extremely effective—even basic ones
- Social engineering often beats brute force
- Post-exploitation requires caution and persistence
- Defenders have to catch **everything**, attackers only need to succeed **once**
- Small things (like logins, file size, or hidden paths) can be major clues

---

## What's Next?

I'm planning to:
- Explore Active Directory labs and lateral movement
- Learn detection engineering using Sigma + Sysmon
- Try SIEM tools like Splunk or Wazuh
- Try new attacks as a red teamer
- Exploring Burp Suite for web hacking (ethical ofcourse!)

---

## Let’s Connect!

If you have feedback, suggestions, or want to collaborate, feel free to reach out. I’m always learning and open to ideas!

---
