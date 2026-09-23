# NetworkWalks Week 2 – Footprinting, Reconnaissance & Network Scanning

## Training

```text
Training: NetworkWalks Cybersecurity & Ethical Hacking
Week: 2
Projects: W2-PM1 → W2-PM5
Platform: Kali Linux / Windows / Virtual Lab
Student: [YOUR NAME]
Batch: [YOUR BATCH]
Date: [DATE]
```

> Do not invent identity, batch, date, or contact details. Replace placeholders above with your own information before submission.

---

## Overview

Week 2 focuses on **footprinting, passive/active reconnaissance, OSINT, and network discovery** — the foundation of every authorized security assessment. This repository documents hands-on practical work performed in a controlled, authorized lab environment.

No results are fabricated. Where a task has not yet been performed, placeholders (`[INSERT RESULT]`, `[ACTUAL RESULT]`) are used. Screenshots and raw tool outputs constitute the primary evidence.

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

## How to Complete This Repository

1. Perform each task in your authorized lab.
2. Copy the raw terminal output into the corresponding file under `commands/` or `output/`, replacing `[INSERT RESULT]`.
3. Save screenshots with the exact filenames referenced in each module README.
4. Fill in each `report/findings.md` with actual findings.
5. Update the Status column in the Module Navigation table above (`[ ]` → `[x]`) only when evidence is present.
6. Fill in `documentation/troubleshooting.md` only with issues that actually occurred.
7. Review the Final Quality Check before pushing to GitHub.

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
