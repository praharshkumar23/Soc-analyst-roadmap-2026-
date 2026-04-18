# SOC Analyst Interview Preparation Guide

[![Questions](https://img.shields.io/badge/Questions-150%2B-blue.svg)]()
[![Basics](https://img.shields.io/badge/Basics-100-success.svg)]()
[![Scenarios](https://img.shields.io/badge/Scenario%20Based-50-red.svg)]()
[![Focus](https://img.shields.io/badge/Focus-SOC%20Interview-orange.svg)]()
[![Level](https://img.shields.io/badge/Level-Entry%20to%20Intermediate-brightgreen.svg)]()

This file is made for SOC Analyst interview prep. It covers 100 core questions and 50 scenario-based questions in one place.

The goal is simple: help you answer clearly in interviews, not just memorize lines.

---

## Table of Contents

1. [How to Use This File](#how-to-use-this-file)
2. [20 Basic Security Questions](#20-basic-security-questions)
3. [20 Event ID Questions](#20-event-id-questions)
4. [20 Networking and Ports Questions](#20-networking-and-ports-questions)
5. [20 SOC Concepts Questions](#20-soc-concepts-questions)
6. [20 Incident, Log, and Investigation Questions](#20-incident-log-and-investigation-questions)
7. [50 Scenario-Based Questions](#50-scenario-based-questions)
8. [Last-Minute Revision Sheet](#last-minute-revision-sheet)

---

## How to Use This File

- Read the answer once.
- Then close the file and answer in your own words.
- Keep answers short in real interviews unless the interviewer asks for more detail.
- For technical questions, try this format: **definition -> why it matters -> example**.
- For scenario questions, try this format: **detect -> validate -> investigate -> contain -> escalate -> document**.

---

## 20 Basic Security Questions

### 1) What is cybersecurity?
**Answer:** Cybersecurity is the practice of protecting systems, networks, applications, and data from unauthorized access, attack, damage, or disruption.

**Why it matters:** A company depends on confidentiality, integrity, and availability of data. Cybersecurity exists to reduce risk to those things.

---

### 2) What is the CIA triad?
**Answer:** CIA stands for Confidentiality, Integrity, and Availability.
- **Confidentiality:** only authorized users can access data.
- **Integrity:** data is accurate and not changed without permission.
- **Availability:** systems and data stay accessible when needed.

**Why it matters:** A lot of interview answers become stronger when you link them back to CIA.

---

### 3) What is a threat?
**Answer:** A threat is anything that can cause harm to a system, user, or organization. It can be a person, malware, insider, attacker group, or even a process failure.

**Why it happens:** Threats exist because systems have value and attackers want money, access, disruption, or data.

---

### 4) What is a vulnerability?
**Answer:** A vulnerability is a weakness in software, hardware, configuration, or process that can be exploited.

**Why it happens:** Bad coding, weak settings, missing patches, misconfigurations, or poor user behavior create vulnerabilities.

---

### 5) What is risk?
**Answer:** Risk is the chance that a threat will exploit a vulnerability and cause impact.

**Simple formula:** Risk = likelihood × impact.

---

### 6) What is an exploit?
**Answer:** An exploit is the method or code used to take advantage of a vulnerability.

**Example:** A remote code execution bug becomes dangerous when an attacker has an exploit for it.

---

### 7) What is malware?
**Answer:** Malware is malicious software designed to disrupt, damage, steal, spy, or gain unauthorized access.

**Types:** virus, worm, trojan, ransomware, spyware, rootkit, keylogger.

---

### 8) What is phishing?
**Answer:** Phishing is a social engineering attack where an attacker tricks a user into clicking a malicious link, opening an attachment, sharing credentials, or sending money.

**Why it works:** It abuses trust, urgency, fear, or curiosity.

---

### 9) What is ransomware?
**Answer:** Ransomware is malware that encrypts files or systems and demands payment.

**Why it happens:** Attackers use it for financial gain, often after phishing, exposed RDP, weak passwords, or privilege escalation.

---

### 10) What is social engineering?
**Answer:** Social engineering is manipulating people to reveal information or perform actions that help an attacker.

**Examples:** phishing, vishing, pretexting, baiting, impersonation.

---

### 11) What is authentication?
**Answer:** Authentication is the process of verifying identity.

**Examples:** password, OTP, smart card, fingerprint.

---

### 12) What is authorization?
**Answer:** Authorization decides what an authenticated user is allowed to do.

**Difference:** Authentication is “who are you?” Authorization is “what can you access?”

---

### 13) What is accounting in AAA?
**Answer:** Accounting records user activity and actions for auditing and monitoring.

**AAA:** Authentication, Authorization, Accounting.

---

### 14) What is least privilege?
**Answer:** Least privilege means giving users or systems only the minimum access needed to do their job.

**Why it matters:** It reduces blast radius if an account is misused.

---

### 15) What is MFA?
**Answer:** Multi-factor authentication uses two or more factors to verify identity.

**Factors:** something you know, something you have, something you are.

---

### 16) What is hashing?
**Answer:** Hashing converts input data into a fixed-length output.

**Why it is used:** integrity checks, password storage, file verification.

**Examples:** SHA-256, SHA-1, MD5. In practice, SHA-256 is much stronger than MD5 and SHA-1.

---

### 17) What is encryption?
**Answer:** Encryption transforms readable data into unreadable form using an algorithm and a key.

**Why it matters:** It protects confidentiality during storage and transmission.

---

### 18) Difference between IDS and IPS?
**Answer:**
- **IDS** detects and alerts.
- **IPS** detects and can block automatically.

**Easy line for interview:** IDS is passive detection, IPS is active prevention.

---

### 19) What is a firewall?
**Answer:** A firewall filters network traffic based on rules.

**Why it matters:** It allows or blocks traffic based on IP, port, protocol, application, or policy.

---

### 20) What is a VPN?
**Answer:** A VPN creates an encrypted tunnel between a user or site and another network.

**Why it matters:** It protects traffic over untrusted networks and supports secure remote access.

---

## 20 Event ID Questions

### 21) What is Windows Event ID 4624?
**Answer:** 4624 means a successful logon.

**Why it happens:** A user, service, or system account logged in successfully.

**SOC use:** Check logon type, source IP, account name, and time.

---

### 22) What is Event ID 4625?
**Answer:** 4625 means a failed logon attempt.

**Why it happens:** Wrong password, disabled account, bad username, expired account, or attack activity like brute force.

**SOC use:** Watch for repeated failures from one source.

---

### 23) What is Event ID 4634?
**Answer:** 4634 means an account logged off.

**Why it matters:** Useful in session tracking and login timeline analysis.

---

### 24) What is Event ID 4648?
**Answer:** 4648 means a logon was attempted using explicit credentials.

**Why it happens:** A user or process supplied alternate credentials.

**SOC use:** Important for lateral movement or credential misuse analysis.

---

### 25) What is Event ID 4672?
**Answer:** 4672 means special privileges were assigned to a new logon.

**Why it matters:** Often linked to admin or highly privileged accounts.

---

### 26) What is Event ID 4688?
**Answer:** 4688 means a new process was created.

**Why it happens:** A program was started.

**SOC use:** Great for detecting suspicious tools like `powershell.exe`, `cmd.exe`, `rundll32.exe`, `wmic.exe`.

---

### 27) What is Event ID 4689?
**Answer:** 4689 means a process ended.

**Why it matters:** Useful with 4688 for process lifetime and activity tracking.

---

### 28) What is Event ID 4697?
**Answer:** 4697 means a service was installed on the system.

**Why it matters:** Attackers use malicious services for persistence.

---

### 29) What is Event ID 4698?
**Answer:** 4698 means a scheduled task was created.

**Why it happens:** Admin automation or attacker persistence.

**SOC use:** Check task name, command, author, and timing.

---

### 30) What is Event ID 4700/4701/4702?
**Answer:** These relate to scheduled tasks being enabled, disabled, or updated.

**Why it matters:** Attackers may modify tasks after initial compromise.

---

### 31) What is Event ID 4719?
**Answer:** 4719 means system audit policy was changed.

**Why it matters:** Threat actors may weaken logging to hide activity.

---

### 32) What is Event ID 4720?
**Answer:** 4720 means a user account was created.

**Why it matters:** Could be normal admin work or unauthorized account creation.

---

### 33) What is Event ID 4722?
**Answer:** 4722 means a user account was enabled.

**SOC use:** Suspicious if an old or disabled account becomes active unexpectedly.

---

### 34) What is Event ID 4723 and 4724?
**Answer:**
- **4723:** an attempt was made to change an account password.
- **4724:** an attempt was made to reset an account password.

**Why it matters:** Important in account takeover investigations.

---

### 35) What is Event ID 4725 and 4726?
**Answer:**
- **4725:** a user account was disabled.
- **4726:** a user account was deleted.

**SOC use:** Check who performed the action and whether it matches change control.

---

### 36) What is Event ID 4732 or 4733?
**Answer:**
- **4732:** a member was added to a security-enabled local group.
- **4733:** a member was removed.

**Why it matters:** Privilege escalation often shows up in group membership changes.

---

### 37) What is Event ID 4740?
**Answer:** 4740 means a user account was locked out.

**Why it happens:** Too many failed logon attempts, often from user mistakes or brute-force activity.

---

### 38) What is Event ID 4768?
**Answer:** 4768 means a Kerberos authentication ticket (TGT) was requested.

**SOC use:** Useful in domain logon analysis and Kerberos attack investigations.

---

### 39) What is Event ID 4769?
**Answer:** 4769 means a Kerberos service ticket was requested.

**Why it matters:** Helpful in service access review and Kerberoasting investigations.

---

### 40) What is Event ID 4771 or 4776?
**Answer:**
- **4771:** Kerberos pre-authentication failed.
- **4776:** domain controller tried to validate credentials.

**Why it matters:** Useful for brute-force, password spray, and auth failure investigations.

---

### 41) What is Event ID 1102?
**Answer:** 1102 means the audit log was cleared.

**Why it matters:** This is highly suspicious because attackers often clear logs to hide evidence.

---

### 42) What is Event ID 7045?
**Answer:** 7045 means a new service was installed.

**Why it matters:** Common in persistence, malware deployment, and remote execution cases.

---

## 20 Networking and Ports Questions

### 43) What is an IP address?
**Answer:** An IP address identifies a device on a network.

**Types:** IPv4 and IPv6.

---

### 44) What is the difference between private and public IP?
**Answer:**
- **Private IP:** used inside local networks.
- **Public IP:** reachable over the internet.

**Why it matters:** Helps separate internal host activity from internet-facing activity.

---

### 45) What is a MAC address?
**Answer:** A MAC address is a hardware address used at Layer 2 for local network communication.

---

### 46) What is DNS?
**Answer:** DNS translates domain names into IP addresses.

**Why it matters in SOC:** Attackers use DNS for phishing, C2, tunneling, and malicious redirection.

---

### 47) What is DHCP?
**Answer:** DHCP automatically assigns IP addresses and network settings to devices.

---

### 48) What is NAT?
**Answer:** NAT translates private IP addresses to public IP addresses and vice versa.

**Why it matters:** In investigations, many hosts may appear behind one public IP.

---

### 49) What is TCP?
**Answer:** TCP is a connection-oriented protocol that provides reliable delivery.

**Why it matters:** Used when data must arrive correctly and in order.

---

### 50) What is UDP?
**Answer:** UDP is connectionless and faster but does not guarantee delivery.

**Why it matters:** Used in DNS, streaming, VoIP, and some monitoring traffic.

---

### 51) What is the TCP three-way handshake?
**Answer:** SYN -> SYN-ACK -> ACK.

**Why it matters:** Helps establish a reliable TCP session.

---

### 52) What is a port?
**Answer:** A port identifies a service or application on a host.

**Why it matters:** SOC analysts often investigate unusual ports or unexpected services.

---

### 53) What does port 20/21 do?
**Answer:** FTP data and FTP control.

**Risk:** Plain FTP is insecure because credentials can be exposed.

---

### 54) What does port 22 do?
**Answer:** SSH.

**SOC view:** Secure remote administration. Repeated failures may indicate brute force.

---

### 55) What does port 23 do?
**Answer:** Telnet.

**Risk:** Insecure because traffic is not encrypted.

---

### 56) What does port 25 do?
**Answer:** SMTP.

**SOC view:** Important in phishing and mail relay investigations.

---

### 57) What does port 53 do?
**Answer:** DNS.

**SOC view:** Watch for suspicious domains, large query volume, or tunneling behavior.

---

### 58) What does port 67/68 do?
**Answer:** DHCP.

---

### 59) What does port 80 do?
**Answer:** HTTP.

**Risk:** Unencrypted web traffic.

---

### 60) What does port 110 do?
**Answer:** POP3.

**Use:** Email retrieval.

---

### 61) What does port 123 do?
**Answer:** NTP.

**SOC view:** Time sync matters because bad time breaks log correlation.

---

### 62) What does port 135 do?
**Answer:** RPC.

**SOC view:** Can appear in Windows admin activity and lateral movement.

---

### 63) What does port 137/138/139 do?
**Answer:** NetBIOS services.

**SOC view:** Older Windows network activity. Can appear in enumeration or file sharing.

---

### 64) What does port 143 do?
**Answer:** IMAP.

---

### 65) What does port 161/162 do?
**Answer:** SNMP.

**SOC view:** Useful for monitoring, but weak SNMP configs can be abused.

---

### 66) What does port 389 do?
**Answer:** LDAP.

**SOC view:** Important in Active Directory queries and possible enumeration.

---

### 67) What does port 443 do?
**Answer:** HTTPS.

**SOC view:** Encrypted web traffic. Malicious traffic can hide inside it.

---

### 68) What does port 445 do?
**Answer:** SMB.

**SOC view:** Big one for file sharing, lateral movement, ransomware spread, and admin activity.

---

### 69) What does port 3389 do?
**Answer:** RDP.

**SOC view:** Common target for brute force and unauthorized remote access.

---

### 70) What is a subnet?
**Answer:** A subnet divides a network into smaller parts.

**Why it matters:** Helps you understand whether two IPs are local, routed, or in separate segments.

---

### 71) What is the OSI model?
**Answer:** A 7-layer model used to understand how data moves through networks.

**Layers:** Physical, Data Link, Network, Transport, Session, Presentation, Application.

---

### 72) What is a packet capture or PCAP?
**Answer:** A PCAP is a recorded network traffic file used for analysis.

**SOC use:** Useful in malware traffic, beaconing, phishing callback, and data exfiltration analysis.

---

## 20 SOC Concepts Questions

### 73) What is a SOC?
**Answer:** A Security Operations Center is a team and function that continuously monitors, detects, investigates, and responds to security events.

---

### 74) What does a SOC Analyst L1 do?
**Answer:** L1 analysts monitor alerts, triage them, validate suspicious activity, document findings, escalate real incidents, and close false positives.

---

### 75) What is SIEM?
**Answer:** SIEM stands for Security Information and Event Management. It centralizes logs and helps detect suspicious activity through searches, rules, and correlation.

---

### 76) What is EDR?
**Answer:** EDR stands for Endpoint Detection and Response. It focuses on endpoint visibility, suspicious behavior, process activity, and response actions.

---

### 77) SIEM vs EDR?
**Answer:**
- **SIEM:** broad log aggregation and correlation across many sources.
- **EDR:** deep endpoint visibility and response.

**Easy line:** SIEM sees across the environment, EDR sees deeply on the host.

---

### 78) What is an alert?
**Answer:** An alert is a notification triggered by a rule, threshold, anomaly, or security event that may need investigation.

---

### 79) What is an incident?
**Answer:** An incident is a confirmed security event that violates policy or threatens systems, users, or data.

---

### 80) What is a false positive?
**Answer:** A false positive is an alert that looks suspicious but is actually benign.

---

### 81) What is a true positive?
**Answer:** A true positive is an alert that correctly identifies malicious or unauthorized activity.

---

### 82) What is a false negative?
**Answer:** A false negative is when malicious activity happens but the detection fails to alert on it.

**Why it matters:** This is often more dangerous than a false positive.

---

### 83) What is an IOC?
**Answer:** IOC means Indicator of Compromise.

**Examples:** malicious IP, domain, URL, file hash, email sender, registry key.

---

### 84) What is a TTP?
**Answer:** TTP means Tactics, Techniques, and Procedures.

**Why it matters:** TTPs describe attacker behavior, not just one indicator.

---

### 85) What is MITRE ATT&CK?
**Answer:** MITRE ATT&CK is a framework that maps attacker behavior into tactics and techniques.

**SOC use:** good for detection mapping, investigation, and reporting.

---

### 86) What is log correlation?
**Answer:** Log correlation means connecting events from different systems to understand one activity or attack chain.

---

### 87) What is triage?
**Answer:** Triage is the process of reviewing an alert, checking context, deciding severity, and determining next steps.

---

### 88) What is severity?
**Answer:** Severity shows how serious an alert or incident is based on impact, confidence, asset criticality, and scope.

---

### 89) What is escalation?
**Answer:** Escalation means passing an alert or incident to a higher team or analyst level when it needs deeper action.

---

### 90) What is threat intelligence?
**Answer:** Threat intelligence is information about threats, actors, infrastructure, behaviors, or indicators used to improve defense.

---

### 91) What is use case tuning?
**Answer:** Tuning means improving detection logic to reduce noise and improve quality.

**Example:** excluding known admin tools or expected service accounts.

---

### 92) What is a playbook?
**Answer:** A playbook is a documented set of steps for handling a specific type of alert or incident.

---

## 20 Incident, Log, and Investigation Questions

### 93) What is the incident response lifecycle?
**Answer:** Preparation, Identification, Containment, Eradication, Recovery, and Lessons Learned.

---

### 94) What is containment?
**Answer:** Containment limits the spread or impact of an incident.

**Examples:** isolate host, disable account, block IP, remove malicious domain access.

---

### 95) What is eradication?
**Answer:** Eradication removes the root cause.

**Examples:** delete malware, remove persistence, patch vulnerability, reset credentials.

---

### 96) What is recovery?
**Answer:** Recovery restores systems to normal operations and verifies they are clean.

---

### 97) Why are logs important in SOC?
**Answer:** Logs provide evidence. They show who did what, when, where, and sometimes how.

---

### 98) What makes a good investigation note?
**Answer:** Short, factual, timestamped, evidence-based notes.

**Good format:** alert summary, evidence checked, findings, decision, escalation or closure reason.

---

### 99) What is lateral movement?
**Answer:** Lateral movement is when an attacker moves from one host or account to another inside the environment.

**Examples:** RDP, SMB, PsExec, WMI, stolen credentials.

---

### 100) What is privilege escalation?
**Answer:** Privilege escalation is when an attacker gains higher permissions than originally available.

---

### 101) What is persistence?
**Answer:** Persistence is a method attackers use to maintain access after reboot, logout, or cleanup.

**Examples:** scheduled task, service, startup item, registry run key.

---

### 102) What is command and control (C2)?
**Answer:** C2 is communication between a compromised system and an attacker-controlled server.

---

### 103) What is data exfiltration?
**Answer:** Data exfiltration is unauthorized transfer of data out of the environment.

---

### 104) What is brute force?
**Answer:** Brute force is repeated login guessing against an account or service.

---

### 105) What is password spraying?
**Answer:** Password spraying uses one or a few common passwords against many accounts.

**Difference from brute force:** It spreads attempts to avoid lockouts.

---

### 106) What is beaconing?
**Answer:** Beaconing is regular periodic traffic from a host to an external system, often seen in malware C2.

---

### 107) What is a file hash and why check it?
**Answer:** A file hash is a fingerprint of a file. Analysts check it to compare samples against known malware or trusted files.

---

### 108) What is sandboxing?
**Answer:** Sandboxing runs a file or URL in an isolated environment to observe behavior safely.

---

### 109) Why is PowerShell often monitored?
**Answer:** PowerShell is powerful and legitimate, but attackers also use it for download, execution, discovery, and persistence.

---

### 110) Why is `rundll32.exe` suspicious sometimes?
**Answer:** It is a legitimate Windows binary, but attackers abuse it to run malicious DLLs or scripts.

---

### 111) Why is `wmic.exe` suspicious sometimes?
**Answer:** It is a legitimate admin tool, but attackers use it for discovery, remote execution, and system queries.

---

### 112) Why is `cmd.exe` or `powershell.exe` spawned by Office suspicious?
**Answer:** Office apps usually should not launch command interpreters. This can indicate macro abuse or malicious document execution.

---

## 50 Scenario-Based Questions

### 1) You see 50 failed logins from one IP against one user in 5 minutes. What do you do?
**Answer:** Check whether the source IP is internal or external, review Event ID 4625 details, look for lockout events like 4740, confirm whether there is eventually a successful login, and determine if it is brute force or user error. If malicious, block or escalate and document affected user, source, and timeline.

---

### 2) A user reports a suspicious email with an attachment. What are your first steps?
**Answer:** Preserve the email, review sender, headers, URLs, attachment type, and delivery path. Detonate or hash-check the attachment safely, search if other users got the same email, and isolate impacted hosts if execution occurred.

---

### 3) You find Event ID 1102 on a critical server. What does it mean and what do you do?
**Answer:** It means the audit log was cleared. Treat it as suspicious, identify who cleared it, correlate with logon, process, and admin activity, check EDR data, and escalate because it may indicate defense evasion.

---

### 4) There is an alert for PowerShell downloading a file from the internet. How do you investigate?
**Answer:** Check command-line arguments, parent process, user, host, destination URL or IP, file path, hash, and whether the file executed. Search for related process creation, network connections, persistence, and similar activity on other hosts.

---

### 5) A user account was added to the local Administrators group. What next?
**Answer:** Validate whether the change was approved, identify who added the user, when it happened, and on which asset. Check related Event IDs, logons, ticket records, and whether the account started suspicious admin actions afterward.

---

### 6) You see repeated outbound connections every 60 seconds to one external IP. What could it be?
**Answer:** It may be beaconing. Check destination reputation, protocol, port, timing regularity, process responsible, and whether the host shows other malicious indicators like suspicious processes or persistence.

---

### 7) An endpoint triggered malware detection, but the user says nothing happened. What do you do?
**Answer:** Do not rely only on user statement. Review the detection, file path, hash, process tree, quarantine status, execution evidence, and whether the same hash appeared elsewhere. Then decide if it is true positive, blocked attempt, or false positive.

---

### 8) A scheduled task was created at 2:13 AM on a user workstation. What makes this suspicious?
**Answer:** Unusual time, unknown author, suspicious command, random task name, or parent process can all raise concern. Check Event ID 4698, task XML if available, linked process events, and user context.

---

### 9) RDP login succeeded from an unusual country. How would you handle it?
**Answer:** Validate whether the company allows remote access from that region, confirm VPN context, review user travel status, check for preceding failed logins, and search for post-login behavior like file access, privilege use, or lateral movement.

---

### 10) You see many 4624 successful logins outside office hours. Is that always bad?
**Answer:** No. It could be service accounts, admins, remote workers, or maintenance. I would validate account type, logon type, source, historical behavior, and whether the asset is sensitive before calling it malicious.

---

### 11) A user clicked a phishing link but says they did not enter credentials. What do you check?
**Answer:** Review proxy or browser logs, DNS lookups, URL reputation, whether any redirects or downloads happened, and whether authentication attempts occurred soon after. Then monitor the account for suspicious sign-ins.

---

### 12) You find SMB connections from one workstation to many hosts in minutes. What might that indicate?
**Answer:** Possible lateral movement, worm-like behavior, admin script, or scanning. I would check if the host is an admin jump box, review process activity, user context, file access, and timing.

---

### 13) A domain admin account logged in to a normal user workstation. Why is that important?
**Answer:** High-value accounts should not log in casually to user endpoints. It increases credential theft risk. I would validate if it was planned admin activity and check for follow-on suspicious actions.

---

### 14) You get an impossible travel alert. How do you verify it?
**Answer:** Check source IPs, VPN/proxy use, device identifiers, user agent, timestamps, and whether one login might be from a cloud security service or mobile network. Then decide if it is suspicious or expected.

---

### 15) A host is making DNS requests to random-looking domains. What could that mean?
**Answer:** It could indicate DGA malware, tunneling, or automated malicious infrastructure lookup. I would inspect domain patterns, frequency, NXDOMAIN rates, process source, and any matching C2 behavior.

---

### 16) An alert says `winword.exe` spawned `powershell.exe`. Why do analysts care?
**Answer:** Office applications usually should not spawn scripting engines. This can indicate macro abuse or malicious documents. I would inspect the command line, downloaded payloads, and user actions around the event.

---

### 17) A service named `UpdateService123` was installed. What would you review?
**Answer:** Service name, binary path, signer, creator account, creation time, host criticality, and whether the binary is known good. Random names in temp or user paths are especially suspicious.

---

### 18) You see a spike in 4771 failures across many users. What attack does that suggest?
**Answer:** Possible password spraying or Kerberos auth attack. I would review source systems, targeted accounts, timing spread, and whether any account later succeeded.

---

### 19) A browser downloaded a ZIP, then `cmd.exe` launched. What is your workflow?
**Answer:** Trace the file origin, hash the ZIP and extracted payload, inspect process tree, check if persistence or network connections followed, and isolate if execution is confirmed.

---

### 20) A user says their account locked out repeatedly. How do you investigate?
**Answer:** Check 4740 events, source systems, services or saved credentials using the old password, mapped drives, mobile devices, and whether failures come from a single host or many.

---

### 21) You see outbound traffic to port 4444. Is that bad?
**Answer:** Not automatically. Context matters. I would identify the process, destination, frequency, asset role, and whether the traffic matches known tools, malware, or legitimate applications.

---

### 22) A new local user account appears on a server. What do you do?
**Answer:** Validate change approval, identify creator account, check if the new user gained admin rights, review logon activity, and determine whether it is persistence or expected maintenance.

---

### 23) A host suddenly starts talking to many countries it never contacted before. What does that suggest?
**Answer:** It may indicate compromised software, malware callback, CDN changes, or data exfiltration. I would review destination types, process owners, bytes transferred, and timing.

---

### 24) You see many small outbound HTTPS connections to one rare domain. What do you check?
**Answer:** Domain age, reputation, certificate details, process responsible, JA3 if available, request timing, and whether the host has suspicious parent-child process events.

---

### 25) A user received MFA prompts they did not initiate. What might be happening?
**Answer:** Possible MFA fatigue or credential theft attempt. I would advise password reset, session revocation, login review, source IP analysis, and conditional access checks.

---

### 26) An EDR alert says LSASS access attempt detected. Why serious?
**Answer:** Attackers access LSASS to dump credentials. I would inspect the process requesting access, privilege level, parent process, memory dump attempts, and other credential theft indicators.

---

### 27) Multiple endpoints show the same suspicious hash. What next?
**Answer:** Determine prevalence, first seen host, delivery vector, execution status, containment scope, and whether the hash is known malicious. Then isolate affected systems if needed.

---

### 28) A machine generated a lot of 4688 events for `net.exe user` and `whoami`. What does it suggest?
**Answer:** Likely discovery activity. I would see who ran the commands, whether it was an admin script or attacker recon, and check for subsequent lateral movement or privilege use.

---

### 29) A cloud login alert shows a legacy authentication attempt. Why care?
**Answer:** Legacy auth may bypass modern protections like MFA in some environments. I would verify whether it is allowed, identify source, and disable if unnecessary.

---

### 30) A host communicates with a known malicious IP, but the EDR shows no execution. What do you conclude?
**Answer:** I would not conclude too early. It may be blocked traffic, browsing artifact, or deeper compromise. I would review process source, DNS, proxy, firewall, and user behavior before closing.

---

### 31) You see excessive file rename activity followed by ransom note creation. What do you do?
**Answer:** Treat it as likely ransomware. Isolate host immediately, check spread to shares, identify encryption process, protect backups, and escalate fast.

---

### 32) An analyst says an alert is low severity because it is only one host. Do you agree?
**Answer:** Not always. One host can still be high impact if it is a domain controller, finance server, executive laptop, or privileged admin system.

---

### 33) A VIP user reports browser pop-ups and slowness. How would you investigate?
**Answer:** Review recent downloads, extensions, process tree, DNS and web traffic, and signs of adware, browser hijack, or malicious redirection. Prioritize because the user is high value.

---

### 34) A suspicious login came from an internal IP. Does that make it safe?
**Answer:** No. Internal IPs can still be compromised hosts, VPN exit points, jump boxes, or attacker footholds. I would validate source device ownership and behavior.

---

### 35) You find `rundll32.exe` launching from a user temp folder. Why suspicious?
**Answer:** Legitimate binaries running code from temp folders often indicate abuse. I would inspect command-line arguments, loaded DLL path, parent process, and persistence.

---

### 36) There was a malware alert but it was quarantined successfully. Is the case closed?
**Answer:** Not immediately. I would still confirm whether it executed, whether persistence was established, how it arrived, and if any other devices were exposed.

---

### 37) A user account disabled yesterday suddenly shows activity today. What do you check?
**Answer:** Validate timestamps, source logs, whether the account was re-enabled, cached credentials, sync delay, or suspicious admin actions involving the account.

---

### 38) You see repeated 3389 connections from one external IP to many assets. What is likely happening?
**Answer:** Likely RDP scanning or brute-force attempts. I would confirm exposure, target scope, failed vs successful auth, and recommend blocking or restricting access.

---

### 39) There is a high volume of 5156 allowed connection events. How would you make sense of it?
**Answer:** Filter by asset, time, destination, port, and process. Raw volume alone is not enough. I would look for anomalies, rare destinations, or suspicious parent applications.

---

### 40) You are given only an IP and told “investigate.” What is your process?
**Answer:** Determine internal vs external, asset owner, historical activity, associated users, DNS lookups, ports, processes, alerts, reputation, and timeline. Then decide whether it is benign, suspicious, or confirmed malicious.

---

### 41) You are given only a hash and told “investigate.” What do you do?
**Answer:** Check reputation, identify all hosts where seen, execution evidence, file paths, parent processes, signer, creation time, and related network activity. Then scope impact.

---

### 42) You are given only a username and told “investigate.” What is your approach?
**Answer:** Review authentication history, recent alerts, privilege changes, device access, VPN/cloud logins, mailbox activity if relevant, and any suspicious process execution tied to that account.

---

### 43) A Linux server shows repeated SSH failures then one success. What now?
**Answer:** Verify whether the success came from the same source, check geolocation, review command history, new users, cron jobs, auth logs, and outbound connections. Consider compromised credentials.

---

### 44) You suspect data exfiltration. What evidence supports that?
**Answer:** Large or unusual outbound transfer, rare destination, compression or staging files, access to sensitive shares before transfer, and activity outside normal user behavior.

---

### 45) An employee is leaving the company and suddenly accesses many files. Is it always malicious?
**Answer:** No, but it is worth reviewing. Context matters: role, notice period, file types, transfer method, and whether access exceeds normal patterns.

---

### 46) Your SIEM triggers on a known bad IP, but threat intel is old. What should you do?
**Answer:** Validate current reputation, context of connection, whether traffic was blocked, and whether the intel is still relevant before escalating hard.

---

### 47) You see a webshell alert on a server. What do you check first?
**Answer:** Web server logs, uploaded file path, parent process, child commands, external callback traffic, integrity of the web root, and whether the server is internet-facing.

---

### 48) What would make you escalate a “medium” alert quickly?
**Answer:** Sensitive asset, privileged account, multiple correlated signals, confirmed malware execution, suspicious persistence, or evidence of lateral movement.

---

### 49) How do you decide between false positive and true positive?
**Answer:** I compare the alert against context, logs, process behavior, user activity, asset role, historical baseline, and threat intel. I do not decide from one field alone.

---

### 50) In an interview, how should you answer scenario questions if you are not sure?
**Answer:** Stay calm and explain your investigation process. It is better to say “I would validate X, then correlate Y, then decide based on evidence” than to guess confidently without logic.

---

## Last-Minute Revision Sheet

### High-value Event IDs
- 4624 = successful logon
- 4625 = failed logon
- 4648 = explicit credentials used
- 4672 = special privileges assigned
- 4688 = process creation
- 4698 = scheduled task created
- 4719 = audit policy changed
- 4720 = user created
- 4723/4724 = password change/reset
- 4732 = member added to group
- 4740 = account lockout
- 4768 = Kerberos TGT request
- 4769 = Kerberos service ticket request
- 4771 = Kerberos pre-auth failed
- 4776 = NTLM credential validation
- 1102 = audit log cleared
- 7045 = service installed

### High-value Ports
- 21 = FTP
- 22 = SSH
- 23 = Telnet
- 25 = SMTP
- 53 = DNS
- 67/68 = DHCP
- 80 = HTTP
- 110 = POP3
- 123 = NTP
- 135 = RPC
- 137-139 = NetBIOS
- 143 = IMAP
- 161/162 = SNMP
- 389 = LDAP
- 443 = HTTPS
- 445 = SMB
- 3389 = RDP

### 10 Interview Lines That Sound Strong
- “I would validate the alert before deciding whether it is malicious.”
- “I would correlate logs from multiple data sources.”
- “I would check user, host, process, time, and source IP context.”
- “I would distinguish between suspicious and confirmed malicious activity.”
- “I would document evidence, decision, and escalation reason.”
- “I would look for false positives but not dismiss the alert too early.”
- “I would use process tree and command line to understand execution.”
- “I would scope whether the activity is isolated or widespread.”
- “I would consider asset criticality before assigning severity.”
- “I would explain my reasoning, not just the final answer.”

### Final Advice
Do not try to sound perfect. Sound clear.

In SOC interviews, interviewers often care more about your thought process than your memory.

If you know the basics, can explain logs clearly, and can walk through scenarios step by step, you already look much stronger than most freshers.
