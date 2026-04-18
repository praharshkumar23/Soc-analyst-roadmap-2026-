# 🚀 Quick Start Guide - SOC Analyst Projects

[![Projects](https://img.shields.io/badge/Projects-6-blue.svg)]()
[![Timeline](https://img.shields.io/badge/Timeline-3--5%20Months-orange.svg)]()
[![Level](https://img.shields.io/badge/Level-Beginner%20Friendly-brightgreen.svg)]()
[![Cost](https://img.shields.io/badge/Cost-0--30%2Fmonth-success.svg)]()
[![Focus](https://img.shields.io/badge/Focus-SOC%20Analyst-red.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

Welcome to your SOC analyst training roadmap. This guide is your starting point. It tells you what to do first, what to study, and how to stop wasting time on random videos and random notes.

> **Read this first. Then start working.**
> If you are a fresher, this is the cleanest way to begin. It gives you structure, basic direction, and a simple way to build proof of work that helps in interviews.

**Goal:** go from beginner to job-ready, one step at a time.

---

## 📋 What You Have

You now have **6 complete project templates** covering the main parts of SOC analyst work.

| Project | Platform | Focus Area | Difficulty | Time |
|---------|----------|------------|------------|------|
| **Project 1** | LetsDefend | Alert Triage & Monitoring | Beginner | 2-3 weeks |
| **Project 2** | CyberDefenders | Phishing Analysis | Beginner-Int | 1-2 weeks |
| **Project 3** | TryHackMe | Incident Response (SIEM/EDR) | Intermediate | 2-3 weeks |
| **Project 4** | CyberDefenders | Ransomware Forensics | Int-Advanced | 2 weeks |
| **Project 5** | TryHackMe | Threat Hunting | Int-Advanced | 2-3 weeks |
| **Project 6** | Home Lab | Detection Engineering | Advanced | 2-3 weeks |

**Total Timeline:** 3-5 months if you spend around 10-15 hours per week.

That timeline is flexible. If you stay consistent, you can move faster. If you keep switching between topics, everything slows down.

---

## 🎯 Choose Your Path

### Path A: "I need a job ASAP" (8-10 weeks)
**Goal:** Minimum viable portfolio for job applications.

**Do These Projects:**
1. ✅ Project 1: Live SOC Monitoring (LetsDefend) - 3 weeks
2. ✅ Project 2: Phishing Analysis (CyberDefenders) - 2 weeks
3. ✅ Project 3: Incident Response (TryHackMe) - 3 weeks

**Portfolio Output:**
- 9+ case studies/reports
- 300+ processed security alerts
- 3-5 resume bullets per project
- Interview talking points for core SOC topics
- A clean GitHub folder or markdown portfolio

**Job Application Readiness:** After Week 8
- **Roles:** SOC Analyst Tier-1, Security Analyst (entry), MDR Analyst
- **Advantage:** You’ll have more hands-on work than most freshers who only have certificates.

---

### Path B: "I want to be a strong candidate" (12-16 weeks)
**Goal:** A better portfolio for competitive roles.

**Do These Projects:**
- Projects 1-5

**Portfolio Output:**
- 15+ detailed investigations
- Advanced SIEM queries
- Forensic analysis reports
- 10-12 resume bullets total
- Better interview answers because you’ve seen more real scenarios

**Job Application Readiness:** After Week 16
- **Roles:** SOC Analyst Tier-2, Incident Response Analyst, Detection Analyst
- **Advantage:** You’ll sound more real in interviews because you’ve done the work.

---

### Path C: "I want to become a detection engineer" (Full 20 weeks)
**Goal:** Specialized detection engineering focus.

**Do ALL 6 Projects, emphasizing Project 6**

**Portfolio Output:**
- Complete SOC skillset
- GitHub detection repository
- Open-source contributions
- Published rules
- More confidence with logs, alerts, and tuning

**Job Application Readiness:** After Week 20
- **Roles:** Detection Engineer, SIEM Engineer, Threat Detection Specialist
- **Advantage:** Rare combination of operator + engineer skills.

---

## 📅 Week 1 Action Plan

### Day 1: Platform Setup (2 hours)
- [ ] Create **LetsDefend** account (free tier): https://letsdefend.io
- [ ] Create **TryHackMe** account (free): https://tryhackme.com
- [ ] Create **CyberDefenders** account (free): https://cyberdefenders.org
- [ ] Create a simple folder structure:

```text
soc-project/
├── projects/
│   ├── 01-Live-SOC-Monitoring/
│   ├── 02-Phishing-Analysis/
│   ├── 03-Incident-Response/
│   └── notes/
├── screenshots/
└── templates/
```

- [ ] Make a `triage-log.md` file before you start Project 1.
- [ ] Make one place for notes, screenshots, and reports so you do not lose things later.

### Day 2-3: Start Project 1 Prep (4 hours)
- [ ] Open `templates/Project-1-Template.md`
- [ ] Read **all** of "Step-by-Step Execution Plan"
- [ ] Complete LetsDefend onboarding tutorials
- [ ] Understand the alert dashboard interface
- [ ] Create your first `triage-log.md` file
- [ ] Skim the beginner basics file once so the terms feel familiar

### Day 4-7: First 10 Alerts (6-8 hours)
- [ ] Work through 10 alerts on LetsDefend
- [ ] Document each one in `triage-log.md` (use template from Project 1)
- [ ] Take screenshots (REDACTED)
- [ ] Reflect: What patterns are you seeing?
- [ ] Write 1-2 lines after each alert about what made it look normal or suspicious

**By End of Week 1:** You should have triaged 10 alerts and started building real SOC skills.

---

## 🛠️ Tools & Resources

### Free Platform Accounts (Required)
- **LetsDefend** (free tier gives around 20 alerts/month - enough for Project 1)
- **TryHackMe** (free tier works, but premium is useful for some rooms)
- **CyberDefenders** (completely free, unlimited challenges)

### Optional Tools That Help
- **GitHub Account** (free) - for publishing notes and detection rules
- **Splunk Free** - useful for home lab practice
- **Elastic Stack** - free open-source SIEM option
- **VirtualBox** or **VMware Player** - for running Linux and Windows VMs
- **Wireshark** - for packet analysis
- **CyberChef** - for decoding, cleaning, and transforming data

**Total Cost:** $0 - $30/month depending on whether you use TryHackMe premium.

---

## 📘 Extra Basics You Should Know

### Basic Learning Order
Start with the basics first. Do not jump straight into projects if these still feel weak.

1. Networking fundamentals.
2. Linux fundamentals.
3. Windows fundamentals.
4. Cyber attacks and SOC concepts.
5. Analyst tools like Wireshark, VirusTotal, CyberChef, AbuseIPDB, and URLScan.
6. Then start Project 1.

### Good Free Learning Platforms
- **TryHackMe:** great for guided beginner labs like Network Fundamentals, Linux Fundamentals, Windows Fundamentals, SOC Level 1, and Wireshark basics.
- **CyberDefenders:** strong for blue team labs, phishing, memory, PCAP, malware, and incident-style investigations.
- **LetsDefend:** good for alert triage practice and learning SOC workflow.
- **Blue Team Labs Online:** useful for investigations, challenge-style practice, and confidence building.
- **OverTheWire Bandit:** best for Linux command line practice.
- **Professor Messer:** simple theory for networking and security basics.

### How to Study Without Wasting Time
- Do not just watch videos. Do the lab or command right after the lesson.
- Keep one notebook or markdown file for each topic.
- Write notes in your own words, not copied lines.
- If a topic feels confusing, repeat it once before moving on.
- Save screenshots only for the things you actually understood.

### What to Practice Daily
- 15 minutes of networking revision.
- 15 minutes of Linux terminal practice.
- 15 minutes of Windows event log review.
- 15 minutes of one SOC-related lab or room.

---

## 📝 Templates Available in Each Project

Every project template includes:

✅ **Step-by-Step Execution Plan** (day-by-day breakdown)  
✅ **Evidence Capture Guidelines** (what screenshots/artifacts to save)  
✅ **3 Resume Bullet Versions** (technical, results-oriented, skills-focused)  
✅ **Interview Talking Points** (STAR method answers)  
✅ **Report/Documentation Templates** (copy-paste and customize)  
✅ **Skills Developed Checklist** (track your growth)  
✅ **Real-world context** so you understand what the task means in SOC work

---

## 🎓 How to Use the Templates

1. **Read the FULL template** before starting. Don’t skip around.
2. **Follow the day-by-day plan** because it stops you from getting overwhelmed.
3. **Document as you go** so you are not trying to remember everything later.
4. **Customize** the templates. They are starting points, not final answers.
5. **Capture evidence** and keep it organized in one folder.
6. **Write short notes in your own words** after every alert or lab.
7. **Redo tricky parts** if something does not make sense the first time.

A lot of freshers try to finish too fast. That usually leads to weak understanding. Slower and cleaner is better than rushing and forgetting everything.

---

## 📈 Tracking Your Progress

Create a simple tracker in a spreadsheet or markdown file.

```markdown
# SOC Project Progress Tracker

## Project 1: Live SOC Monitoring
- [x] Week 1: Platform setup + first 20 alerts
- [ ] Week 2: Speed improvement + pattern recognition (20 more alerts)
- [ ] Week 3: Complex investigations + portfolio prep
- **Status:** In Progress (Week 1, Day 5)
- **Evidence Collected:** 15 alert screenshots, triage log started
- **Next Milestone:** Complete 40 alerts total by end of Week 2

## Project 2: Phishing Analysis
- [ ] Not started yet
- **Planned Start Date:** [After completing Project 1]

[Repeat for all projects]
```

You do not need a fancy app for this. A plain markdown file is enough. Keep it simple and update it often.

---

## 💼 Resume Preparation

### As You Complete Each Project:

1. **Copy 2-3 resume bullets** from the template
2. **Customize with YOUR metrics:**
   - Bad: "Monitored security alerts"
   - Good: "Monitored and triaged 150+ security alerts..."
3. **Save** in a `resume-bullets.md` file
4. **After 3 projects:** Update your actual resume and LinkedIn

**Pro Tip:** Don't wait until you finish all 6 projects to start applying. After completing Projects 1-3, you're already in a much better place for entry-level SOC roles.

Also, write bullets that sound like you actually did the work. Keep numbers real. Keep the wording simple. If a line feels too polished or too fake, rewrite it.

---

## 🚨 Common Beginner Mistakes to Avoid

1. ❌ **Trying to do everything at once** → Focus on ONE project at a time
2. ❌ **Skipping documentation** → Future you will regret not taking notes
3. ❌ **Not redacting screenshots** → NEVER share real company data
4. ❌ **Perfectionism** → Done is better than perfect; iterate as you learn
5. ❌ **Waiting to feel "ready"** → Start now, learn as you go
6. ❌ **Copying template words blindly** → Add your own understanding and your own tone
7. ❌ **Ignoring basics** → If networking, Linux, and Windows are weak, projects feel much harder

---

## 🤝 Getting Help

### When You're Stuck:

1. **Re-read the relevant template section** because a lot of answers are already there.
2. **Check platform communities:**
   - LetsDefend Discord
   - TryHackMe forums
   - CyberDefenders Discord
3. **Google the specific error or concept** (for example, "What is SPF in email headers?")
4. **Use LinkedIn SOC analyst groups** to see how other people talk about the same topics.
5. **Take a break and come back later** if your brain is fried. That helps more than staring at the screen.
6. **Pick one learning platform at a time** so you do not bounce around too much.

---

## ✅ Minimum Viable Portfolio (MVP)

**To start applying for SOC Analyst Tier-1 roles, you need:**

- ✅ 3-5 detailed case studies (from Projects 1-3)
- ✅ Updated resume with 6-9 SOC-focused bullets
- ✅ LinkedIn profile mentioning these projects
- ✅ Basic GitHub repo or Notion page showcasing work (optional but recommended)
- ✅ A simple explanation of your process, not just the final result

**You do NOT need:**
- ❌ All 6 projects completed
- ❌ Certifications only — helpful, but not enough on their own
- ❌ Prior cybersecurity job experience
- ❌ A perfect portfolio before you start applying

---

## 🎯 Success Metrics

### How to Know You're Making Progress:

**After Project 1:**
- You can explain the SOC alert triage process in an interview ✅
- You recognize common attack patterns (brute force, phishing, malware) ✅
- You've documented 50+ alerts with analysis ✅
- You can talk about false positives without sounding lost ✅

**After Project 3:**
- You're comfortable writing SIEM queries (SPL or KQL) ✅
- You can reconstruct attack timelines from logs ✅
- You understand the MITRE ATT&CK framework ✅
- You can explain what happened in a simple incident report ✅

**After Project 6:**
- You've published detection rules on GitHub ✅
- You can design a detection rule from scratch ✅
- You understand detection engineering principles ✅
- You can explain why a rule fired and how to tune it ✅

---

## 🏁 Your First Step

**Right now, do this:**

1. Open `templates/Project-1-Template.md`
2. Read the "Project Overview" and "Learning Objectives"
3. Create LetsDefend account
4. Block out 10 hours THIS WEEK on your calendar for SOC project work
5. Start Day 1 tasks
6. Keep your first notes short and simple
7. Do not wait for the perfect moment — just begin

**Remember:** Every expert SOC analyst started exactly where you are now. The difference between them and someone who never makes it? They took the first step.

---

## 📞 Need Clarification?

If you have questions about:
- Which project to start with → Start with Project 1 (LetsDefend)
- How much time to invest → Minimum 8-10 hours/week for meaningful progress
- When to start applying → After completing Projects 1-3 (Week 8-10)
- Which platform to prioritize → LetsDefend first (easiest onboarding)
- How to write notes → Keep them short, clear, and in your own words
- What to save → Screenshots, logs, queries, and final write-ups

---

**You've got comprehensive templates, a clear roadmap, and everything you need to succeed.**

**The only question left is: When do you start?**

**Recommendation: TODAY. Open Project 1. Create your LetsDefend account. Start alert #1.**

**Good luck, future SOC Analyst! 🔒🎯**

> Small steps matter. Keep it steady.
