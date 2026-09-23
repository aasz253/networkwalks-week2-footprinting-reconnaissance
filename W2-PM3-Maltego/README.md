# W2-PM3 — Footprinting with Maltego

**Authorized target/domain:** [AUTHORIZED TARGET — your own / instructor-approved domain only]

> Do not publish private personal information unnecessarily. Redact emails / PII not required for the training objective.

## Task 1 — Install Maltego

1. Download from the official Maltego website.
2. Install on Kali Linux / supported platform.
3. Launch and verify version.

Screenshot: `screenshots/01-installation.png` → [INSERT RESULT]

Record:

```text
Maltego version: [INSERT RESULT]
Install source: [official website]
OS: [e.g., Kali Linux]
```

## Task 2 — Account Setup / Target Footprinting

1. Create / sign in to Maltego account (Community / authorized license).
2. Create a new graph.
3. Add a **Domain** entity for the authorized target.
4. Run authorized transforms (e.g., DNS / WHOIS / related-domain transforms available to your license — record actual names).
5. Record results, email-related information if authorized, and relationship visualization.

Screenshots:

* `screenshots/01-installation.jpg` — done, my shot: `sudo dpkg -i Maltego.v4.3.0.deb`
  on Kali (first try without sudo failed as expected, second with sudo installed
  4.3.0). File kept as .jpg since that's the original format.
* `screenshots/02-account-setup.png` → [INSERT RESULT]
* `screenshots/03-domain-entity.png` → [INSERT RESULT]
* `screenshots/04-transform-results.png` → [INSERT RESULT]

Document:

* Domain entity value: [AUTHORIZED TARGET]
* Transforms used: [ACTUAL TRANSFORM NAMES]
* Results: [INSERT RESULT]
* Email-related information if authorized: [INSERT RESULT or N/A]
* Relationship visualization: [describe graph — nodes/edges observed]

## Findings Report

See [report/findings.md](report/findings.md).

## Evidence Checklist

```text
[ ] screenshots/01-installation.png added
[ ] screenshots/02-account-setup.png added (redact personal email if needed)
[ ] screenshots/03-domain-entity.png added
[ ] screenshots/04-transform-results.png added
[ ] report/findings.md completed
[ ] No unnecessary PII published
```
