# CySA+ Simulation Lab

A tile-based dashboard for original, performance-based practice simulations (PBQs) covering
CompTIA CySA+ (CS0-003) scenarios: incident and log analysis, kill chain identification,
vulnerability triage, configuration verification, and multi-phase SOC analyst workflows.

**Educational use only.** This is a self-study practice tool built from original simulation
exercises. It is not affiliated with, endorsed by, or sponsored by CompTIA®. CompTIA and
CySA+ are trademarks of CompTIA, Inc. Always confirm current exam content on comptia.org.

## What's here

Open `index.html` to see the dashboard. Each tile launches one interactive simulation:

| Simulation | What it covers |
|---|---|
| Malicious Behavior Analysis | Analyze suspicious system activity |
| Kill Chain Stages Exercise | Map evidence to kill chain stages |
| Vulnerability Remediation Simulation | Prioritize and remediate vulnerabilities |
| Cybersecurity Configuration Verification Lab | Verify and recommend secure configs |
| Nmap Server Role & Security Analysis | Interpret Nmap scan output |
| IT Help Desk Simulation | Resolve a reported security issue |
| Security Logs Analysis Lab | Investigate a suspicious login |
| Web Server Vulnerability Assessment | Assess and respond to web server findings |
| Security Incident Analysis Quiz | Connect evidence across a full incident |
| Phishing Attack Simulation | Review logs for a phishing attack |
| Analyst Workbench: OWASP Top 10 & CVSS Triage | Classify findings and score with CVSS |
| SecOps Horizon: Tier 1 SOC Induction Portal | Multi-phase SOC analyst onboarding sim |
| IOC Triage: Analyst Decision Lab | Triage and classify 7 artifacts under time pressure |
| Security Incident Ticket Analysis | Classify and resolve four analyst tickets |
| Attack Lifecycle Identification (Kill Chain) | SOC analyst kill-chain identification sim |
| Endpoint Behavioral Analysis: Process & Persistence | Investigate suspicious endpoint processes |
| Incident Kill Chain Analysis | Full SOC analyst kill chain investigation |
| Log Correlation: Phishing to C2 | Correlate logs from phish to beaconing |
| Web Exploitation & Data Exposure | Directory traversal & data exposure investigation |

Several simulations include a PDF or JPG answer key (kept alongside the simulation's HTML
file) for instructor review.

## Duplicates removed

Three simulations existed as two identical copies each (once at the repo root, once inside a
matching subfolder that also holds a companion "Student Guide" PDF). The root-level copies
were removed, since they were byte-for-byte identical to the subfolder versions — no content
was lost:

- `SOC Analyst Correlation Lab - Phishing to C2.html`
- `SOC Analyst Simulation - Incident Kill Chain Analysis.html`
- `SOC Analyst Simulation – Attack Lifecycle Identification (Cyber Kill Chain).html`

("9. Security Incident.html" and "Security Incident Ticket Analysis.html" look similar by
name but are genuinely different exercises — both were kept.)

## Pause / resume

Every simulation page has a **"← Back to Dashboard"** bar pinned to the top, so a student can
leave at any point and return to the dashboard without losing their place in the overall set.
The dashboard tracks, per device, which simulations are **Not Started**, **In Progress**, or
**Completed** (marked automatically when a simulation's built-in scoring/submit action runs),
shown as a badge on each tile and a progress bar at the top of the page. Progress is stored
in the browser's local storage — it's per-device/per-browser, not a login-based account
system, and can be cleared any time with the "Reset progress" button.

Note: progress tracking remembers *which* simulations have been finished, not mid-simulation
state — each simulation is its own independent exercise, so reopening one after leaving it
mid-way starts that specific simulation over rather than resuming a partially-answered step.

## Structure

```
index.html                                   ← dashboard (start here)
sim-common.js                                ← shared "back to dashboard" bar + progress tracking
1.Cybersecurity Investigation.html
2.Kill chain.html
3.Vulnerability Remediation.html
4.Cybersecurity Configuration.html
5.Security Analysis .html
6.IT Help Desk.html
7.Cybersecurity Suspicous Login.html
8.Web Server Vulnerability.html
9.Security Incident.html
10. Phishing Log Review.html
CySA+ Analyst Workbench OWASP Top 10 Assessment and CVSS Triage Simulator.html
CySA+ SOC Simulation.html
IOC Triage - Analyst Decision Lab.html
Security Incident Ticket Analysis.html
SOC Analyst Simulation - Attack Lifecycle Identification (Cyber Kill Chain)/
SOC Analyst Simulation - Endpoint Behavioral Analysis Simulation - Process & Persistence/
SOC Analyst Simulation - Incident Kill Chain Analysis/
SOC Analyst Simulation - Log Correlation - Phishing to C2/
SOC Analyst Simulation - Web Exploitation, Directory Traversal & Data Exposure/
*_Answer_Key*.pdf / *.jpg                    ← instructor answer keys
```

## Hosting on GitHub Pages

1. Make sure `index.html` and `sim-common.js` sit at the **root** of the repo (not nested
   inside a subfolder) alongside the simulation files.
2. In the repo settings, enable **GitHub Pages** for the branch containing these files (root folder).
3. The dashboard will be live at `https://<username>.github.io/<repo>/`.

No build step, server, or external dependencies are required — everything runs client-side.

## Mobile friendly

The dashboard and simulation pages use responsive layouts and are usable on phones and
tablets, though the drag-and-drop and multi-panel SOC simulations are easiest to use on a
larger screen.
