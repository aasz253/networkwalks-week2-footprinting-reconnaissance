# NetworkWalks Week 2 – Footprinting, Reconnaissance & Network Scanning

## Training

```text
Training: NetworkWalks Cybersecurity & Ethical Hacking
Week: 2
Projects: W2-PM1 → W2-PM5
Platform: Kali Linux (VM) + Windows host
Student: aasz253
Batch: [YOUR BATCH]
Date: [DATE]
```

> Still filling this in as I go — batch/date to update before submission.

---

## My setup

Working through this on my Kali VM. Real versions from my box (checked 23 Sep 2026):

```text
OS: Kali GNU/Linux Rolling 2026.2 (kernel 6.19.14+kali-amd64)
whois 5.6.6
WhatWeb 0.6.4
curl 8.20.0
dnsrecon 1.3.1
Nmap 7.99
theHarvester (installed, /usr/bin/theHarvester)
Zenmap (installed, throws a Python locale DeprecationWarning on launch — still opens)
Maltego: not installed yet
```

Windows side used for `ipconfig` + Zenmap topology part in PM5.

---

## Overview

Week 2 is all about footprinting and recon — basically learning what you can find
out about a target without touching anything you're not supposed to. I'm doing
all of this in my own lab / against instructor-approved targets only.

Honest note: where I haven't run something yet I left `[INSERT RESULT]` /
`[ACTUAL RESULT]` markers instead of guessing. Raw outputs + screenshots are
the actual proof, so those folders are empty until I work through each task.

---

## Learning Objectives

Week 2 covers:

* Passive reconnaissance concepts and workflow
* Domain information gathering (WHOIS)
* DNS reconnaissance (nslookup, dnsrecon)
* Web technology fingerprinting (WhatWeb)
* HTTP header analysis (curl)
* WAF identification (wafw00f) — fingerprinting only, not a security verdict
* GHDB methodology and search-engine reconnaissance
* OSINT principles and defensive implications
* Maltego entity / transform / relationship analysis
* theHarvester for public emails, subdomains, and hosts
* Network discovery and host enumeration
* Zenmap / Nmap ping scan and topology visualization
* Evidence collection (commands + raw output + screenshots)
* Security awareness and defensive recommendations

---

## Module Navigation

| Module | Topic | Main Tools | Status |
| ------ | ----- | ---------- | ------ |
| [W2-PM1-Kali-Recon](W2-PM1-Kali-Recon/) | Kali Recon | whois, WhatWeb, nslookup, curl, wafw00f, dnsrecon | [ ] |
| [W2-PM2-GHDB](W2-PM2-GHDB/) | GHDB | Google / GHDB | [ ] |
| [W2-PM3-Maltego](W2-PM3-Maltego/) | Maltego | Maltego | [ ] |
| [W2-PM4-theHarvester](W2-PM4-theHarvester/) | OSINT | theHarvester | [ ] |
| [W2-PM5-Zenmap](W2-PM5-Zenmap/) | Network Scanning | Zenmap / Nmap | [ ] |

> Do not mark a module complete until actual evidence (raw output + screenshot) has been added.

Additional documentation:

* [Methodology](documentation/methodology.md)
* [Ethics and Scope](documentation/ethics-and-scope.md)
* [Troubleshooting](documentation/troubleshooting.md)
* [Lessons Learned](documentation/lessons-learned.md)

---

## Repository Structure

