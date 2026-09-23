# W2-PM1 — Footprinting & Reconnaissance with Multiple Kali Tools

**Target (training):** `networkwalks.com`
**Scope:** my own lab + whatever the instructor cleared — passive recon only for this one

> Re-checking everything live, not trusting the screenshots in the course slides
> since WHOIS/DNS stuff changes. What I paste in `commands/` is what I actually got.

## My lab notes

Ran `--version` checks on 23 Sep 2026 so I know my baseline before the real runs:

```text
whois 5.6.6 / WhatWeb 0.6.4 / curl 8.20.0 / dnsrecon 1.3.1
```

Outputs + screenshots still to come. Leaving the placeholders until then.

## Tasks

### Task 1 — WHOIS

```bash
whois networkwalks.com
```

Document:

* Registrar
* Registration / creation information
* Expiry information
* Name servers
* Other relevant publicly available information

Raw output: [commands/whois.txt](commands/whois.txt)
Screenshot: `screenshots/01-whois.png` → [INSERT RESULT — add screenshot, do not fabricate]

### Task 2 — WhatWeb

```bash
whatweb networkwalks.com
```

Document actual technologies discovered. Do not copy example results from course material if the current scan differs.

Raw output: [commands/whatweb.txt](commands/whatweb.txt)
Screenshot: `screenshots/02-whatweb.png` → [INSERT RESULT]

### Task 3 — DNS (nslookup)

```bash
nslookup networkwalks.com
```

Document actual DNS resolution results (A / AAAA / CNAME as returned).

Raw output: [commands/nslookup.txt](commands/nslookup.txt)
Screenshot: `screenshots/03-nslookup.png` → [INSERT RESULT]

Example evidence block (use when completed):

```markdown
## Evidence

The following screenshot shows the actual DNS resolution performed during the lab:

![DNS Resolution](screenshots/03-nslookup.png)
```

### Task 4 — HTTP Headers (curl)

```bash
curl -I https://networkwalks.com
```

Document:

* HTTP status
* Server information if exposed
* Redirects
* Security headers (only if present in output)
* Cache-related headers
* Other relevant headers

Do not claim a header exists unless the actual output shows it.

Raw output: [commands/curl-headers.txt](commands/curl-headers.txt)
Screenshot: `screenshots/04-curl-headers.png` → [INSERT RESULT]

### Task 5 — WAF Detection (wafw00f)

```bash
wafw00f networkwalks.com
```

Document the actual result. WAF detection is fingerprinting only — it does not prove complete security or insecurity.

Raw output: [commands/wafw00f.txt](commands/wafw00f.txt)
Screenshot: `screenshots/05-wafw00f.png` → [INSERT RESULT]

### Task 6 — DNSRecon

```bash
dnsrecon -d networkwalks.com
```

Document the actual records returned. Do not publish sensitive information unnecessarily.

Raw output: [commands/dnsrecon.txt](commands/dnsrecon.txt)
Screenshot: `screenshots/06-dnsrecon.png` → [INSERT RESULT]

## Findings Report

See [report/findings.md](report/findings.md).

## Screenshots on file

* `screenshots/00-autorecon-extra.jpg` — extra, not a required task: shows an
  `sudo autorecon <redacted>.com` run with open tcp ports (25/993/21/995/110/
  53/80/143/587/443/2525) and 3 scans still running. Target name redacted in
  the image. Keeping it here as background only.
* Required shots still pending: `01-whois.png`, `02-whatweb.png`,
  `03-nslookup.png`, `04-curl-headers.png`, `05-wafw00f.png`, `06-dnsrecon.png`.

## Evidence Checklist

```text
[ ] commands/whois.txt contains actual output
[ ] commands/whatweb.txt contains actual output
[ ] commands/nslookup.txt contains actual output
[ ] commands/curl-headers.txt contains actual output
[ ] commands/wafw00f.txt contains actual output
[ ] commands/dnsrecon.txt contains actual output
[ ] screenshots/01-whois.png added
[ ] screenshots/02-whatweb.png added
[ ] screenshots/03-nslookup.png added
[ ] screenshots/04-curl-headers.png added
[ ] screenshots/05-wafw00f.png added
[ ] screenshots/06-dnsrecon.png added
[ ] report/findings.md completed with actual findings
```
