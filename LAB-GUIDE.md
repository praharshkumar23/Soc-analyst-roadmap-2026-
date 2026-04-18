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

---

# 🔗 Integration Guide - SOC Labs, Learning Paths, and Practice Plan

[![Labs](https://img.shields.io/badge/Labs-20%2B-blue.svg)]()
[![Level](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-brightgreen.svg)]()
[![Style](https://img.shields.io/badge/Style-Fresher%20Friendly-orange.svg)]()
[![Cost](https://img.shields.io/badge/Cost-Mostly%20Free-success.svg)]()
[![Focus](https://img.shields.io/badge/Focus-SOC%20Practice-red.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

This guide is for the part where you stop reading and actually practice. It connects the roadmap with real labs, simple basics, and a proper order so you do not feel lost.

> **Use this guide as your practice map.**
> If the roadmap is the theory, this file is the hands-on part. It tells you which labs to do, in what order, and why each one matters.

**The goal is simple:** build skill step by step, not all at once.

---

## 📋 What This Guide Gives You

You already have the roadmap and project templates. This guide adds the missing practice side.

| Part | What It Helps With | Why It Matters |
|------|--------------------|----------------|
| Basics | Networking, Linux, Windows, security terms | Stops beginner confusion |
| Practice labs | Real SOC-style tasks | Builds hands-on skill |
| Learning order | What to do first, second, and third | Saves time |
| Tool practice | Wireshark, SIEM, CyberChef, logs | Helps in projects and interviews |
| Portfolio work | Notes, reports, screenshots, bullets | Makes your work usable in resume |

A lot of freshers jump straight into projects without this layer. That is where they get stuck. This file is meant to fix that.

---

## 🧱 Start With Basics

Before you do heavy labs, get these things clear in your head.

### Networking Basics
You do not need to become a network engineer. But you should know enough to read logs and understand traffic.

- IP address and subnet basics.
- Private vs public IP.
- Ports and protocols.
- DNS, HTTP, HTTPS, SMTP, SMB, RDP.
- TCP vs UDP.
- TCP three-way handshake.

### Linux Basics
You should be able to move around a terminal without panic.

- `ls`, `cd`, `pwd`, `mkdir`, `cp`, `mv`, `rm`.
- `cat`, `less`, `head`, `tail`.
- `grep`, `awk`, `sort`, `uniq`, `find`.
- Reading logs in `/var/log`.
- Basic process and service checks.

### Windows Basics
Most SOC alerts touch Windows in some way.

- Event Viewer.
- Event IDs like 4624, 4625, 4688, 4698, 7045, 1102.
- Task Manager, Resource Monitor, Process Explorer.
- Startup locations and common malware paths.
- PowerShell basics.

### SOC Thinking Basics
This is the part people skip, but it matters a lot.

- What is normal vs suspicious.
- What false positives look like.
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
4. Security concepts.
5. Blue-team tools.
6. Beginner labs.
7. SOC projects.

Do not jump around too much. It feels fast for one day, but it slows you down later.

---

## 🧪 Practice Platforms

### TryHackMe
Best for guided learning. Good if you want step-by-step rooms and a clear path.

Use it for:
- Network Fundamentals.
- Linux Fundamentals.
- Windows Fundamentals.
- SOC Level 1.
- Wireshark rooms.
- SIEM and incident response rooms.

Why it helps:
- It explains things simply.
- It gives structure.
- It is very beginner friendly.
- It lets you build confidence before tougher labs.

### CyberDefenders
Best for blue-team style investigations.

Use it for:
- Phishing analysis.
- PCAP analysis.
- Memory forensics.
- Log analysis.
- Malware-related investigations.

Why it helps:
- It feels closer to real SOC work.
- You practice thinking like an analyst.
- It improves your report writing.
- Good for evidence-based learning.

### LetsDefend
Best for alert triage practice.

Use it for:
- Monitoring alerts.
- Sorting false positives from real issues.
- Reading dashboards.
- Writing triage notes.
- Learning SOC workflow.

Why it helps:
- It trains you for real L1 work.
- You learn alert handling early.
- Good for resume bullets.
- Helps with daily SOC habits.

### Blue Team Labs Online
Best for scenario-based investigation practice.

Use it for:
- Incident-style labs.
- Defender workflows.
- Log and endpoint thinking.
- Realistic blue-team scenarios.

Why it helps:
- It feels close to actual SOC tasks.
- Good for trying new challenge types.
- Helps build confidence with unknown cases.

### OverTheWire Bandit
Best for Linux practice.

Use it for:
- Terminal comfort.
- Basic command line flow.
- Simple problem solving.
- Getting used to Linux paths and permissions.

### Security Blue Team Free Courses
Good for extra theory and beginner support.

Use it for:
- Introduction to Bash.
- Introduction to Python.
- Introduction to PowerShell.
- Introduction to Network Analysis.
- Introduction to Digital Forensics.
- Introduction to Threat Hunting.

---

## 🧭 Recommended Lab Path

### Phase 1: Comfort Stage
Do these first if you are new.

- TryHackMe Network Fundamentals.
- TryHackMe Linux Fundamentals.
- TryHackMe Windows Fundamentals.
- OverTheWire Bandit levels 0-10.
- Wireshark basics room.

**Goal:** understand the basics without feeling rushed.

### Phase 2: SOC Starter Stage
Move here after the basics feel okay.

- LetsDefend beginner alerts.
- TryHackMe SOC Level 1 modules.
- CyberDefenders phishing or log-based labs.
- Simple PCAP analysis.
- Basic triage notes.

**Goal:** learn how alert investigation actually feels.

### Phase 3: Analyst Stage
This is where you start thinking more like a SOC analyst.

- Multi-log investigation labs.
- Endpoint activity review.
- Timeline building.
- IOC extraction.
- Simple incident reports.

**Goal:** connect logs, tools, and events together.

### Phase 4: Project Stage
Now you use the skills in your roadmap projects.

- Project 1: LetsDefend monitoring.
- Project 2: Phishing analysis.
- Project 3: Incident response.
- Project 4: Ransomware forensics.
- Project 5: Threat hunting.
- Project 6: Detection engineering.

**Goal:** turn practice into portfolio work.

---

## 📅 4-Week Beginner Practice Plan

### Week 1
Focus only on comfort.

- Day 1: Set up accounts.
- Day 2: Networking basics.
- Day 3: Linux basics.
- Day 4: Windows basics.
- Day 5: Wireshark basics.
- Day 6: Write short notes.
- Day 7: Revise everything.

### Week 2
Move into guided labs.

- 2 TryHackMe rooms.
- 1 OverTheWire session.
- 1 Windows log practice session.
- 1 short CyberChef practice.
- 1 note-cleanup session.
- 1 rest/revision day.

### Week 3
Start SOC-style practice.

- 2 LetsDefend alerts.
- 1 CyberDefenders lab.
- 1 SIEM query practice session.
- 1 log review session.
- 1 report-writing session.
- 1 revision day.

### Week 4
Combine everything.

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

Practice these:
- Filter by IP.
- Filter by port.
- Find DNS queries.
- Follow TCP stream.
- Spot unusual traffic patterns.

### CyberChef
Use it for decoding and cleanup.

Practice these:
- Base64 decode.
- URL decode.
- Defang URLs.
- Extract strings.
- Clean messy log data.

### VirusTotal
Use it to check files, IPs, URLs, and hashes.

Practice these:
- Read detection summary.
- Check relations.
- Understand what a reputation result means.

### URLScan
Use it for suspicious URL analysis.

Practice these:
- Submit links safely.
- Read network and page behavior.
- Spot phishing clues.

### AbuseIPDB
Use it for IP reputation checks.

Practice these:
- See abuse reports.
- Understand if an IP is noisy or malicious.

### Process Explorer and Autoruns
Use them for Windows process and persistence checks.

Practice these:
- Find parent-child process chains.
- Check startup items.
- Look for strange paths or unsigned files.

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

- **One guided room** like TryHackMe.
- **One blue-team lab** like CyberDefenders.
- **One alert triage session** like LetsDefend.
- **One terminal practice session** like Bandit.
- **One tool session** like Wireshark or CyberChef.

That mix keeps things practical and avoids boredom.

---

## 🚫 Mistakes To Avoid

- Doing only theory and no labs.
- Doing only labs and no notes.
- Jumping to advanced stuff too early.
- Copying answers without understanding them.
- Skipping Windows and Linux basics.
- Ignoring report writing.
- Practicing too many platforms at the same time.

You do not need everything at once. You need steady progress.

---

## 💼 How This Helps Your Resume

Every good lab should give you something usable.

You can turn practice into:
- Resume bullets.
- Interview stories.
- GitHub notes.
- Portfolio write-ups.
- LinkedIn posts.

Example:
- Bad: "Completed a phishing lab."
- Better: "Analyzed a phishing email, extracted IOCs, and documented the attack path using a structured triage note."

Keep it real. Keep it simple.

---

## 🧠 Freshers Should Remember

- You do not need to know everything on day 1.
- The point is to get a little better every week.
- Basics matter more than fancy tools.
- Clean notes are a skill.
- Real understanding shows in interviews.
- Small lab progress is still progress.

If something feels too hard, break it into smaller parts.

---

## 🏁 First Step Today

1. Open TryHackMe.
2. Start a networking or Linux beginner room.
3. Create one `notes.md` file.
4. Keep one folder for screenshots.
5. Finish one small lab today.

That is enough to begin.

---

## 🔚 Final Thought

You do not need a perfect start. You just need a real one.

**Start with basics. Practice in labs. Write notes. Then move into projects.**

When you follow that order, the roadmap starts making sense.
