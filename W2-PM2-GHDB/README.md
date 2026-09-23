# W2-PM2 — Footprinting & Reconnaissance with GHDB

## What This Module Covers

* What Google Hacking Database (GHDB) is: a categorized collection of Google search queries (dorks) used for defensive security research.
* What Google dorks are: advanced search operators (`site:`, `filetype:`, `inurl:`, `intitle:`, etc.) that surface publicly indexed information.
* Why defenders use search-engine reconnaissance: to find unintended exposure of their own assets before attackers do.
* How exposed information increases attack surface: indexed documents, directories, login pages, configs, and devices give attackers passive intelligence.
* How organizations reduce unintended exposure: robots directives, authentication, index controls, asset inventory, removal requests, monitoring.

> IMPORTANT: Do NOT publish a public list of live exposed cameras, credentials, private systems, or sensitive third-party data. This repository documents **authorized-training methodology only**.

## Authorized Approach

For any actual testing, use ONLY one of:

1. An authorized lab target approved by the instructor, or
2. A deliberately vulnerable environment (e.g., Google Gruyere, OWASP Juice Shop in local lab), or
3. Methodology documentation without live sensitive targets (search patterns described, no victim data published).

## Search Categories (methodology only — no live victim data)

```text
Exposed directories
Publicly indexed documents
Login pages
Configuration exposure
Security camera search patterns
```

Full methodology: [dorks/ghdb-methodology.md](dorks/ghdb-methodology.md)
Findings template: [evidence/findings.md](evidence/findings.md)

## Screenshots

Save methodology/authorized-lab evidence (with sensitive details redacted) in `screenshots/` with descriptive filenames, e.g. `01-methodology-overview.png`.

Note on file present: `screenshots/00-sqlmap-unrelated.jpg` shows a sqlmap
session enumerating local lab databases (dvwa, metasploit, owasp10, etc.). That
is exploitation tooling, not GHDB search-engine recon, so I'm NOT counting it
as PM2 evidence — leaving the file in place until I replace it with real
GHDB-methodology shots, or delete it before submission.

## Evidence Checklist

```text
[ ] dorks/ghdb-methodology.md reviewed
[ ] evidence/findings.md completed with authorized findings only
[ ] No live third-party sensitive data published
[ ] Screenshots added (if applicable) with redaction
```
