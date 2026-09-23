# W2-PM4 — Footprinting & Reconnaissance with theHarvester

> Run these commands only where permitted by the training scope and current tool/source availability. Public sources and rate limits change — record what actually happened.

## Task 1 — Baidu source

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

* Command record: [commands/baidu-command.txt](commands/baidu-command.txt)
* Raw output: [output/baidu-results.txt](output/baidu-results.txt)
* Screenshot: `screenshots/01-baidu-results.png` → [INSERT RESULT]

## Task 2 — All sources

```bash
theHarvester -d microsoft.com -l 50 -b all
```

* Command record: [commands/all-sources-command.txt](commands/all-sources-command.txt)
* Raw output: [output/all-sources-results.txt](output/all-sources-results.txt)
* Screenshot: `screenshots/02-all-sources-results.png` → [INSERT RESULT]

## What to Document

* Number of results (hosts / emails / IPs as reported by the tool — actual counts only)
* Domains / subdomains discovered
* Public email addresses if appropriate (minimize PII — aggregate counts preferred)
* Sources queried and which returned data
* Differences between the two searches (limit, source breadth, result volume)
* Limitations (source availability, rate limiting, stale data, API keys required)

Save actual output — do not fabricate. See [report/findings.md](report/findings.md).

## Evidence Checklist

```text
[ ] commands/baidu-command.txt saved
[ ] commands/all-sources-command.txt saved
[ ] output/baidu-results.txt contains actual output
[ ] output/all-sources-results.txt contains actual output
[ ] screenshots/01-baidu-results.png added
[ ] screenshots/02-all-sources-results.png added
[ ] report/findings.md completed
[ ] No unnecessary personal information published
```
