# 🔒 SOC Analyst Training Roadmap 2026

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Projects](https://img.shields.io/badge/Projects-10-blue.svg)](./templates/)
[![Content](https://img.shields.io/badge/Content-147K%20words-green.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()
[![SOC](https://img.shields.io/badge/Focus-SOC%20Analyst-red.svg)]()
[![Beginner](https://img.shields.io/badge/Level-Beginner%20Friendly-brightgreen.svg)]()
[![Automation](https://img.shields.io/badge/2026-Automation--First-orange.svg)]()

> **Complete, production-ready SOC analyst training program for freshers and beginners.** This roadmap starts from absolute zero — networking, Linux, Windows, cyber attacks — and builds you into a job-ready, automation-first SOC Analyst through hands-on projects, real tools, and portfolio-ready work.

**Transform from complete beginner to automation-first SOC analyst in 8–24 weeks.**

---

## 📋 Table of Contents

- [Overview](#overview)
- [Who This Is For](#who-this-is-for)
- [Before You Start — Beginner Basics You Must Know](#before-you-start--beginner-basics-you-must-know)
  - [1. Networking Fundamentals](#1-networking-fundamentals)
  - [2. Linux Basics](#2-linux-basics)
  - [3. Windows Basics](#3-windows-basics)
  - [4. Cyber Attacks 101](#4-cyber-attacks-101)
  - [5. Cybersecurity Core Concepts](#5-cybersecurity-core-concepts)
  - [6. Basic Analyst Tools](#6-basic-analyst-tools)
- [What You Get](#what-you-get)
- [Quick Start](#quick-start)
- [Learning Paths](#learning-paths)
- [Project Portfolio](#project-portfolio)
  - [Foundation Projects (1-6)](#foundation-projects-1-6)
  - [Automation Projects (7-8)](#automation-projects-7-8)
  - [Future-State Projects (9-10)](#future-state-projects-9-10)
- [Technology Stack](#technology-stack)
- [Career Outcomes](#career-outcomes)
- [Certifications](#certifications)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)
- [Common Beginner Mistakes](#common-beginner-mistakes)



---

## 🎯 Overview

### The SOC Landscape Has Changed

By 2026, **cybercrime is a $20 trillion economy**. The average data breach costs **$4.88 million**. Attack windows have collapsed from weeks to **hours**.

**Traditional SOC analysts are no longer enough. The future belongs to automation-first security professionals.**

But here is the thing most roadmaps miss — **you cannot automate what you don't understand manually first**. Before you touch SOAR or AI workflows, you need to understand networking, operating systems, how attacks work, and how analysts think. That foundation is what separates a professional SOC analyst from someone who just follows a checklist.

This program is built to give you both — **solid fundamentals first, then automation-first skills second**.

This program trains you for the **new reality:**
- ✅ Understanding how networks, systems, and attacks work before touching any tool
- ✅ Building real manual SOC skills through hands-on projects
- ✅ AI agents handling 90%+ of routine triage
- ✅ Human-agent teaming as a baseline expectation
- ✅ SOAR orchestration as a mandatory skill
- ✅ Cloud-native, identity-first security thinking
- ✅ Intelligence-driven security operations

---

## 👥 Who This Is For

This roadmap is made for:

- **Complete freshers** with zero prior cybersecurity experience
- **CS and IT graduates** who know theory but have no practical SOC exposure
- **Career switchers** from IT support, networking, or helpdesk roles
- **Self-learners** who have been jumping between random YouTube videos with no direction
- **Students** who want portfolio-ready projects before graduation
- **Anyone** who has heard terms like SIEM, EDR, or threat hunting but cannot explain them clearly

You do **not** need:
- Prior cybersecurity work experience
- Expensive tools or paid subscriptions
- Advanced programming knowledge
- Certifications to start

---

## 📚 Before You Start — Beginner Basics You Must Know

> **Do not skip this section.** Most freshers jump straight into SIEM tools and projects without understanding the foundations. That leads to confusion, surface-level knowledge, and weak interview answers. Spend 2–4 weeks on these basics before touching any project. It will make everything else 10x easier.

---

### 1. Networking Fundamentals

Networking is the backbone of SOC work. Every alert, every log, every attack involves network activity. If you don't understand how data moves across a network, you won't be able to investigate anything properly.

**What you must understand:**
IP Addressing

IPv4 and IPv6 address formats

Private vs public IP ranges

NAT — how private IPs reach the internet

What DNS does and how resolution works

Why DNS logs matter in SOC (C2 beaconing, data exfiltration)

Protocols

TCP vs UDP  ,TCP 3-way handshake — SYN, SYN-ACK, ACK , HTTP vs HTTPS — what traffic looks like

ICMP — ping, traceroute, and why attackers abuse it  

Common Ports to Memorize

OSI Model

Why analysts care: logs are tied to specific layers

text

**Free resources to use:**
- TryHackMe: "Network Fundamentals" path
- Professor Messer Network+ (first 10 free videos)
- NetworkChuck "Networking for Hackers" YouTube series
- Wireshark: install free, capture your own traffic and read it

**Checkpoint — you are ready when you can:**
- Explain TCP handshake without looking it up
- Identify what port 445 is and why it matters in SOC
- Read a basic Wireshark capture and spot anomalies

---

### 2. Linux Basics

text

**Free resources to use:**
- TryHackMe: "Linux Fundamentals Parts 1, 2, 3"
- OverTheWire Bandit (wargame — levels 1 to 15)
- Install Ubuntu or Kali on VirtualBox and practice daily

**Checkpoint — you are ready when you can:**
- Navigate a Linux system confidently in terminal
- Read auth.log and find failed SSH attempts
- Use grep to filter specific events from a log file

---

### 3. Windows Basics

Most enterprise environments run Windows. Windows endpoints generate the majority of SOC alerts. Windows Event Logs are the primary source of evidence in most investigations.

**What you must understand:**
Windows Event Logs
These Event IDs are asked in almost every SOC interview:


text

**Free resources to use:**
- TryHackMe: "Windows Fundamentals Parts 1, 2, 3"
- Blue Team Labs Online: Windows event log analysis labs
- Install Windows 10 VM and practice using Event Viewer daily

**Checkpoint — you are ready when you can:**
- Explain what Event ID 4625 means without looking it up
- Open Event Viewer and filter for failed logins
- Identify a suspicious process in Task Manager

---
### 4. Cyber Attacks 101

A SOC analyst's job is to detect and respond to attacks. If you don't know how attacks work, you won't know what to look for. You don't need to be an attacker, but you need to understand attacker thinking.

**What you must understand:**
Attack Lifecycle (Cyber Kill Chain)


Phishing

Fake emails with malicious links or attachments


text

**Free resources to use:**
- MITRE ATT&CK Navigator: attack.mitre.org
- TryHackMe: "Intro to Cyber Security" path
- TryHackMe: "Jr Penetration Tester" path (gives attacker perspective)
- Cyber Kill Chain article by Lockheed Martin

**Checkpoint — you are ready when you can:**
- Explain the Cyber Kill Chain 7 stages from memory
- Map a brute force attack to MITRE ATT&CK technique
- Describe what ransomware does at the system level

---

### 5. Cybersecurity Core Concepts

These are the foundational concepts every SOC analyst is expected to know. They appear in interviews constantly.

**What you must understand:**
CIA Triad


**Free resources to use:**
- TryHackMe: "SOC Level 1" path
- SANS Cyber Aces free course
- Professor Messer Security+ Domain 1 and 2

---

### 6. Basic Analyst Tools

Before starting the projects, get comfortable with these tools. You will use them in every single project.
Wireshark

Capture and analyze network traffic



**Checkpoint — you are ready when you can:**
- Search an IP on AbuseIPDB and explain what results mean
- Upload a file hash to VirusTotal and read the verdict
- Open Wireshark and filter by protocol or IP

---

> ✅ **Basics complete. Now move to the projects.**
> If you completed all 6 sections above, you have more foundational knowledge than 80% of freshers who apply for SOC roles. Now it is time to turn that knowledge into real project work.

---

## 🎁 What You Get

### 📚 **5 Core Documents** (147,000+ words)

| Document | Purpose | Read Time |
|----------|---------|-----------|
| [QUICK-START-GUIDE.md](QUICK-START-GUIDE.md) | Week 1 action plan, platform setup | 20 min |
| [SOC-Analyst-Roadmap.md](SOC-Analyst-Roadmap.md) | Foundation roadmap (Projects 1–6) | 10 min |
| [2026-Automation-First-Roadmap.md](2026-Automation-First-Roadmap.md) | Future-state vision (AI, SOAR, cloud) | 40 min |
| [INTEGRATION-GUIDE.md](INTEGRATION-GUIDE.md) | How everything fits together | 35 min |

### 🛠️ **10 Project Templates** (8 Complete, 2 Outlined)

**Foundation Projects:** Manual investigation skills
**Automation Projects:** SOAR orchestration, ML-powered threat intelligence
**Future-State Projects:** AI agents, post-quantum cryptography

Each template includes:
- ✅ Day-by-day execution plan
- ✅ Evidence capture guidelines
- ✅ 3 resume bullet versions (technical, results-oriented, strategic)
- ✅ STAR method interview answers
- ✅ Documentation templates
- ✅ Skills checklist

---

## 🚀 Quick Start

### **Get Started in 3 Steps (30 minutes)**

1. **Read the Quick Start Guide**
   ```bash
   # Open this file first
   cat QUICK-START-GUIDE.md
   ```

2. **Create Platform Accounts** (All Free)
   - [LetsDefend](https://letsdefend.io) — SOC monitoring and alert triage labs
   - [TryHackMe](https://tryhackme.com) — SIEM and incident response rooms
   - [CyberDefenders](https://cyberdefenders.org) — Blue team investigation challenges

3. **Start Project 1**
   ```bash
   # Open and follow step-by-step
   cat templates/Project-1-Template.md
   ```

**This Week:** Triage your first 20 security alerts 🎯

---

## 🛤️ Learning Paths

### **Path A: Fast Track** (10–12 weeks)
**Goal:** Entry-level SOC Analyst Tier-1 job

**Who this is for:** Freshers who need a job quickly and want the minimum viable portfolio to start applying.

**Study plan:**
- Week 1–3: Complete beginner basics (networking, Linux, Windows, attacks)
- Week 4–6: Project 1 — Live SOC Monitoring
- Week 7–8: Project 2 — Phishing Analysis
- Week 9–10: Project 3 — Incident Response (SIEM)
- Week 11–12: Project 7 — Automated Phishing Responder

**Projects:** 1, 2, 3, 7
**Outcome:** 9–12 resume bullets, 4 portfolio projects
**Start Applying:** Week 10

---

### **Path B: Complete Professional** (16–20 weeks)
**Goal:** Mid-level SOC Analyst or Detection Engineer

**Who this is for:** Learners who want a strong portfolio before applying and are targeting L2 or detection roles.

**Study plan:**
- Week 1–3: Complete all beginner basics
- Week 4–10: Projects 1, 2, 3 (foundation)
- Week 11–16: Projects 4, 5, 6 (forensics, hunting, detection)
- Week 17–20: Project 7 (SOAR automation)

**Projects:** 1–7 (all foundation plus SOAR)
**Outcome:** 15–18 resume bullets, 7 projects, GitHub detection repo
**Start Applying:** Week 16

---

### **Path C: Automation-First Leader** (20–24 weeks)
**Goal:** AI SOC Engineer or Tier 4 Orchestrator

**Who this is for:** Serious learners who want to be in the top 1% of candidates and target advanced blue team roles.

**Study plan:**
- Week 1–3: Complete all beginner basics
- Week 4–16: Projects 1–6 (full foundation)
- Week 17–20: Projects 7–8 (automation and ML TIP)
- Week 21–24: Projects 9–10 (AI hunting, PQC)

**Projects:** 1–10 (full suite)
**Outcome:** 20+ resume bullets, certifications, open-source contributions
**Start Applying:** Week 20+

---

## 📂 Project Portfolio

### Foundation Projects (1–6)

Build manual investigation skills before automating. Every automation skill in this roadmap depends on understanding these projects first.

| # | Project | Platform | Duration | Difficulty | Skills |
|---|---------|----------|----------|------------|--------|
| **1** | [Live SOC Monitoring](Project-1) | LetsDefend | 2–3 weeks | Beginner | Alert triage, log analysis, SOC workflow |
| **2** | [Phishing Email Analysis](Project-2) | CyberDefenders | 1–2 weeks | Beginner–Int | Email forensics, header analysis, IOC extraction |
| **3** | [Incident Response (SIEM)](Project-3) | TryHackMe | 2–3 weeks | Intermediate | Splunk/Elastic queries, MITRE ATT&CK mapping |
| **4** | [Ransomware Forensics](Project-4) | CyberDefenders | 2 weeks | Int–Advanced | Memory analysis, PCAP investigation, Volatility |
| **5** | [Threat Hunting](Project-5) | TryHackMe | 2–3 weeks | Int–Advanced | Hypothesis-driven hunting, IOC correlation |
| **6** | [Detection Engineering](Project-6d) | Home Lab | 2–3 weeks | Advanced | Sigma rule writing, GitHub publication |

**What each project builds:**
- **Project 1** teaches you how a real SOC queue works — you review alerts, check context, decide if it is a real threat or a false positive, and document your findings. This is the daily reality of an L1 analyst.
- **Project 2** gives you phishing investigation skills — reading email headers, checking SPF/DKIM/DMARC, extracting URLs and hashes, looking up IOCs.
- **Project 3** introduces SIEM investigation — writing queries, correlating log events, mapping attacker behavior to MITRE ATT&CK.
- **Project 4** goes deeper into forensics — analyzing memory dumps with Volatility, reading PCAP files, reconstructing what ransomware did on a system.
- **Project 5** shifts from reactive to proactive — you form a hypothesis and hunt for hidden attacker activity in logs that didn't trigger any alerts.
- **Project 6** closes the loop — you write your own detection rules in Sigma format, deploy them, and publish to GitHub.

---

### Automation Projects (7–8)

**2026 automation-first skills.** These projects build the workflow automation and machine learning capabilities that separate basic analysts from automation-first professionals.

| # | Project | Platform | Duration | Difficulty | Skills |
|---|---------|----------|----------|------------|--------|
| **7** | [Automated Phishing Responder](Project-7) ⭐ | Wazuh + Shuffle + TheHive | 2–3 weeks | Advanced | SOAR orchestration, playbook automation, API integration |
| **8** | [Automated Threat Intelligence Platform](Project-8) 🚀 | MISP + OpenCTI + Cortex + ML | 3–4 weeks | Enterprise | ML-based IOC filtering, STIX/TAXII, automated detections |

**Project 7 — Automated Phishing Responder:**
You build an end-to-end automated response workflow. When a phishing alert triggers, the system automatically extracts IOCs, checks them against threat feeds, creates a case in TheHive, sends notifications, and blocks the threat — all without manual analyst intervention. This is real SOAR work.

**Project 8 — Automated Threat Intelligence Platform:**
- ML model (89% accuracy) filters 10,000 IOCs down to 50 actionable ones
- Intelligence to detection time: **5 minutes** (vs 5 days manual)
- Automated Sigma rule generation and SIEM deployment
- 15+ threat intelligence sources integrated

---

### Future-State Projects (9–10)

Outlined in [2026-Automation-Roadmap.md](2026-Automation-First-Roadmap.md)

| # | Project | Focus | Status |
|---|---------|-------|--------|
| **9** | AI-Assisted Threat Hunting | Jupyter notebooks + AI agents for pattern detection | 🔄 Outlined |
| **10** | Post-Quantum Cryptography | PQC readiness assessment and crypto agility review | 🔄 Outlined |

---

## 🛠️ Technology Stack

### **Platforms (All Free and Open-Source)**

**Training Platforms:**
- LetsDefend — SOC simulation with real alert queues
- TryHackMe — SIEM labs, incident response, blue team rooms
- CyberDefenders — Realistic blue team CTF investigations

**SIEM and EDR:**
- Splunk Free (15 GB/day ingestion limit)
- Elastic Stack (open-source, no limit)
- Wazuh (open-source EDR and SIEM combined)

**SOAR and Case Management:**
- Shuffle (open-source SOAR platform)
- TheHive (case management and incident tracking)

**Threat Intelligence:**
- MISP (open-source threat intelligence platform)
- OpenCTI (knowledge graph for threat data)
- Cortex (automated IOC enrichment analyzers)

**Detection:**
- Sigma (universal rule format for all SIEMs)
- YARA (file and memory-based detection rules)

**AI and ML:**
- Python scikit-learn (for ML-based IOC filtering)
- Jupyter notebooks (for AI-assisted analysis)
- OpenAI or Claude APIs (optional, for AI workflow automation)

---

## 📈 Career Outcomes

### **Full Timeline from Beginner to Professional**

| Phase | Week | What You Do | Job Readiness |
|-------|------|-------------|---------------|
| **Basics** | 1–3 | Networking, Linux, Windows, attacks | Building foundation |
| **Foundation** | 4–10 | Projects 1–3 (triage, phishing, SIEM) | ✅ SOC Analyst Tier-1 ready |
| **Growth** | 11–16 | Projects 4–6 (forensics, hunting, detection) | ✅ Tier-2 / Detection Analyst |
| **Automation** | 17–20 | Projects 7–8 (SOAR, ML TIP) | ✅ Automation-first analyst |
| **Future** | 21–24 | Projects 9–10 + certifications | ✅ AI SOC Engineer |

### **Resume Impact**

**Before this program (generic fresher):**
Studied cybersecurity fundamentals

Completed online courses

Familiar with networking concepts

text

**After this program (project-ready candidate):**
Monitored and triaged 150+ security alerts with 92% TP/FP classification accuracy

Investigated phishing campaigns extracting 25+ IOCs and blocking malicious domains

Conducted ransomware forensic investigation using Volatility and Wireshark PCAP analysis

Wrote KQL and SPL queries correlating Event ID 4624/4625 login events in Sentinel/Splunk

Built SOAR pipeline in Shuffle reducing mean time to contain from 45 minutes to 3 minutes

Developed ML-powered TIP processing 12,500 IOCs/day with 89% accuracy using scikit-learn

text

### **Competitive Advantage**

| Candidate Type | What They Have |
|----------------|----------------|
| **Average fresher** | Certifications only, no projects |
| **Good fresher** | 2–3 basic TryHackMe projects |
| **Top 10% candidate** | SOAR automation project (Project 7) |
| **Top 1% candidate** | You — Enterprise TIP + ML + full portfolio 🏆 |

---

## 🎓 Certifications

> **Note:** Projects matter more than certifications in the 2024–2026 hiring market. Build the projects first, then certify.

### Recommended Certification Path

**Entry-Level (after Projects 1–3):**
- CompTIA Security+ — validates foundational knowledge
- Microsoft SC-900 — cloud security fundamentals

**Intermediate (after Projects 4–6):**
- GIAC Security Essentials (GSEC) — practical SOC skills
- Microsoft AZ-500 — Azure Security Engineer
- AWS Security Specialty — cloud security operations

**Advanced and 2026-Focused (after Projects 7–10):**
- SEC545: GenAI and LLM Security
- SEC598: AI SOC Orchestration
- Azure AI Engineer (AI-102)
- CompTIA CySA+ — cybersecurity analyst certification
- MICROSOFT - SC 200

---

## 🚀 Getting Started

### **Today (30 minutes)**

1. ⭐ Star this repository
2. 📖 Read [STARTING-GUIDE-FRESH.md](START-GUIDE-FRESH.md)
3. 📚 Start Section 1 of beginner basics — Networking Fundamentals
4. 🔐 Create accounts on LetsDefend, TryHackMe, and CyberDefenders

### **Week 1–3 (Beginner Basics)**

5. Work through all 6 beginner basics sections above
6. Complete TryHackMe: Network Fundamentals + Linux Fundamentals 1-2-3
7. Study Windows Event IDs and practice Event Viewer
8. Browse MITRE ATT&CK — read 5 technique pages

### **Week 4 (Start Projects)**

9. 📂 Open Prokect 1-8 
10. 🎯 Complete Day 1–7 tasks — triage your first 20 alerts
11. 📝 Start your triage log and document every alert

### **Week 8–10 (Apply)**

12. ✅ Complete Projects 1–3
13. 📄 Update resume with 6–9 SOC project bullets
14. 💼 Start applying for SOC Analyst Tier-1 jobs

---

## 📁 Repository Structure
soc-analyst-roadmap-2026/
├── README.md ← You are here
├──BEGINNER-BASICS.md 👈 Read after README
├── STARTING-GUIDE.md ← 👈 Read after Basics
├── SOC-Analyst-Roadmap.md ← Core 6 foundation projects
├── 2026-Automation-First-Roadmap.md ← Future skills (AI, SOAR, cloud)
├── INTEGRATION-GUIDE.md ← How all parts connect
├── templates/
│ ├── Project-1-Template.md (Live SOC Monitoring)
│ ├── Project-2-Template.md (Phishing Analysis)
│ ├── Project-3-Template.md (Incident Response)
│ ├── Project-4-Template.md (Ransomware Forensics)
│ ├── Project-5-Template.md (Threat Hunting)
│ ├── Project-6-Template.md (Detection Engineering)
│ ├── Project-7-Template.md (Automated Phishing Responder)
│ └── Project-8-Template.md (Automated TIP)
└── INTERVIEW Preparation 

text

---

## ⚠️ Common Beginner Mistakes

These mistakes are extremely common. Avoid them.

- **Skipping the basics section** — jumping to SIEM without knowing how TCP works leads to shallow knowledge that breaks under interview pressure
- **Doing projects without documenting** — if you don't write it down, it didn't happen in an interview
- **Copying project output without understanding it** — interviewers will ask follow-up questions
- **Trying to do everything at once** — focus on one project at a time and finish it properly
- **Waiting to feel "ready"** — you will never feel 100% ready. Start now, learn as you go
- **Only collecting certificates** — certifications without projects won't differentiate you
- **Not building a GitHub portfolio** — your GitHub is your proof of work

---

## 🤝 Contributing

This is a community training program. Contributions are welcome.

**Ways to contribute:**
- 🐛 Report unclear instructions or broken steps
- 💡 Suggest additional beginner resource links
- 📝 Share your project write-ups and success stories
- 🔗 Submit pull requests for content improvements

**Guidelines:**
- Follow the existing template structure
- Keep all content practical and actionable, not theoretical
- Test any technical steps before submitting
- Beginner-friendly language is preferred

---



**You are free to:**
- ✅ Use for personal learning
- ✅ Share with others
- ✅ Modify and adapt for your own roadmap
- ✅ Use project work in your portfolio

Attribution appreciated but not required.

---

## 🌟 Star History

If this roadmap helped you land a job or build your skills, consider giving it a ⭐. It helps other freshers find this resource.

---

## 📞 Connect

**Questions or feedback?**

- 💬 Open an issue in this repository
- 🐦 Share your progress: `#SOCRoadmap2026`
- 💼 Built by security learners, for aspiring SOC analysts

---

## 🎯 Final Thoughts

**What you have:**
- ✅ Complete beginner basics — networking, Linux, Windows, attacks
- ✅ Full training program 
- ✅ 10 project blueprints (8 detailed templates)
- ✅ Day-by-day execution plans
- ✅ Resume bullets and interview prep
- ✅ 2026 automation-first vision

**What you need:**
- ⏰ Consistency — 10 hours per week minimum
- 🚀 Execution — start, don't just read and bookmark
- ⏳ Patience — 8 to 24 weeks to job-ready depending on your path

**The SOC analyst career you want is 8 weeks away.**



---

<div align="center">

### **Stop reading. Start executing.**

**[👉 Begin with the Basics →](BEGINNER-BASICS.md)**

Made for aspiring SOC analysts

</div>