```text
networkwalks-week2-footprinting-reconnaissance/
│
├── README.md
│
├── W2-PM1-Kali-Recon/
│   ├── README.md
│   ├── commands/
│   ├── screenshots/
│   └── report/findings.md
│
├── W2-PM2-GHDB/
│   ├── README.md
│   ├── dorks/ghdb-methodology.md
│   ├── evidence/findings.md
│   └── screenshots/
│
├── W2-PM3-Maltego/
│   ├── README.md
│   ├── screenshots/
│   └── report/findings.md
│
├── W2-PM4-theHarvester/
│   ├── README.md
│   ├── commands/
│   ├── output/
│   ├── screenshots/
│   └── report/findings.md
│
├── W2-PM5-Zenmap/
│   ├── README.md
│   ├── commands/nmap-commands.txt
│   ├── screenshots/
│   ├── topology/topology.pdf
│   └── report/findings.md
│
├── documentation/
│   ├── methodology.md
│   ├── ethics-and-scope.md
│   ├── troubleshooting.md
│   └── lessons-learned.md
│
└── .gitignore
```

---

## Ethics and Authorization

All reconnaissance and scanning documented here **must be performed only against**:

* Your own systems
* Your authorized VirtualBox lab
* Training targets explicitly authorized by the instructor
* Systems for which written permission exists

Do **not** perform unauthorized scanning, exploitation, credential collection, or access attempts. Do not publish passwords, API keys, tokens, private credentials, or unnecessary personal/third-party data. See [documentation/ethics-and-scope.md](documentation/ethics-and-scope.md).

WAF detection, header analysis, and DNS enumeration are **fingerprinting techniques** — they do not prove complete security or insecurity.

---

## Evidence Standard

For every completed task:

1. Run the command/tool.
2. Save the actual output (raw text in `commands/` or `output/`).
3. Capture a screenshot.
4. Give the screenshot a descriptive filename (as listed in each module README).
5. Explain what the screenshot proves.
6. Add the evidence to the appropriate README/report.
7. Never fabricate evidence.

Example:

```markdown
## Evidence

The following screenshot shows the actual DNS resolution performed during the lab:

![DNS Resolution](screenshots/03-nslookup.png)
```

Screenshot files are not committed in this template — add your own `.png` files to the indicated `screenshots/` folders. Each folder contains a `.gitkeep` so the directory structure is preserved.

---

## How I'm working through this

1. Run each command in my lab, paste the real terminal output into `commands/` or `output/`.
2. Screenshot it, keep the filenames exactly as each module README says.
3. Write up what I actually saw in `report/findings.md`.
4. Only tick the box in the table above when the evidence is really there.
5. Anything weird that breaks goes in `documentation/troubleshooting.md`.

## Progress log

```text
23 Sep 2026 — repo scaffolded, tool versions noted. PM1 outputs + screenshots still pending.
[DATE] — PM1 whois/whatweb run ......... [ ]
[DATE] — PM4 theHarvester runs .......... [ ]
[DATE] — PM5 lab subnet scan ............ [ ]
```


---

## GitHub Commands

```bash
git init
git add .
git commit -m "Add Week 2 cybersecurity reconnaissance labs"
git branch -M main
git remote add origin [GITHUB_REPOSITORY_URL]
git push -u origin main
```

> Replace `[GITHUB_REPOSITORY_URL]` with your actual repository URL. Example format (do not use unless it is yours):
> `https://github.com/[YOUR_USERNAME]/networkwalks-week2-footprinting-reconnaissance.git`

**Pre-commit check:** before `git add .`, verify no file contains credentials, tokens, private keys, or unnecessary personal data. See `.gitignore`.

---

## Final Quality Check

```text
[ ] Root README created
[ ] W2-PM1 folder created
[ ] W2-PM2 folder created
[ ] W2-PM3 folder created
[ ] W2-PM4 folder created
[ ] W2-PM5 folder created
[ ] Screenshots organized
[ ] Command outputs organized
[ ] Findings documented
[ ] Troubleshooting documented
[ ] Lessons learned documented
[ ] Ethics/scope documented
[ ] No credentials committed
[ ] No fabricated results
[ ] No unnecessary private information
[ ] Actual lab evidence included
[ ] Topology PDF included where required
[ ] All README links work
[ ] Repository is ready for instructor review
```

> Do not mark unchecked items as completed. This repository must demonstrate your own practical work, not a reproduction of course notes.
