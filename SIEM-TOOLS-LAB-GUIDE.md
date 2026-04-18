# 🖥️ SIEM Tools Lab Guide for Freshers

[![Tools](https://img.shields.io/badge/Tools-Splunk%20%7C%20Sentinel%20%7C%20Wazuh%20%7C%20ELK-blue.svg)]()
[![Level](https://img.shields.io/badge/Level-Fresher%20Friendly-brightgreen.svg)]()
[![Cost](https://img.shields.io/badge/Cost-Mostly%20Free-success.svg)]()
[![Focus](https://img.shields.io/badge/Focus-Hands--On%20Labs-orange.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

This file is for freshers who want to practice with real SIEM tools. No corporate license needed. Everything here is free or has a free tier.

> **The goal is simple:** learn how SIEM tools work by actually using them — not just watching videos about them.

---

## 📋 Table of Contents

1. [What is a SIEM](#what-is-a-siem)
2. [Why SIEM Practice Matters for Freshers](#why-siem-practice-matters-for-freshers)
3. [SIEM Tools Overview](#siem-tools-overview)
4. [Tool 1 — Splunk](#tool-1--splunk)
5. [Tool 2 — Microsoft Sentinel](#tool-2--microsoft-sentinel)
6. [Tool 3 — Wazuh](#tool-3--wazuh)
7. [Tool 4 — ELK Stack](#tool-4--elk-stack)
8. [Lab Setup Requirements](#lab-setup-requirements)
9. [Lab 1 — Splunk Log Search and Alerts](#lab-1--splunk-log-search-and-alerts)
10. [Lab 2 — Microsoft Sentinel KQL Queries](#lab-2--microsoft-sentinel-kql-queries)
11. [Lab 3 — Wazuh Agent and Alert Detection](#lab-3--wazuh-agent-and-alert-detection)
12. [Lab 4 — ELK Stack Log Ingestion and Kibana](#lab-4--elk-stack-log-ingestion-and-kibana)
13. [Common SIEM Queries Cheatsheet](#common-siem-queries-cheatsheet)
14. [How to Turn Labs Into Resume Bullets](#how-to-turn-labs-into-resume-bullets)
15. [Mistakes to Avoid](#mistakes-to-avoid)
16. [First Step Today](#first-step-today)

---

## 🔍 What is a SIEM

SIEM stands for Security Information and Event Management.

It does two things:
- **Security Information:** collects, stores, and normalizes logs from many sources.
- **Event Management:** detects suspicious patterns, triggers alerts, and helps investigate incidents.

In a SOC, analysts use SIEM to:
- Search logs.
- Build detection rules.
- Investigate alerts.
- Create dashboards.
- Track incident timelines.

**Sources it collects from:** Windows event logs, Linux syslogs, firewall logs, proxy logs, EDR telemetry, Active Directory, cloud logs, and more.

---

## 🎯 Why SIEM Practice Matters for Freshers

Most job descriptions say "Splunk" or "Sentinel" or "SIEM experience preferred."

Without hands-on practice, you can only say "I know what SIEM is." With lab practice, you can say "I deployed Splunk, wrote SPL queries, and built detection alerts for brute force and phishing activity."

That difference is real in interviews.

---

## 🧰 SIEM Tools Overview

| Tool | Cost | Best For | Query Language |
|------|------|----------|----------------|
| Splunk | Free up to 500MB/day | Log search, alerts, dashboards | SPL |
| Microsoft Sentinel | Free trial on Azure | Cloud SIEM, KQL practice, Azure integration | KQL |
| Wazuh | Completely free | Agent-based detection, home lab | Custom rules, Kibana |
| ELK Stack | Completely free | Log ingestion, visualization | Lucene / KQL (Kibana) |
| Security Onion | Completely free | Network + host monitoring, threat hunting | Multiple |
| LetsDefend SIEM | Free tier | Beginner alert triage practice | Platform-based |

---

## 🔴 Tool 1 — Splunk

### What it is
Splunk is one of the most widely used SIEM platforms in enterprise SOCs. It collects logs, lets you search with SPL, build alerts, and create dashboards.

### Free Access
- **Splunk Enterprise Free Trial:** 60-day trial or free developer license.
- **Splunk BOTS (Boss of the SOC):** free CTF-style dataset for investigation practice.
- **TryHackMe Splunk rooms:** free guided labs.

### What to Practice
- Log in to Splunk.
- Understand the search bar and time range selector.
- Run basic SPL queries.
- Build a simple alert.
- Create one dashboard panel.

### Basic SPL Queries to Know

```spl
-- Search all events
index=*

-- Filter by sourcetype
index=main sourcetype="WinEventLog:Security"

-- Search for failed logins (Event ID 4625)
index=* EventCode=4625

-- Count events by user
index=* EventCode=4625 | stats count by user

-- Search for specific IP
index=* src_ip="192.168.1.100"

-- Top 10 source IPs
index=* | top limit=10 src_ip

-- Search for PowerShell execution
index=* process_name="powershell.exe"

-- Timechart of failed logins
index=* EventCode=4625 | timechart count by user

-- Search for brute force (more than 10 failures)
index=* EventCode=4625 | stats count by src_ip | where count > 10

-- Table output
index=* EventCode=4688 | table _time, user, process_name, parent_process
```

### Key SPL Commands
- `stats count by field` — aggregate counts
- `table field1 field2` — display specific fields
- `timechart` — trend over time
- `where count > X` — filter by threshold
- `dedup field` — remove duplicates
- `sort -count` — sort descending
- `eval newfield=expression` — create calculated field
- `rex` — extract fields with regex
- `lookup` — enrich data with reference tables

---

## 🔵 Tool 2 — Microsoft Sentinel

### What it is
Microsoft Sentinel is a cloud-native SIEM and SOAR on Azure. It uses KQL (Kusto Query Language) for searching, detection, and analytics.

### Free Access
- **Azure Free Account:** $200 credit, enough for 30 days of Sentinel lab.
- **Microsoft Learn:** free guided Sentinel modules.
- **SC-200 study path:** full free learning path on Microsoft Learn.

### What to Practice
- Create a Sentinel workspace.
- Connect a Windows VM as a log source.
- Run KQL queries in Log Analytics.
- Build one scheduled analytics rule.
- Explore the Incidents tab.

### Basic KQL Queries to Know

```kql
// All security events
SecurityEvent
| take 100

// Failed logons (Event ID 4625)
SecurityEvent
| where EventID == 4625
| project TimeGenerated, Account, Computer, IpAddress

// Count failed logons by account
SecurityEvent
| where EventID == 4625
| summarize FailCount = count() by Account
| sort by FailCount desc

// Successful logons
SecurityEvent
| where EventID == 4624
| project TimeGenerated, Account, Computer, LogonType

// Process creation
SecurityEvent
| where EventID == 4688
| project TimeGenerated, Account, NewProcessName, ParentProcessName, CommandLine

// PowerShell execution
SecurityEvent
| where EventID == 4688
| where NewProcessName contains "powershell"
| project TimeGenerated, Account, CommandLine

// Brute force detection (10+ failures in 10 min)
SecurityEvent
| where EventID == 4625
| summarize FailCount = count() by Account, bin(TimeGenerated, 10m)
| where FailCount > 10

// Scheduled task created
SecurityEvent
| where EventID == 4698
| project TimeGenerated, Account, Computer, TaskName

// Account created
SecurityEvent
| where EventID == 4720
| project TimeGenerated, Account, SubjectUserName, Computer

// Group membership change
SecurityEvent
| where EventID == 4732
| project TimeGenerated, Account, MemberName, GroupName
```

### Key KQL Operators
- `where` — filter rows
- `project` — select columns
- `summarize` — aggregate
- `sort by` — order results
- `extend` — add computed column
- `join` — combine tables
- `bin()` — bucket by time
- `contains` — substring match
- `has` — token match
- `between` — date/number range

---

## 🟢 Tool 3 — Wazuh

### What it is
Wazuh is a free open-source SIEM and XDR platform. It collects logs from agents on endpoints, detects threats, monitors file integrity, and triggers alerts.

### Free Access
- Completely free. No trial limit.
- Install on Ubuntu VM.

### What to Practice
- Deploy Wazuh manager on Ubuntu.
- Install Wazuh agent on Windows VM.
- Simulate failed logins and watch alerts.
- Explore file integrity monitoring.
- Review active response rules.

### Basic Setup Steps
1. Install Wazuh on Ubuntu (official installation script from wazuh.com).
2. Access the Wazuh dashboard via browser.
3. Install Wazuh agent on a Windows VM.
4. Enroll the agent to the manager.
5. Generate test activity on the Windows host.
6. Watch alerts appear in the dashboard.

### Things to Test
- Multiple failed RDP or local logon attempts.
- Create and delete a user account.
- Add a scheduled task.
- Modify a critical file.
- Run `whoami` or `net user` from CMD.

### What Wazuh Covers
- Log analysis from endpoints.
- Integrity monitoring.
- Vulnerability detection.
- Active response actions.
- MITRE ATT&CK mapping in dashboard.

---

## 🟡 Tool 4 — ELK Stack

### What it is
ELK Stack is Elasticsearch + Logstash + Kibana. It is an open-source log platform used for collecting, parsing, and visualizing data. Beats agents send logs to Logstash.

### Free Access
- Completely free. Self-hosted.
- Works on Ubuntu VM or Docker.

### What to Practice
- Set up Elasticsearch and Kibana.
- Use Filebeat to ship Windows or Linux logs.
- Create an index pattern.
- Build a Kibana dashboard.
- Run basic searches and filters.

### Basic Setup Order
1. Install Elasticsearch.
2. Install Kibana.
3. Install Filebeat on the host you want to monitor.
4. Configure Filebeat to send logs to Elasticsearch.
5. Create index pattern in Kibana.
6. Start searching and building visualizations.

### Kibana Search Examples
```
# Filter by event ID
event.code: 4625

# Filter by source IP
source.ip: 192.168.1.100

# Filter by process name
process.name: powershell.exe

# Filter by username
user.name: administrator

# Date range filter
@timestamp >= "2024-01-01" and @timestamp <= "2024-12-31"
```

### What ELK Helps You Practice
- Log ingestion and normalization.
- Index management.
- Building visualizations.
- Running manual threat hunts.
- Understanding dashboards.

---

## 💻 Lab Setup Requirements

### Minimum Hardware
- 8 GB RAM recommended (16 GB for multi-tool lab).
- 100 GB free disk space.
- A laptop or desktop.

### Virtualization Options
- **VirtualBox** — free, good for beginners.
- **VMware Workstation Player** — free for personal use.

### Recommended VM Setup

| VM | OS | Role |
|----|-----|------|
| VM 1 | Ubuntu 22.04 | SIEM server (Wazuh or ELK) |
| VM 2 | Windows 10 | Log source / agent |
| VM 3 | Kali Linux (optional) | Attack simulation |

### Free Downloads
- Ubuntu Server: ubuntu.com
- Windows 10 evaluation: microsoft.com/en-us/evalcenter
- Kali Linux: kali.org
- VirtualBox: virtualbox.org

---

## 🧪 Lab 1 — Splunk Log Search and Alerts

**Objective:** Search logs, find suspicious activity, and create a basic alert.

### Steps
1. Download and install Splunk Enterprise (free trial).
2. Upload a sample Windows event log or use BOTS dataset.
3. Search for Event ID 4625 using SPL.
4. Count failures by user and IP.
5. Build a saved search for brute force (more than 10 failures in 10 minutes).
6. Create an alert that triggers when threshold is exceeded.
7. Screenshot the alert and document findings.

### What to Document
- Query used.
- What you found.
- How the alert was built.
- What a real analyst would do next.

### Resume Bullet Idea
`Built Splunk alert to detect brute-force attacks using SPL, filtering Event ID 4625 with threshold-based logic across Windows event logs.`

---

## 🧪 Lab 2 — Microsoft Sentinel KQL Queries

**Objective:** Write KQL queries to detect suspicious activity and build a detection rule.

### Steps
1. Create a free Azure account.
2. Deploy Microsoft Sentinel workspace.
3. Connect a Windows VM or use demo data.
4. Run queries for Event ID 4625, 4688, 4698.
5. Build a scheduled analytics rule for brute force or PowerShell execution.
6. Trigger the rule and review the incident in Sentinel.
7. Document your query and incident summary.

### What to Document
- KQL query used.
- Alert logic.
- Incident details.
- What you escalated or closed.

### Resume Bullet Idea
`Developed Microsoft Sentinel analytics rule using KQL to detect PowerShell-based execution and brute-force patterns from Windows Security Event logs.`

---

## 🧪 Lab 3 — Wazuh Agent and Alert Detection

**Objective:** Deploy Wazuh, connect an agent, simulate attacks, and review alerts.

### Steps
1. Install Wazuh on Ubuntu VM using official script from wazuh.com.
2. Access Wazuh dashboard.
3. Install Windows agent on VM 2.
4. Simulate 10 failed logons on Windows VM.
5. Check Wazuh dashboard for 4625 alerts.
6. Run `net user hacker /add` on Windows VM.
7. See account creation alert in Wazuh.
8. Enable file integrity monitoring on a test folder.
9. Modify a file and see FIM alert trigger.
10. Document all alerts.

### What to Document
- Alerts generated.
- Rule IDs triggered.
- MITRE ATT&CK mapping.
- Simulated attack description.

### Resume Bullet Idea
`Deployed Wazuh SIEM on Ubuntu, onboarded Windows endpoint, and validated detection coverage for brute force, account creation, and file integrity tampering events.`

---

## 🧪 Lab 4 — ELK Stack Log Ingestion and Kibana

**Objective:** Set up ELK, ingest logs, and build a basic dashboard.

### Steps
1. Install Elasticsearch and Kibana on Ubuntu VM.
2. Install Filebeat on Windows VM.
3. Configure Filebeat to ship Windows Security logs.
4. Create index pattern in Kibana.
5. Search for failed logons using Kibana filter.
6. Build a simple bar chart of failed logins by user.
7. Add a count metric to the dashboard.
8. Screenshot and document.

### What to Document
- How logs were ingested.
- Index name and fields used.
- Dashboard panels built.
- What you learned.

### Resume Bullet Idea
`Built ELK Stack lab environment to ingest Windows event logs via Filebeat, created Kibana dashboards to visualize authentication failures and process creation events.`

---

## 📋 Common SIEM Queries Cheatsheet

### SPL (Splunk)
```spl
-- Failed logins
index=* EventCode=4625 | stats count by user, src_ip

-- Process creation
index=* EventCode=4688 | table _time, user, process_name, CommandLine

-- Scheduled task
index=* EventCode=4698 | table _time, user, TaskName

-- Log cleared
index=* EventCode=1102

-- Top talkers by IP
index=* | top limit=10 src_ip
```

### KQL (Sentinel)
```kql
// Failed logins
SecurityEvent | where EventID == 4625
| summarize count() by Account, IpAddress

// Process creation with PowerShell
SecurityEvent | where EventID == 4688
| where NewProcessName contains "powershell"

// New user created
SecurityEvent | where EventID == 4720

// Log cleared
SecurityEvent | where EventID == 1102

// Lateral movement via SMB
NetworkConnection | where DestinationPort == 445
| summarize count() by SourceAddress
```

### Wazuh / Kibana
```
event.code: 4625
event.code: 4688 AND process.name: powershell.exe
winlog.event_id: 1102
agent.name: DESKTOP-WIN10
rule.mitre.technique: T1078
```

---

## 💼 How to Turn Labs Into Resume Bullets

Bad: `Learned Splunk.`

Better: `Deployed Splunk Enterprise, ingested Windows event logs, and built SPL-based detection rules for brute force and suspicious process execution.`

For each lab you complete, write:
- Tool used.
- What you set up.
- What you detected.
- How many events or rules created (if possible).

Keep numbers real. If you made 3 detection rules, say 3. Not "multiple."

---

## 🚫 Mistakes to Avoid

- Setting up the tool but never actually querying it.
- Only watching install videos without doing the lab yourself.
- Skipping documentation — the lab only helps your resume if you write it down.
- Trying all four tools at once. Pick one, get comfortable, then move to the next.
- Ignoring error messages — they teach you more than successful installs.
- Not saving your queries somewhere — you will forget them.

---

## 🏁 First Step Today

Pick one tool. Start with **Wazuh** if you want fully free and offline. Start with **Splunk** if you want the most job-relevant name on your resume. Start with **Sentinel** if you want cloud SIEM and KQL practice.

Then:
1. Install or access the tool today.
2. Run one query.
3. Write one note.
4. Come back tomorrow and run five more queries.

That is it. One lab at a time.

---

> Small labs done properly beat big labs forgotten quickly.
> Keep it steady. Keep it real.
