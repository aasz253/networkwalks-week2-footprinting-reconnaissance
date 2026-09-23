# GHDB Methodology (Authorized Training Only)

## 1. Purpose

Use search-engine reconnaissance defensively: discover what of **your own / authorized lab** infrastructure is publicly indexed, then remediate.

## 2. Core Operators

| Operator | Purpose | Example Pattern (generic) |
| -------- | ------- | ------------------------- |
| `site:` | Limit to a domain you own / are authorized to test | `site:[AUTHORIZED DOMAIN]` |
| `filetype:` | Find indexed file types | `site:[AUTHORIZED DOMAIN] filetype:pdf` |
| `inurl:` | Match URL patterns | `site:[AUTHORIZED DOMAIN] inurl:admin` |
| `intitle:` | Match page titles | `site:[AUTHORIZED DOMAIN] intitle:"index of"` |
| `intext:` | Match body text | `site:[AUTHORIZED DOMAIN] intext:"password"` |
| `-` | Exclude terms | `site:[AUTHORIZED DOMAIN] -inurl:[EXCLUDE]` |

> Replace `[AUTHORIZED DOMAIN]` with your lab target only. Never run these against third parties without permission.

## 3. Category Methodology (no live payloads against third parties)

### 3.1 Exposed directories

* Objective: verify your own servers do not list directory contents publicly.
* Pattern class: title-based directory listing queries scoped with `site:` to your domain.
* Validate: open result, confirm it is your asset, check server auto-index setting.
* Remediate: disable auto-index, add index files, enforce auth, review robots/meta controls.

### 3.2 Publicly indexed documents

* Objective: verify no sensitive PDFs, spreadsheets, or backups of your org are indexed.
* Pattern class: `site:` + `filetype:` scoped to your domain.
* Validate: confirm ownership, classify sensitivity.
* Remediate: remove from web root, add auth, request de-indexing, rotate exposed secrets.

### 3.3 Login pages

* Objective: inventory your own login/admin portals visible externally.
* Pattern class: `site:` + `inurl:` / `intitle:` for login/admin portals of your domain.
* Validate: confirm asset ownership, check for default creds (do NOT test third-party logins), MFA, lockout.
* Remediate: restrict by IP/VPN, enforce MFA, remove from index where appropriate.

### 3.4 Configuration exposure

* Objective: verify `.env`, `.git`, backup, config files of your assets are not indexed or reachable.
* Pattern class: `site:` + filename/extension patterns for your domain.
* Validate: confirm only against your assets.
* Remediate: block dotfiles/backups at server/WAF, remove from repo history, rotate secrets.

### 3.5 Security camera search patterns

* Document the **pattern class only** (e.g., title-based queries for camera viewers). Do not enumerate or publish live third-party cameras.
* If lab includes your own camera/IoT device: scope queries to its authorized hostname, verify auth is required, remediate open access.

## 4. Rules of Engagement

1. `site:`-scope every query to an authorized domain.
2. Never publish IPs, credentials, or screenshots of third-party exposed systems.
3. Redact hostnames/credentials in evidence screenshots.
4. Record date, engine, query class (not victim URLs), and defensive outcome.
5. Prefer deliberately vulnerable local apps for practice.

## 5. Defensive Recommendations Summary

* Maintain an external asset inventory and review indexed content regularly.
* Disable directory listing; require authentication for admin/config areas.
* Set `robots.txt` / `noindex` where appropriate (defense-in-depth, not sole control).
* Remove secrets from code and web roots; rotate anything ever exposed.
* Use Search Console / Bing Webmaster Tools removal for your own URLs.
* Monitor with periodic GHDB-class queries against your own domains.

## 6. Evidence to Record

* Authorized scope statement
* Query classes used (not live victim queries)
* Finding (your asset only): exposed / not exposed
* Screenshot reference (redacted)
* Remediation applied
