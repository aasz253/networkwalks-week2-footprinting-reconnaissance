# Methodology

## 1. Reconnaissance Workflow

1. Define scope and authorization (see ethics-and-scope.md).
2. Start passive: WHOIS, DNS, search-engine, OSINT (no direct contact beyond normal public queries).
3. Move to light active only where authorized: HTTP header fetch, DNS enumeration, local ping scan.
4. Record every command, raw output, and screenshot at time of execution.
5. Analyze for defensive lessons; never exploit or access beyond scope.

## 2. Tool Roles

| Tool | Type | Purpose |
| ---- | ---- | ------- |
| whois | Passive | Domain registration, registrar, name servers |
| WhatWeb | Light active | Web technology fingerprinting |
| nslookup | Passive/active | DNS resolution verification |
| curl -I | Light active | HTTP status, headers, redirects |
| wafw00f | Fingerprinting | WAF presence heuristics only |
| dnsrecon | Active (authorized) | DNS record enumeration |
| GHDB / dorks | Passive | Indexed-exposure review of own assets |
| Maltego | OSINT | Entity / relationship visualization |
| theHarvester | OSINT | Public hosts, emails, subdomains aggregation |
| Nmap / Zenmap (`-sn`) | Active (lab only) | Host discovery, topology |

## 3. Evidence Handling

* Raw output → `commands/` or `output/` as text.
* Screenshots → `screenshots/` with fixed filenames per module README.
* Analysis → `report/findings.md`.
* Placeholders (`[INSERT RESULT]`, `[ACTUAL RESULT]`) mean "not yet performed" — never replace with guesses.
* Redact PII / credentials before committing.

## 4. Defensive Framing

Every finding should answer: what does an attacker learn, and what should the defender change (patch, config, auth, monitoring, de-indexing, segmentation)?
