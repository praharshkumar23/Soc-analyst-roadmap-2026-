# 📘 Beginner Basics — What Every SOC Fresher Must Know Before Starting Projects

[![Section](https://img.shields.io/badge/Sections-6-blue.svg)]()
[![Duration](https://img.shields.io/badge/Duration-2--4%20Weeks-orange.svg)]()
[![Level](https://img.shields.io/badge/Level-Absolute%20Beginner-brightgreen.svg)]()
[![Cost](https://img.shields.io/badge/Resources-100%25%20Free-success.svg)]()
[![Required](https://img.shields.io/badge/Status-Required%20Before%20Projects-red.svg)]()
[![SOC](https://img.shields.io/badge/Focus-SOC%20Analyst-blue.svg)]()

> **Read this before touching any project.**
> Most freshers jump straight into SIEM tools, alert triage, and incident response without understanding the fundamentals. That leads to surface-level knowledge, weak interview answers, and confusion when things don't go as expected.
>
> Spend **2–4 weeks** on this section. Everything in the project roadmap assumes you know this material. If you skip it, you will struggle. If you complete it, you will be more prepared than 80% of fresher candidates who apply for SOC roles.

**Build the foundation first. Then build the projects.**

---

## 📋 Table of Contents

- [How to Use This File](#how-to-use-this-file)
- [Section 1 — Networking Fundamentals](#section-1--networking-fundamentals)
- [Section 2 — Linux Basics](#section-2--linux-basics)
- [Section 3 — Windows Basics](#section-3--windows-basics)
- [Section 4 — Cyber Attacks 101](#section-4--cyber-attacks-101)
- [Section 5 — Cybersecurity Core Concepts](#section-5--cybersecurity-core-concepts)
- [Section 6 — Basic Analyst Tools](#section-6--basic-analyst-tools)
- [Final Checklist Before Starting Projects](#final-checklist-before-starting-projects)

---

## 🗂️ How to Use This File

Work through each section **in order**. Do not skip ahead.

Each section includes:
- **Why it matters for SOC** — so you know why you are learning it
- **What you must understand** — the actual knowledge required
- **Free resources** — exactly where to learn it at zero cost
- **Checkpoint** — how to confirm you are ready to move on

**Suggested pace:**

| Days | Sections | Focus |
|------|----------|-------|
| 1–5 | 1 and 2 | Networking + Linux |
| 6–10 | 3 and 4 | Windows + Cyber Attacks |
| 11–14 | 5 and 6 | Core Concepts + Analyst Tools |
| 15–21 | All | Practice, revision, quick notes |

After completing all 6 sections, open `QUICK-START-GUIDE.md` and begin Project 1.

---

## 🌐 Section 1 — Networking Fundamentals

### Why This Matters for SOC

Networking is the foundation of everything in security operations. Every alert is triggered by network activity. Every attack uses the network at some stage. Every log tells a network story — source IP, destination IP, port, protocol, bytes transferred.

If you cannot read an IP address, understand what a port means, or explain why TCP and UDP behave differently, you will not understand why alerts fire. You will not be able to investigate suspicious connections. You will not be able to tell the difference between legitimate traffic and attacker communication.

This is not optional knowledge. It is table stakes.

---

### 1.1 IP Addressing

```
IPv4
- Format: four octets separated by dots — 192.168.1.100
- Range: 0.0.0.0 to 255.255.255.255

Private IP Ranges (internal, not routable on internet)
- 10.0.0.0    to 10.255.255.255
- 172.16.0.0  to 172.31.255.255
- 192.168.0.0 to 192.168.255.255

Public IP
- Any IP outside the private ranges above
- Used on the open internet

Why it matters in SOC:
- 192.168.x.x in a log = internal traffic
- Unusual public IP connecting inbound = investigate it
- Attackers route C2 traffic through public IPs

Subnetting and CIDR Basics
- 192.168.1.0/24 = first 24 bits are network, last 8 are hosts
- /24 = 254 usable hosts
- /32 = single specific host

NAT (Network Address Translation)
- Converts private IPs to one public IP for internet access
- 500 internal machines can share one public IP
- SOC implication: need internal logs to trace which machine made a connection

IPv6
- Format: 2001:0db8:85a3:0000:0000:8a2e:0370:7334
- Increasingly common in modern networks
- SOC analysts must recognize it in logs
```

---

### 1.2 DNS — Domain Name System

```
What DNS Does
- Translates domains (google.com) to IP addresses
- Without DNS you would type 142.250.195.46 instead of google.com

How DNS Resolution Works
1. You type google.com in browser
2. Computer checks local cache
3. If not cached → recursive DNS resolver (usually ISP)
4. Resolver asks root nameserver → TLD (.com) → authoritative nameserver
5. Returns IP address to your browser

DNS Record Types
A      → domain to IPv4 address (google.com → 142.x.x.x)
AAAA   → domain to IPv6 address
MX     → mail server for a domain
CNAME  → alias pointing to another domain
TXT    → text data, used for SPF/DKIM/DMARC
PTR    → reverse DNS (IP to domain)

Why DNS Matters in SOC
- C2 Beaconing: malware uses DNS to communicate with attacker
- DNS Tunneling: attacker hides exfiltration data inside DNS queries
- Newly registered domains, random names like a7f3bx1.xyz = red flag
- High DNS query volume from one host = possible malware
- DNS to unusual TLDs (.xyz, .top, .pw) = suspicious
```

---

### 1.3 Core Protocols

```
TCP — Transmission Control Protocol
- Connection-oriented: establishes connection before sending data
- Reliable: guarantees delivery, retransmits lost packets
- Used for: HTTP, HTTPS, SSH, SMB, RDP

TCP 3-Way Handshake (memorize this — asked in every interview)
  SYN     → Client: "I want to connect"
  SYN-ACK → Server: "OK, I acknowledge"
  ACK     → Client: "Connection established"

SOC relevance:
- Incomplete handshakes (SYN flood) = denial of service
- SYN to many ports from one IP = port scanning

UDP — User Datagram Protocol
- Connectionless: sends data without establishing connection
- Fast but no retransmission guarantee
- Used for: DNS, DHCP, VoIP, video streaming

ICMP — Internet Control Message Protocol
- Used for ping (echo request/reply) and traceroute
- Not a transport protocol — diagnostic only
- Abused by attackers for: covert channels, recon, DDoS

HTTP vs HTTPS
- HTTP:  unencrypted, port 80, traffic visible in plaintext
- HTTPS: encrypted with TLS, port 443, traffic not readable without key
- SOC concern: HTTP should be minimal in modern networks
- HTTPS-based C2 is common — attackers blend into normal browsing
```

---

### 1.4 Common Ports — Memorize These

| Port | Protocol | Notes for SOC |
|------|----------|---------------|
| 21 | FTP | File transfer — often unencrypted, flag unusual outbound |
| 22 | SSH | Secure shell — brute force is extremely common |
| 23 | Telnet | Completely insecure — should never appear in modern networks |
| 25 | SMTP | Email sending — watch for spam relay attempts |
| 53 | DNS | Always review DNS traffic patterns |
| 80 | HTTP | Flag plaintext browsing — should be rare in enterprise |
| 110 | POP3 | Email retrieval |
| 143 | IMAP | Email access |
| 443 | HTTPS | Normal web traffic — also used heavily for C2 |
| 445 | SMB | File sharing — EternalBlue, ransomware spread here |
| 1433 | MSSQL | Database — flag any unusual external connections |
| 3306 | MySQL | Database access |
| 3389 | RDP | Remote Desktop — very common attack target |
| 4444 | Custom | Default Metasploit listener — major red flag |
| 5985 | WinRM | Windows Remote Management — used for lateral movement |
| 8080 | HTTP Alt | Often used by proxies and C2 frameworks |

---

### 1.5 OSI Model — Simplified for SOC

```
Full OSI Model has 7 layers. These 4 matter most for analysts:

Layer 3 — Network
  - IP addressing and routing
  - Source/destination IP lives here
  - Protocols: IP, ICMP

Layer 4 — Transport
  - TCP and UDP
  - Port numbers live here
  - SYN floods and port scans happen at this layer

Layer 5/6 — Session/Presentation
  - TLS/SSL encryption lives here
  - Why you cannot read HTTPS traffic without a proxy

Layer 7 — Application
  - What the user sends and receives
  - HTTP, DNS, SMTP, FTP, SMB all live here
  - Most SIEM alerts are Layer 7 events

Why it matters:
- Firewall blocks at Layer 3/4 (IP + port)
- IDS/IPS inspects Layer 7 (content)
- Understanding layers tells you where to look in logs
```

---

### 1.6 Packet Analysis with Wireshark

```
Wireshark is a free packet capture and analysis tool.
Every SOC analyst should know the basics.

Install: wireshark.org (free, Windows/Linux/Mac)

Basic Filters
ip.addr == 192.168.1.5          → all traffic to/from this IP
ip.src == 10.0.0.1              → only traffic from this IP
ip.dst == 8.8.8.8               → only traffic to Google DNS
tcp.port == 443                 → HTTPS traffic only
tcp.port == 4444                → suspicious Metasploit traffic
dns                             → all DNS queries
http                            → all HTTP requests
tcp.flags.syn == 1              → all SYN packets

Following a TCP Stream
- Right-click packet → Follow → TCP Stream
- See full conversation between two hosts
- Useful for reading HTTP requests and responses

Common Investigation Scenarios
- SYN flood:      massive SYN packets from one source, no SYN-ACK
- Port scan:      one IP hitting many ports in quick sequence
- C2 beacon:      small packets at regular intervals to external IP
- DNS tunneling:  unusually long DNS queries with encoded data
- Data exfil:     large outbound transfer to unusual destination
```

---

### 📚 Free Resources — Section 1

- TryHackMe: "Pre-Security" path → Network Fundamentals module (free)
- TryHackMe: "Wireshark: The Basics" room (free)
- Professor Messer Network+ YouTube playlist (free, first 10 videos)
- NetworkChuck "Networking for Hackers" YouTube series
- Wireshark official documentation: wireshark.org

### ✅ Section 1 Checkpoint

You are ready to move on when you can:

- [ ] Explain the difference between TCP and UDP with one real example each
- [ ] Describe the TCP 3-way handshake step by step without looking it up
- [ ] Identify which IP addresses are private and which are public
- [ ] Name the port numbers for SSH, RDP, SMB, DNS, and HTTPS from memory
- [ ] Open Wireshark and filter traffic by IP address and port
- [ ] Explain why an attacker would use port 443 for C2 traffic
- [ ] Describe what DNS tunneling is and why it matters in SOC

---

## 🐧 Section 2 — Linux Basics

### Why This Matters for SOC

Nearly every enterprise SIEM, EDR agent, and open-source security tool runs on Linux. Log files live on Linux servers. Wazuh, Elastic Stack, Suricata, and Zeek are all Linux-based. Most SOC home lab work happens inside Linux VMs.

If you cannot use a Linux terminal confidently, you will waste hours troubleshooting basic issues during projects instead of actually learning security skills.

---

### 2.1 Navigation and File Management

```
Command              What It Does
-----------          --------------------------------------------------
ls                   List files in current directory
ls -la               List all files including hidden, with permissions
cd /var/log          Change to /var/log directory
pwd                  Show current directory path
mkdir logs           Create a directory called logs
rm file.txt          Delete a file
rm -rf folder        Delete a folder and all contents (be careful)
cp file1 file2       Copy file1 to file2
mv file1 /tmp        Move file1 to /tmp
touch notes.txt      Create an empty file

Reading Files
cat file.txt              Print entire file to terminal
less file.txt             Scroll through file (q to quit)
head -20 file.txt         Show first 20 lines
tail -20 file.txt         Show last 20 lines
tail -f /var/log/syslog   Follow a live log in real time

File Permissions
-rw-r--r-- 1 root root 4096 auth.log
 r=read  w=write  x=execute
 First set:  owner permissions
 Second set: group permissions
 Third set:  everyone else

chmod 644 file.txt    Set permissions
chown user:group file Change owner
```

---

### 2.2 Searching and Filtering — Critical for Log Analysis

```bash
# Find all failed SSH password attempts
grep "Failed password" /var/log/auth.log

# Case-insensitive search for "error"
grep -i "error" /var/log/syslog

# Search all files in /var/log for a specific IP
grep -r "192.168.1.100" /var/log/

# Count failed login attempts by username, most common first
grep "Failed password" /var/log/auth.log | awk '{print $11}' | sort | uniq -c | sort -rn

# Find usernames being brute-forced, ranked by frequency
cat /var/log/auth.log | grep "Invalid user" | awk '{print $10}' | sort | uniq -c | sort -rn

# Show successful SSH logins with username and source IP
grep "Accepted password" /var/log/auth.log | awk '{print $9,$11}'

# Find all log files modified in last 24 hours
find /var/log -name "*.log" -mtime -1

# Find all executable shell scripts (persistence hunting)
find / -name "*.sh" -perm /111 2>/dev/null
```

---

### 2.3 Processes and System Monitoring

```
ps aux
→ List all running processes with CPU and memory usage
→ Look for: unusual names, processes from /tmp, high CPU

top
→ Real-time process monitor, updated every few seconds
→ Press M = sort by memory | P = sort by CPU

htop
→ Better version of top, more visual
→ sudo apt install htop

kill 1234
→ Terminate process with PID 1234

pkill firefox
→ Kill all processes named firefox

netstat -tulpn
→ All active listening ports and owning process
→ t=TCP u=UDP l=listening p=process n=numeric

ss -tulpn
→ Modern replacement for netstat, same flags

systemctl status apache2
→ Check if a service is running

systemctl list-units --type=service --state=running
→ List all running services — spot malware-added services
```

---

### 2.4 Log File Locations — SOC Reference

| Log File | What It Contains |
|----------|-----------------|
| `/var/log/auth.log` | SSH logins, sudo commands, su attempts (Ubuntu/Debian) |
| `/var/log/secure` | Same content on CentOS/RHEL |
| `/var/log/syslog` | General system events and service messages |
| `/var/log/kern.log` | Kernel messages and hardware events |
| `/var/log/messages` | General system messages (CentOS/RHEL) |
| `/var/log/apache2/access.log` | Every HTTP request to the web server |
| `/var/log/apache2/error.log` | Web server errors and blocked requests |
| `/var/log/nginx/` | Nginx web server access and error logs |
| `/var/log/ufw.log` | UFW firewall allow/deny events |
| `/var/log/dpkg.log` | Package install and uninstall history |
| `/var/log/cron` | Scheduled task execution logs |
| `/var/log/wtmp` | Login and logout history — use `last` command |
| `/var/log/btmp` | Failed login history — use `lastb` command |

---

### 2.5 Users and Account Investigation

```
whoami                Current username
id                    User ID, group ID, and group memberships
id username           Check another user's groups

cat /etc/passwd       All user accounts on the system
                      Format: username:x:UID:GID:info:home:shell

cat /etc/shadow       Hashed passwords — root access only
                      Blank hash = no password set (security issue)

last                  Recent login history from /var/log/wtmp
lastb                 Failed login history from /var/log/btmp
lastlog               Last login time for every account
who                   Currently logged-in users

For Investigations
→ Check if new accounts were created recently
→ Look for accounts with UID 0 (root-level access)
→ Find accounts with /bin/bash shell that should not have it
```

---

### 2.6 Network Commands

```
ifconfig / ip a             Show network interfaces and IP addresses
ip route                    Show routing table

ping 8.8.8.8                Test connectivity
ping -c 4 192.168.1.1       Send exactly 4 pings

traceroute 8.8.8.8          Show hops to destination

curl -I https://google.com  Get HTTP headers from a URL
wget https://example.com    Download a file

nmap -sV 192.168.1.1        Scan host for open ports and services
nmap -sn 192.168.1.0/24     Ping scan entire subnet
```

---

### 📚 Free Resources — Section 2

- TryHackMe: "Linux Fundamentals Part 1, 2, 3" (free rooms)
- OverTheWire Bandit wargame: overthewire.org/wargames/bandit (levels 0–15)
- Install Ubuntu Server on VirtualBox (free) and practice every command daily
- CommandLineFu.com — real-world Linux one-liners including grep combos

### ✅ Section 2 Checkpoint

You are ready when you can:

- [ ] Navigate the Linux file system from terminal without using a GUI
- [ ] Read `/var/log/auth.log` and identify failed SSH attempts
- [ ] Use `grep` and pipes to count and sort log events
- [ ] List all running processes and identify unusual ones
- [ ] Check which ports are open and which process owns each
- [ ] Find recently modified log files using `find`
- [ ] Identify new or suspicious user accounts in `/etc/passwd`

---

## 🪟 Section 3 — Windows Basics

### Why This Matters for SOC

Most enterprise endpoints run Windows. Windows desktops and servers generate the majority of SOC alerts. Windows Event Logs are the primary evidence source in most incident investigations.

A SOC analyst who cannot read a Windows event log confidently is not ready for the job.

---

### 3.1 Windows Event IDs — Must Memorize

These Event IDs appear in SOC alerts, SIEM rules, and interviews constantly.

**Authentication Events**

| Event ID | What It Means | SOC Relevance |
|----------|--------------|---------------|
| 4624 | Successful logon | Check logon type (2=interactive, 3=network, 10=remote) |
| 4625 | Failed logon | #1 brute force indicator — >10 in 5 min from same IP = alert |
| 4634 | Logoff | Session tracking |
| 4648 | Logon with explicit credentials | Used in pass-the-hash, lateral movement |
| 4672 | Special privileges assigned | Admin session — should only be known admins |
| 4740 | Account locked out | Confirms brute force happened |

**Account Management Events**

| Event ID | What It Means | SOC Relevance |
|----------|--------------|---------------|
| 4720 | New user account created | Attacker may create backdoor accounts |
| 4722 | User account enabled | |
| 4724 | Password reset attempt | |
| 4726 | User account deleted | |
| 4732 | User added to privileged group | Critical — watch Administrators, Domain Admins |

**Process and Persistence Events**

| Event ID | What It Means | SOC Relevance |
|----------|--------------|---------------|
| 4688 | New process created | Most important for malware detection |
| 4689 | Process terminated | |
| 4698 | Scheduled task created | Common attacker persistence method |
| 4702 | Scheduled task modified | |
| 7045 | New service installed | Malware installs itself as a service |

**Security Events**

| Event ID | What It Means | SOC Relevance |
|----------|--------------|---------------|
| 1102 | Security log cleared | Major red flag — attacker covering tracks |
| 4719 | Audit policy changed | Attacker disabling detection |

---

### 3.2 Where to Find Logs in Windows

```
Event Viewer
- Open: Win+R → eventvwr.msc → Enter
- Or search "Event Viewer" in Start menu

Log Categories
Security     → 4624, 4625, 4688 — most important for SOC
System       → 7045 (new service installs), driver events
Application  → Software errors and events
Setup        → Windows installation events

Custom Views
- Filter by specific Event ID
- Example: Security log filtered to 4625 only

PowerShell Operational Log
- Microsoft-Windows-PowerShell/Operational
- Logs every PowerShell command run on the system
- Attackers use PowerShell heavily — this log is gold

Sysmon (Free — install on every lab machine)
- Enhanced logging: process creation, network connections, file creation
- Much more detail than default Windows logging
- Every SOC analyst should know what Sysmon is
```

---

### 3.3 Windows Tools Every SOC Analyst Should Know

**Built-in Tools**

```
Task Manager (Ctrl+Shift+Esc)
→ Running processes, CPU and memory usage
→ Right-click process → Open file location
→ Flag: no description, running from unusual path

Resource Monitor (resmon.exe)
→ Per-process view of CPU, memory, disk, network
→ Network tab shows active connections per process

netstat -ano
→ All active connections with PID
→ Match PID to process in Task Manager
→ Example: netstat -ano | findstr 4444

ipconfig /all
→ Full network config including DNS servers
→ Unusual DNS server = possible DNS hijack

tasklist /svc      → Processes with associated services
sc query           → All services and current status
```

**Sysinternals Suite (Free from Microsoft)**

```
Process Explorer
→ Advanced Task Manager — parent-child process tree
→ Check each process against VirusTotal
→ Highlights unsigned binaries (common malware indicator)

Autoruns
→ Everything set to run at startup or login
→ Registry run keys, scheduled tasks, services, browser extensions
→ Unsigned entries = investigate immediately

TCPView
→ Real-time live view of TCP and UDP connections
→ With process names and ports — like netstat but visual

Strings
→ Extract readable text from binary files
→ Quick malware analysis without a sandbox
```

---

### 3.4 Registry Awareness

```
What is the Registry
- Hierarchical database storing Windows configuration
- Attackers modify registry keys to survive reboots

Key Persistence Locations

HKLM\Software\Microsoft\Windows\CurrentVersion\Run
→ Runs for ALL users at startup — classic malware location

HKCU\Software\Microsoft\Windows\CurrentVersion\Run
→ Runs for CURRENT user only at startup

HKLM\System\CurrentControlSet\Services
→ All installed services — malware installs here

HKLM\Software\Microsoft\Windows NT\CurrentVersion\Image File Execution Options
→ Debugger hijacking — attacker replaces legitimate binary

How to Check
- regedit.exe → navigate to key manually
- PowerShell: Get-ItemProperty 'HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run'
- Autoruns (Sysinternals) — shows all at once, easiest method
```

---

### 3.5 File System — Key Locations

**Legitimate System Paths**

```
C:\Windows\System32       Core OS binaries (cmd.exe, svchost.exe)
C:\Windows\SysWOW64       32-bit binaries on 64-bit systems
C:\Program Files          Installed 64-bit applications
C:\Program Files (x86)    Installed 32-bit applications
C:\ProgramData            Application data for all users
```

**Common Malware Drop Locations**

```
C:\Users\<name>\AppData\Roaming      Very common — hidden from casual view
C:\Users\<name>\AppData\Local\Temp   Malware often executes from here
C:\Temp or C:\Windows\Temp           Attacker staging directory
C:\Users\Public                      World-writable, no attention drawn
```

**Red Flags**

```
- svchost.exe running from AppData instead of System32 → fake svchost
- Process with system-sounding name in wrong location
- Executables with random names like xkZj3p.exe
- DLLs in unusual locations loaded by legitimate processes
```

---

### 3.6 PowerShell for SOC

```powershell
# Last 50 Security events
Get-EventLog -LogName Security -Newest 50

# Last 100 failed logon events
Get-EventLog -LogName Security -InstanceId 4625 -Newest 100

# Top 10 processes by CPU
Get-Process | Sort-Object CPU -Descending | Select-Object -First 10

# Processes using more than 50% CPU
Get-Process | Where-Object {$_.CPU -gt 50}

# Active established TCP connections
Get-NetTCPConnection | Where-Object {$_.State -eq "Established"}

# Connections to suspicious port 4444
Get-NetTCPConnection | Where-Object {$_.RemotePort -eq 4444}

# All enabled scheduled tasks
Get-ScheduledTask | Where-Object {$_.State -eq "Ready"}

# All local user accounts with last login
Get-LocalUser | Select-Object Name, Enabled, LastLogon

# All running services
Get-Service | Where-Object {$_.Status -eq "Running"}
```

---

### 📚 Free Resources — Section 3

- TryHackMe: "Windows Fundamentals Part 1, 2, 3" (free rooms)
- Blue Team Labs Online: Windows event log investigation labs (free tier)
- Microsoft Sysinternals Suite: docs.microsoft.com/sysinternals
- Install Windows 10 VM on VirtualBox and practice Event Viewer weekly

### ✅ Section 3 Checkpoint

You are ready when you can:

- [ ] Name Event IDs for successful login, failed login, new process, and new service without notes
- [ ] Open Event Viewer and filter the Security log for Event ID 4625
- [ ] Explain the difference between logon type 2 and logon type 10 in Event ID 4624
- [ ] Use Process Explorer to find a process's full path and parent process
- [ ] Use Autoruns to identify what executes at Windows startup
- [ ] Write a PowerShell command to show the last 100 failed logons
- [ ] Identify the file paths where malware most commonly drops files

---

## ⚔️ Section 4 — Cyber Attacks 101

### Why This Matters for SOC

A SOC analyst detects and responds to attacks. If you don't understand how attacks work, you cannot recognize them in logs. You need attacker-side awareness — not to become an attacker, but to think like one long enough to spot what they leave behind.

---

### 4.1 The Cyber Kill Chain

Developed by Lockheed Martin. Every attack follows this general sequence.

| Stage | Name | What Happens | SOC Relevance |
|-------|------|-------------|---------------|
| 1 | Reconnaissance | Attacker gathers info (OSINT, scanning) | Hard to detect — may show in firewall or honeypot logs |
| 2 | Weaponization | Creates payload (malware, exploit) | Happens on attacker side — not visible to defenders |
| 3 | Delivery | Sends it to victim (email, web, USB) | Email gateway, proxy logs, web filter alerts |
| 4 | Exploitation | Vulnerability is triggered | EDR alerts, process creation logs (Event 4688) |
| 5 | Installation | Malware installed for persistent access | New services (7045), scheduled tasks (4698), new files |
| 6 | Command and Control | Malware beacons back to attacker | Network logs, DNS logs, beaconing patterns |
| 7 | Actions on Objective | Data theft, ransomware, lateral movement | File access logs, large transfers, encryption activity |

---

### 4.2 MITRE ATT&CK Framework

```
What It Is
- Structured knowledge base of real-world attacker behavior
- Maintained by MITRE Corporation
- Used by every major SOC team worldwide
- Free at attack.mitre.org

Structure
- Tactics (14 total): what the attacker wants to achieve
  Initial Access, Execution, Persistence, Privilege Escalation,
  Defense Evasion, Credential Access, Discovery, Lateral Movement,
  Collection, C2, Exfiltration, Impact

- Techniques: how they achieve each tactic
  Each tactic has multiple techniques
  Example: T1059 Command and Scripting Interpreter (Execution)
  Sub-techniques: T1059.001 PowerShell | T1059.003 Windows Command Shell

Key Techniques Every Fresher Must Know
T1078   Valid Accounts                  (persistence, lateral movement)
T1053   Scheduled Task                  (persistence)
T1059   Scripting Interpreter           (PowerShell, cmd.exe)
T1021   Remote Services                 (RDP, SMB, WinRM)
T1486   Data Encrypted for Impact       (ransomware)
T1055   Process Injection               (malware hiding in legit processes)
T1566   Phishing                        (initial access)
T1110   Brute Force                     (credential access)
T1071   Application Layer Protocol      (C2 over HTTP/HTTPS/DNS)
T1003   Credential Dumping              (Mimikatz, LSASS)
```

---

### 4.3 Common Attack Types with Detection Guidance

**BRUTE FORCE**
```
What it is: Attacker tries many passwords until one works

Detection:
- Windows: Event ID 4625 (multiple from same source IP)
- Linux:   /var/log/auth.log — "Failed password" repeated
- SIEM rule: >10 failed logins in 5 minutes = alert
- Confirm success: check if Event ID 4624 followed 4625

Response: Block source IP, check for subsequent successful login
MITRE:    T1110 — Brute Force
```

**PHISHING**
```
What it is: Deceptive email tricks user into clicking link or opening attachment

Detection:
- Email gateway alert on suspicious attachment or URL
- SPF/DKIM/DMARC failure in email headers
- Proxy logs: user accessed newly registered or flagged domain
- User reports suspicious email

What to check: email headers, sender reputation, link destination,
attachment hash on VirusTotal, SPF/DKIM pass or fail
MITRE: T1566 — Phishing
```

**MALWARE INFECTION**
```
What it is: Malicious software installed on endpoint

Detection:
- Event ID 4688: suspicious new process (cmd.exe from Word)
- EDR alert on unusual behavior
- High CPU or memory from unknown process
- Outbound connections to unusual external IPs
- .exe file created in AppData or Temp

What to check: process tree, parent process, hash on VirusTotal,
file location, network connections
MITRE: T1059, T1055, T1036
```

**RANSOMWARE**
```
What it is: Malware that encrypts files and demands payment

Early indicators (before files encrypted):
- Event 4688: vssadmin.exe with "delete shadows" argument
- Sudden mass file modifications or renames
- High disk I/O from unknown process
- New files with random extensions (.locked, .encrypted)

Later indicators:
- Ransom note in folders (README.txt, DECRYPT_MY_FILES.html)
- Files inaccessible or corrupted

Key Event IDs: 4688 (process), 4698 (scheduled task persistence)
MITRE: T1486 — Data Encrypted for Impact
```

**LATERAL MOVEMENT**
```
What it is: Attacker moves from one compromised machine to others

Common methods:
- PsExec:          runs commands on remote machine over SMB (port 445)
- WMI:             Windows Management Instrumentation for remote execution
- RDP:             Remote Desktop to hop between machines
- Pass-the-Hash:   uses stolen hash without cracking it

Detection:
- Same account logging into multiple machines in short time
- Event 4624 type 3 (network login) from unusual source
- Admin accounts used from non-admin workstations
- psexesvc.exe appearing on target (Event 7045)

MITRE: T1021 — Remote Services
```

**COMMAND AND CONTROL (C2)**
```
What it is: Communication channel between malware and attacker

Common methods:
- HTTPS to external IP (blends with normal traffic)
- DNS queries with encoded data (DNS tunneling)
- Beaconing — regular small packets at fixed intervals

Detection:
- Beacon: packet every 30/60 seconds to same external IP
- Unusual DNS: long subdomains, high frequency queries
- Traffic to newly registered domain or flagged IP
- Connections on unusual ports (4444, 8080, 1337)

MITRE: T1071 — Application Layer Protocol
```

**CREDENTIAL DUMPING**
```
What it is: Attacker extracts password hashes from memory

Tools used: Mimikatz, ProcDump
Target:     LSASS process (Local Security Authority)

Detection:
- Event 4688: unusual process accessing lsass.exe
- Sysmon Event 10: process accessing LSASS memory
- EDR/AV alert for Mimikatz signatures

Why it matters: Once credentials are dumped, attacker moves freely
MITRE: T1003 — OS Credential Dumping
```

---

### 📚 Free Resources — Section 4

- MITRE ATT&CK Navigator: attack.mitre.org (browse all techniques)
- TryHackMe: "Intro to Cyber Security" path (free)
- TryHackMe: "Cyber Kill Chain" room (free)
- TryHackMe: "MITRE" room (free)
- Lockheed Martin Cyber Kill Chain paper (free PDF)
- CyberDefenders: free blue team labs with real attack scenarios

### ✅ Section 4 Checkpoint

You are ready when you can:

- [ ] Name all 7 stages of the Cyber Kill Chain without notes
- [ ] Explain what MITRE ATT&CK is and name 5 tactics
- [ ] Describe how to detect a brute force attack in Windows and Linux logs
- [ ] List 3 early indicators of a ransomware infection
- [ ] Explain what lateral movement is and how PsExec works
- [ ] Describe what C2 beaconing looks like in network traffic
- [ ] Map a phishing attack to the correct Kill Chain stage and MITRE technique

---

## 🧠 Section 5 — Cybersecurity Core Concepts

### Why This Matters for SOC

These concepts appear in every SOC interview. They define how analysts think, communicate, and prioritize. They are the shared language of the blue team.

---

### 5.1 The CIA Triad

```
Every security decision maps back to one of these three properties.

Confidentiality
- Data accessible only to authorized users
- Violation: attacker exfiltrates customer records
- Controls: encryption, access control, least privilege

Integrity
- Data not modified without authorization
- Violation: attacker tampers with financial records
- Controls: hashing, digital signatures, audit logs

Availability
- Systems and data accessible when needed
- Violation: DDoS attack takes down production servers
- Controls: redundancy, backups, load balancing

Interview tip: When describing an incident, name which CIA
property was violated. Shows structured analytical thinking.
```

---

### 5.2 Alert Classification — The Core of L1 Work

| Classification | What It Means | Action |
|---------------|--------------|--------|
| **True Positive (TP)** | Real attack, correctly detected | Investigate, escalate, contain |
| **False Positive (FP)** | Normal activity, wrongly flagged | Tune detection rule, document exception |
| **True Negative (TN)** | No attack, correctly quiet | Normal operation |
| **False Negative (FN)** | Real attack, NOT detected | Worst outcome — attacker slipped through |

```
SOC L1 Reality
- Most of the job is separating TP from FP
- Learning what "normal" looks like in your environment is the key skill
- Too many FPs → alert fatigue → analysts miss real FNs
- Good analysts tune rules to reduce FP without creating FN
```

---

### 5.3 Incident Response Lifecycle — NIST SP 800-61

```
Phase 1: Preparation
- Before any incident happens
- Playbooks written, team trained, tools installed
- SOC contribution: maintaining runbooks, testing detections

Phase 2: Detection and Analysis
- Identify that an incident is happening
- Determine scope, severity, affected systems
- SOC contribution: alert triage, initial investigation,
  evidence collection, timeline building

Phase 3: Containment, Eradication, Recovery
- Containment:  stop the spread (isolate machine, block IP)
- Eradication:  remove the threat (delete malware, revoke creds)
- Recovery:     restore systems to normal operation
- SOC contribution: executing playbooks, coordinating with IR team

Phase 4: Post-Incident Activity
- Write post-incident report
- Identify what failed and what to improve
- Update detection rules based on gaps found
- SOC contribution: documentation, lessons learned, rule tuning

Interview tip: Walk through these 4 phases when asked how you
would handle any incident scenario. Shows structured IR thinking.
```

---

### 5.4 IOC vs TTP

```
IOC — Indicator of Compromise
  Specific artifacts indicating a system may be compromised
  Examples:
  - IP address:  185.220.101.45
  - Domain:      malware-c2-server.xyz
  - File hash:   d41d8cd98f00b204e9800998ecf8427e
  - URL:         http://bad-domain.com/payload.exe
  - Email:       phishing@spoofed-domain.com

  Problem with IOCs:
  - Attacker changes IP → IOC is useless
  - Attacker recompiles malware → new hash
  - IOCs expire quickly — sometimes within hours

TTP — Tactics, Techniques, Procedures
  How the attacker operates — their behavior pattern
  Examples:
  - Uses PowerShell with base64-encoded commands
  - Deletes shadow copies before deploying ransomware
  - Uses legitimate admin tools (Living off the Land)
  - Beacons every 60 seconds over HTTPS

  Why TTPs are more valuable:
  - Attacker behavior changes slowly even when tools change
  - Detecting the technique catches future variants too
  - MITRE ATT&CK is entirely TTP-based

Good detection strategy:
  - Block known IOCs immediately (fast, tactical)
  - Build detections around TTPs (slow, strategic, durable)
```

---

### 5.5 Threat Intelligence Basics

```
What Is Threat Intelligence
- Processed information about adversaries and their methods
- Helps SOC teams understand who is attacking and how

Types
Strategic:   High-level, for executives (threat actor motivations)
Operational: Specific campaigns and attack patterns
Tactical:    TTPs mapped to MITRE ATT&CK
Technical:   Specific IOCs (IPs, hashes, domains)

Threat Feeds
- Curated lists of known malicious IOCs
- Auto-imported into SIEM to flag known-bad indicators
- Examples: AlienVault OTX, ThreatFox, Abuse.ch, MISP communities

Key Lookup Tools
VirusTotal    → Check IP, domain, URL, or file hash against 70+ engines
AbuseIPDB     → Has this IP been reported for malicious activity?
Shodan        → What services are exposed on this IP?
URLScan.io    → Safely analyze suspicious URLs
GreyNoise     → Is this IP a known internet scanner?
MXToolbox     → Check email domain SPF/DKIM/DMARC records

IOC Sharing Standards
STIX  → Standard format for describing threat intel
TAXII → Protocol for sharing STIX data between organizations
```

---

### 5.6 What Is a SIEM vs EDR

```
SIEM — Security Information and Event Management
- Collects logs from every source across the environment
- Correlates events and generates alerts based on rules
- Used for investigation, detection, and compliance
- Examples: Splunk, Microsoft Sentinel, Elastic SIEM, Wazuh

EDR — Endpoint Detection and Response
- Monitors endpoint behavior in real time
- Detects suspicious activity at the process level
- Can isolate a machine, kill a process, or pull forensic data
- Examples: CrowdStrike, Microsoft Defender for Endpoint, SentinelOne

Key difference:
- SIEM = sees everything across the environment (logs)
- EDR = sees deep behavior on individual endpoints (process level)
- In modern SOC environments, both are used together
```

---

### 📚 Free Resources — Section 5

- TryHackMe: "SOC Level 1" learning path (free)
- SANS Cyber Aces: free foundational cybersecurity course
- Professor Messer Security+ Domain 1 and 2 videos (free on YouTube)

### ✅ Section 5 Checkpoint

You are ready when you can:

- [ ] Explain the CIA Triad with one real example for each property
- [ ] Define TP, FP, TN, and FN without looking them up
- [ ] Walk through the 4 phases of incident response in order
- [ ] Explain the difference between an IOC and a TTP
- [ ] Explain why TTPs are more durable than IOCs for detection
- [ ] Describe SIEM vs EDR and when each is used

---

## 🔧 Section 6 — Basic Analyst Tools

### Why This Matters for SOC

These tools show up in every single project in this roadmap. And they are used daily in real SOC environments. Get comfortable with them before starting any project.

---

### 6.1 Tool Reference — What to Use and When

| Tool | What It Does | When to Use It |
|------|-------------|----------------|
| **Wireshark** | Capture and analyze network traffic | Investigating suspicious connections, PCAP analysis |
| **VirusTotal** | Check file hash, IP, domain, or URL | First step when you see an unknown IOC |
| **URLScan.io** | Safely analyze suspicious URLs | Phishing investigation, checking link destinations |
| **AbuseIPDB** | Check IP reputation and abuse reports | During alert triage when you see an unusual IP |
| **Shodan** | Search exposed internet-facing services | Understanding attacker recon or validating an IP |
| **Hybrid Analysis / Any.run** | Run suspicious files in sandbox | Malware analysis without risking your machine |
| **CyberChef** | Decode, encode, and transform data | Decoding base64, defanging IOCs, parsing obfuscated strings |
| **GreyNoise** | Check if IP is known internet scanner | Reducing false positives from scanner traffic |
| **MXToolbox** | Check email authentication records | Phishing investigation — verify SPF/DKIM/DMARC |

---

### 6.2 Wireshark Quick Reference

```
Install: wireshark.org (free)

Essential Filters
ip.addr == 192.168.1.5        All traffic to/from this IP
ip.src == 10.0.0.1            Only outbound from this IP
tcp.port == 443               HTTPS traffic
tcp.port == 4444              Suspicious Metasploit port
dns                           All DNS queries
http                          All HTTP requests
tcp.flags.syn == 1            SYN packets — detect port scans

Following a Stream
Right-click packet → Follow → TCP Stream
→ Read the full conversation between two hosts
→ See HTTP requests and responses in plaintext
```

---

### 6.3 CyberChef Quick Reference

```
Common Operations
- From Base64:      decode base64-encoded payloads
- URL Decode:       decode percent-encoded strings
- Defang URL:       make URLs safe to share (http → hxxp)
- Extract URLs:     pull URLs from messy log data
- From Hex:         decode hex-encoded strings
- XOR:              decode XOR-obfuscated content

Access free at: gchq.github.io/CyberChef
```

---

### 📚 Free Resources — Section 6

- VirusTotal: virustotal.com (free, no account needed for basic lookups)
- URLScan.io: urlscan.io (free submissions)
- AbuseIPDB: abuseipdb.com (free tier)
- CyberChef: gchq.github.io/CyberChef (completely free, no account)
- Any.run: any.run (free tier for public sandbox runs)
- TryHackMe: "OSINT" room, "Phishing Analysis" room

### ✅ Section 6 Checkpoint

You are ready when you can:

- [ ] Search an IP on AbuseIPDB and explain what the results mean
- [ ] Upload a file hash to VirusTotal and read the detection summary
- [ ] Submit a suspicious URL to URLScan.io and review the report
- [ ] Use CyberChef to decode a base64-encoded string
- [ ] Open Wireshark and filter by protocol or IP address
- [ ] Run a suspicious file in Any.run and identify what it does

---

## ✅ Final Checklist Before Starting Projects

> Complete every checkbox below. If you can answer all of these confidently, you are ready for Project 1.

**Networking**
- [ ] Explain the TCP 3-way handshake step by step
- [ ] Identify private vs public IP ranges
- [ ] Know port numbers for SSH, RDP, SMB, DNS, HTTPS, and 4444
- [ ] Filter a Wireshark capture by IP and port
- [ ] Explain why C2 traffic commonly uses port 443

**Linux**
- [ ] Navigate file system from terminal without GUI
- [ ] Parse failed SSH attempts from `/var/log/auth.log`
- [ ] Use `grep`, `awk`, `sort`, `uniq` to analyze log data
- [ ] Check open ports and the process owning each

**Windows**
- [ ] Name Event IDs 4624, 4625, 4688, 4698, 7045 from memory
- [ ] Filter Event Viewer by specific Event ID
- [ ] Use Process Explorer and Autoruns confidently
- [ ] Identify file paths commonly used by malware

**Attacks and Concepts**
- [ ] Name all 7 Cyber Kill Chain stages
- [ ] Explain IOC vs TTP and why TTPs are more durable
- [ ] Define TP, FP, TN, FN
- [ ] Walk through the 4-phase IR lifecycle
- [ ] Describe brute force, phishing, ransomware, and C2 simply

**Tools**
- [ ] Used VirusTotal, AbuseIPDB, URLScan.io, and CyberChef at least once
- [ ] Filtered a Wireshark packet capture by protocol and IP
- [ ] Decoded a base64 string in CyberChef

---

> ✅ **Basics complete. Now move to the projects.**
> You now have more foundational knowledge than 80% of freshers who apply for SOC roles. Time to turn that into real project work.

**[👉 Continue to -START-GUIDE.md →](STARTING-GUIDE-FRESH.md)**

---

<div align="center">

Made with 🔐 for aspiring SOC analysts

Part of the [SOC Analyst Training Roadmap 2026](README.md)

</div>
