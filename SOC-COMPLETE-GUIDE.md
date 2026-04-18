# 🔗 SOC Analyst — Complete Integration Guide

[![Projects](https://img.shields.io/badge/Projects-6-blue.svg)]()
[![Labs](https://img.shields.io/badge/Labs-20%2B-brightgreen.svg)]()
[![Level](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-orange.svg)]()
[![Cost](https://img.shields.io/badge/Cost-0--30%2Fmonth-success.svg)]()
[![Focus](https://img.shields.io/badge/Focus-SOC%20Analyst-red.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

This is your one complete guide. It has the roadmap, the basics, the labs, the tools, and the practice plan — all in one place. No switching between files.

> **Read this first. Then start working.**
> It gives you structure, a clear learning order, and a simple way to build proof of work for interviews.

**The goal is simple:** go from beginner to job-ready, one step at a time.

---

## 📋 Table of Contents

1. [What You Have](#what-you-have)
2. [Choose Your Path](#choose-your-path)
3. [Start With Basics](#start-with-basics)
4. [Best Learning Order](#best-learning-order)
5. [Week 1 Action Plan](#week-1-action-plan)
6. [Practice Platforms](#practice-platforms)
7. [Recommended Lab Path](#recommended-lab-path)
8. [4-Week Beginner Plan](#4-week-beginner-plan)
9. [Core Tools To Practice](#core-tools-to-practice)
10. [What To Do In Each Lab](#what-to-do-in-each-lab)
11. [Simple Note Template](#simple-note-template)
12. [Good Beginner Lab Mix](#good-beginner-lab-mix)
13. [How To Use The Templates](#how-to-use-the-templates)
14. [Tracking Your Progress](#tracking-your-progress)
15. [Resume Preparation](#resume-preparation)
16. [Minimum Viable Portfolio](#minimum-viable-portfolio)
17. [Success Metrics](#success-metrics)
18. [Mistakes To Avoid](#mistakes-to-avoid)
19. [Getting Help](#getting-help)
20. [First Step Today](#first-step-today)

---

## 📦 What You Have

You have **6 complete project templates** covering the main parts of SOC analyst work.

| Project | Platform | Focus Area | Difficulty | Time |
|---------|----------|------------|------------|------|
| **Project 1** | LetsDefend | Alert Triage & Monitoring | Beginner | 2-3 weeks |
| **Project 2** | CyberDefenders | Phishing Analysis | Beginner-Int | 1-2 weeks |
| **Project 3** | TryHackMe | Incident Response (SIEM/EDR) | Intermediate | 2-3 weeks |
| **Project 4** | CyberDefenders | Ransomware Forensics | Int-Advanced | 2 weeks |
| **Project 5** | TryHackMe | Threat Hunting | Int-Advanced | 2-3 weeks |
| **Project 6** | Home Lab | Detection Engineering | Advanced | 2-3 weeks |

**Total Timeline:** 3-5 months at 10-15 hours per week.

Stay consistent and you move faster. Keep switching topics and everything slows down.

---

## 🎯 Choose Your Path

### Path A: "I need a job ASAP" — 8-10 weeks
**Goal:** Minimum viable portfolio for job applications.

Do these three projects:
1. ✅ Project 1: Live SOC Monitoring (LetsDefend) — 3 weeks
2. ✅ Project 2: Phishing Analysis (CyberDefenders) — 2 weeks
3. ✅ Project 3: Incident Response (TryHackMe) — 3 weeks

**What you get:**
- 9+ case studies and reports
- 300+ processed security alerts
- 3-5 resume bullets per project
- Interview talking points for core SOC topics
- A clean GitHub folder or markdown portfolio

**Roles you can apply for:** SOC Analyst Tier-1, Security Analyst (entry), MDR Analyst

---

### Path B: "I want to be a strong candidate" — 12-16 weeks
**Goal:** A better portfolio for competitive roles.

Do Projects 1-5.

**What you get:**
- 15+ detailed investigations
- Advanced SIEM queries
- Forensic analysis reports
- 10-12 resume bullets total
- Stronger interview answers

**Roles you can apply for:** SOC Analyst Tier-2, Incident Response Analyst, Detection Analyst

---

### Path C: "I want to be a detection engineer" — Full 20 weeks
**Goal:** Specialized detection engineering focus.

Do all 6 projects. Spend the most time on Project 6.

**What you get:**
- Complete SOC skillset
- GitHub detection repository
- Published rules and open-source contributions
- More confidence with logs, alerts, and tuning

**Roles you can apply for:** Detection Engineer, SIEM Engineer, Threat Detection Specialist

---

## 🧱 Start With Basics

Before you touch hard labs, make sure these basics feel familiar.

### Networking Basics
You do not need to become a network engineer. But you should understand enough to read traffic and logs.

- IP address basics.
- Private vs public IP.
- Ports and protocols.
- DNS, HTTP, HTTPS, SMTP, SMB, RDP.
- TCP vs UDP.
- TCP three-way handshake.

### Linux Basics
You should be able to move around a terminal without freezing.

- `ls`, `cd`, `pwd`, `mkdir`, `cp`, `mv`, `rm`.
- `cat`, `less`, `head`, `tail`.
- `grep`, `awk`, `sort`, `uniq`, `find`.
- Reading logs in `/var/log`.
- Basic process and service checks.

### Windows Basics
Most SOC work touches Windows in some way.

- Event Viewer.
- Event IDs like 4624, 4625, 4688, 4698, 7045, 1102.
- Task Manager, Resource Monitor, Process Explorer.
- Startup items and common malware paths.
- Basic PowerShell commands.

### SOC Thinking Basics
This is the part people skip, but it matters a lot.

- What normal looks like vs what suspicious looks like.
- False positive vs true positive.
- IOC vs TTP.
- SIEM vs EDR.
- Why logs matter more than guesses.
- How to write short investigation notes.

---

## 🎯 Best Learning Order

Use this order if you are starting from zero.

1. Networking basics.
2. Linux basics.
3. Windows basics.
4. SOC concepts.
5. Blue-team tools.
6. Beginner labs.
7. SOC projects.

Do not jump around too much. It feels fast for a day or two, but it slows you down later.

---

## 📅 Week 1 Action Plan

### Day 1: Platform Setup (2 hours)
- [ ] Create **LetsDefend** account: https://letsdefend.io
- [ ] Create **TryHackMe** account: https://tryhackme.com
- [ ] Create **CyberDefenders** account: https://cyberdefenders.org
- [ ] Create this folder structure:

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
- [ ] Read all of the "Step-by-Step Execution Plan"
- [ ] Complete LetsDefend onboarding tutorials
- [ ] Understand the alert dashboard interface
- [ ] Skim the basics section once so the terms feel familiar

### Day 4-7: First 10 Alerts (6-8 hours)
- [ ] Work through 10 alerts on LetsDefend
- [ ] Document each one in `triage-log.md`
- [ ] Take screenshots
- [ ] Write 1-2 lines after each alert — what made it look normal or suspicious

**By End of Week 1:** You should have triaged 10 alerts and started building real SOC skills.

---

## 🧪 Practice Platforms

### TryHackMe
Best for guided learning and step-by-step rooms.

Use it for: Network Fundamentals, Linux Fundamentals, Windows Fundamentals, SOC Level 1, Wireshark rooms, SIEM and incident response rooms.

Why it helps: It explains things clearly, it is beginner friendly, it gives structure, and it builds confidence before harder labs.

---

### CyberDefenders
Best for blue-team investigations.

Use it for: Phishing analysis, PCAP analysis, memory forensics, log analysis, malware-related investigations.

Why it helps: It feels close to real SOC work, you learn to think like an analyst, it helps with report writing, and it teaches evidence-based learning.

---

### LetsDefend
Best for alert triage practice.

Use it for: Monitoring alerts, sorting false positives, reading dashboards, writing triage notes, learning SOC workflow.

Why it helps: It trains you for real L1 work, you learn alert handling early, it gives you resume material, and it builds a daily SOC habit.

---

### Blue Team Labs Online
Best for scenario-based investigation practice.

Use it for: Incident-style labs, defender workflows, endpoint and log thinking, realistic blue-team scenarios.

Why it helps: It feels close to actual SOC tasks, gives you a different lab style, and builds confidence with unknown cases.

---

### OverTheWire Bandit
Best for Linux practice.

Use it for: Terminal comfort, command line flow, basic problem solving, paths and permissions.

---

### Security Blue Team Free Courses
Good for extra theory and beginner support.

Use it for: Bash, Python, PowerShell, Network Analysis, Digital Forensics, Threat Hunting intro.

---

## 🧭 Recommended Lab Path

### Phase 1: Comfort Stage
Do these first if you are new.

- TryHackMe Network Fundamentals.
- TryHackMe Linux Fundamentals.
- TryHackMe Windows Fundamentals.
- OverTheWire Bandit levels 0-10.
- Wireshark basics room.

**Goal:** understand basics without pressure.

---

### Phase 2: SOC Starter Stage
Move here after basics feel okay.

- LetsDefend beginner alerts.
- TryHackMe SOC Level 1 modules.
- CyberDefenders phishing or log-based labs.
- Simple PCAP analysis.
- Basic triage notes.

**Goal:** learn what alert investigation feels like.

---

### Phase 3: Analyst Stage
This is where you start thinking more like a SOC analyst.

- Multi-log investigation labs.
- Endpoint activity review.
- Timeline building.
- IOC extraction.
- Simple incident reports.

**Goal:** connect logs, tools, and events together.

---

### Phase 4: Project Stage
Now use the skills in your roadmap projects.

- Project 1: LetsDefend monitoring.
- Project 2: Phishing analysis.
- Project 3: Incident response.
- Project 4: Ransomware forensics.
- Project 5: Threat hunting.
- Project 6: Detection engineering.

**Goal:** turn practice into portfolio work.

---

## 📅 4-Week Beginner Plan

### Week 1 — Comfort Only
- Day 1: Set up accounts.
- Day 2: Networking basics.
- Day 3: Linux basics.
- Day 4: Windows basics.
- Day 5: Wireshark basics.
- Day 6: Write short notes.
- Day 7: Revise everything.

### Week 2 — Guided Labs
- 2 TryHackMe rooms.
- 1 OverTheWire session.
- 1 Windows log practice session.
- 1 CyberChef session.
- 1 note cleanup session.
- 1 rest day.

### Week 3 — SOC-Style Practice
- 2 LetsDefend alerts.
- 1 CyberDefenders lab.
- 1 SIEM query practice session.
- 1 log review session.
- 1 report-writing session.
- 1 revision day.

### Week 4 — Combine Everything
- 1 phishing lab.
- 1 PCAP or network lab.
- 1 endpoint or Windows lab.
- 1 alert triage session.
- 1 resume bullet draft.
- 1 portfolio note cleanup.
- 1 full review day.

---

## 🧰 Core Tools To Practice

### Wireshark
Use it for packet capture and traffic review.

Practice: Filter by IP, filter by port, find DNS queries, follow TCP stream, spot unusual traffic.

### CyberChef
Use it for decoding and cleanup.

Practice: Base64 decode, URL decode, defang URLs, extract strings, clean messy log data.

### VirusTotal
Use it to check files, IPs, URLs, and hashes.

Practice: Read detection summary, check relations, understand reputation results.

### URLScan
Use it for suspicious URLs.

Practice: Submit links safely, read page behavior, spot phishing clues.

### AbuseIPDB
Use it for IP reputation.

Practice: See abuse reports, understand if an IP is noisy or malicious.

### Process Explorer and Autoruns
Use them for Windows process and persistence checks.

Practice: Find parent-child process chains, check startup items, look for strange paths or unsigned files.

---

## 📚 What To Do In Each Lab

When you finish a lab, do not just move on.

Write down:
- What the lab was about.
- What tool you used.
- What clue mattered most.
- What the final answer was.
- What you learned.

If possible, save:
- One screenshot.
- One short summary.
- One resume-style bullet.
- One note about what confused you.

That is how practice becomes useful later.

---

## 📝 Simple Note Template

Use this for every room or lab.

```markdown
# Lab Name

## What I Did
-

## Tools Used
-

## Main Clues
-

## Final Finding
-

## What I Learned
-

## Resume Idea
-
```

Keep it short. You do not need a big report for every single lab.

---

## ✅ Good Beginner Lab Mix

A balanced week should have at least one from each group.

- One guided room like TryHackMe.
- One blue-team lab like CyberDefenders.
- One alert triage session like LetsDefend.
- One terminal practice session like Bandit.
- One tool session like Wireshark or CyberChef.

That mix keeps things practical and avoids boredom.

---

## 🎓 How To Use The Templates

Every project template includes:

- ✅ Step-by-Step Execution Plan (day-by-day breakdown)
- ✅ Evidence Capture Guidelines (what screenshots and artifacts to save)
- ✅ 3 Resume Bullet Versions (technical, results-oriented, skills-focused)
- ✅ Interview Talking Points (STAR method answers)
- ✅ Report and Documentation Templates (copy-paste and customize)
- ✅ Skills Developed Checklist (track your growth)
- ✅ Real-world context so you understand what the task means in SOC work

How to use them:
1. Read the FULL template before starting.
2. Follow the day-by-day plan so you do not get overwhelmed.
3. Document as you go.
4. Customize the templates — they are starting points, not final answers.
5. Capture evidence and keep it in one folder.
6. Write short notes in your own words after every alert or lab.
7. Redo tricky parts if something does not make sense the first time.

Slower and cleaner is better than rushing and forgetting everything.

---

## 📈 Tracking Your Progress

Create a simple tracker in a markdown file.

```markdown
# SOC Project Progress Tracker

## Project 1: Live SOC Monitoring
- [x] Week 1: Platform setup + first 20 alerts
- [ ] Week 2: Speed improvement + pattern recognition
- [ ] Week 3: Complex investigations + portfolio prep
- **Status:** In Progress
- **Evidence Collected:** 15 alert screenshots, triage log started
- **Next Milestone:** Complete 40 alerts total by end of Week 2

## Project 2: Phishing Analysis
- [ ] Not started yet
- **Planned Start Date:** After completing Project 1

[Repeat for all projects]
```

You do not need a fancy app. A plain markdown file is enough. Keep it simple and update it often.

---

## 💼 Resume Preparation

As you complete each project:

1. Copy 2-3 resume bullets from the template.
2. Customize with your own numbers:
   - Bad: "Monitored security alerts"
   - Good: "Monitored and triaged 150+ security alerts across LetsDefend, identifying brute force and phishing patterns"
3. Save everything in a `resume-bullets.md` file.
4. After 3 projects: update your actual resume and LinkedIn.

Do not wait until all 6 projects are done to start applying. After Projects 1-3, you are already in a much better place for entry-level SOC roles.

Write bullets that sound like you actually did the work. Keep numbers real. If a line feels too polished or fake, rewrite it.

---

## ✅ Minimum Viable Portfolio

To start applying for SOC Analyst Tier-1 roles, you need:

- ✅ 3-5 detailed case studies from Projects 1-3
- ✅ Updated resume with 6-9 SOC-focused bullets
- ✅ LinkedIn profile mentioning these projects
- ✅ Basic GitHub repo or Notion page (optional but recommended)
- ✅ A simple explanation of your process, not just the final result

You do NOT need:
- ❌ All 6 projects completed
- ❌ Certifications only
- ❌ Prior cybersecurity job experience
- ❌ A perfect portfolio before you start applying

---

## 🎯 Success Metrics

**After Project 1:**
- You can explain the SOC alert triage process in an interview ✅
- You recognize common attack patterns like brute force, phishing, and malware ✅
- You have documented 50+ alerts with analysis ✅
- You can talk about false positives without sounding lost ✅

**After Project 3:**
- You are comfortable writing SIEM queries in SPL or KQL ✅
- You can reconstruct attack timelines from logs ✅
- You understand the MITRE ATT&CK framework ✅
- You can explain what happened in a simple incident report ✅

**After Project 6:**
- You have published detection rules on GitHub ✅
- You can design a detection rule from scratch ✅
- You understand detection engineering principles ✅
- You can explain why a rule fired and how to tune it ✅

---

## 🚫 Mistakes To Avoid

1. ❌ Trying to do everything at once — focus on ONE project at a time.
2. ❌ Skipping documentation — future you will regret not taking notes.
3. ❌ Not redacting screenshots — never share real company data.
4. ❌ Perfectionism — done is better than perfect.
5. ❌ Waiting to feel ready — start now, learn as you go.
6. ❌ Copying template words blindly — add your own understanding.
7. ❌ Ignoring basics — if networking, Linux, and Windows are weak, projects feel much harder.
8. ❌ Doing only theory and no labs.
9. ❌ Doing only labs and no notes.
10. ❌ Practicing too many platforms at the same time.

---

## 🤝 Getting Help

When you are stuck:

1. Re-read the relevant template section — a lot of answers are already there.
2. Check platform communities: LetsDefend Discord, TryHackMe forums, CyberDefenders Discord.
3. Google the specific error or concept.
4. Use LinkedIn SOC analyst groups to see how other people talk about the same topics.
5. Take a break and come back — that helps more than staring at the screen.
6. Pick one learning platform at a time so you do not bounce around.

---

## 🏁 First Step Today

Right now, do this:

1. Open `templates/Project-1-Template.md`.
2. Read the "Project Overview" and "Learning Objectives".
3. Create your LetsDefend account.
4. Block out 10 hours this week for SOC project work.
5. Create one `notes.md` file.
6. Keep one folder for screenshots.
7. Start Day 1 tasks. Keep your first notes short and simple.

Do not wait for the perfect moment. Just begin.

---

## 🔚 Final Thought

You do not need a perfect start. You just need a real one.

**Start with basics. Practice in labs. Write notes. Then move into projects.**

When you follow that order, the roadmap starts making sense.

Every expert SOC analyst started exactly where you are now. The difference? They took the first step.

**Good luck, future SOC Analyst. 🔒**

> Small steps matter. Keep it steady.
