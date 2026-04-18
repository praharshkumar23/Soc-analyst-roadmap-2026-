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
