# Lessons Learned

## 1. What Reconnaissance Means

Reconnaissance is the systematic collection of publicly available and authorized technical information about a target before any further assessment — to understand attack surface from a defender's perspective.

## 2. Passive vs. Active Reconnaissance

* **Passive:** no direct interaction beyond public sources — e.g., WHOIS lookups, DNS queries to public resolvers, search-engine review, OSINT aggregation (theHarvester, Maltego transforms against public data).
* **Active:** direct interaction with target systems — e.g., HTTP header fetch, DNS enumeration, ping/host discovery. Requires explicit authorization and minimal footprint (lab subnet only for Nmap/Zenmap).

## 3. Importance of DNS

DNS maps names to infrastructure. Enumeration (A/AAAA/MX/TXT/NS/SOA, zone data where authorized) reveals mail flow, providers, and sometimes internal naming — all useful for asset inventory and phishing defense.

## 4. Importance of HTTP Headers

Headers disclose status, redirects, server/framework hints, caching, and security controls (e.g., HSTS, CSP, X-Frame-Options — only where actually observed). Missing security headers are hardening opportunities, not vulnerabilities alone.

## 5. Web Technology Fingerprinting

Tools like WhatWeb identify CMS, frameworks, servers, and analytics. Defenders use this to track outdated components and reduce version disclosure.

## 6. WAF Detection

wafw00f applies heuristics to infer WAF presence. A detection (or lack of one) is fingerprinting only — it proves neither complete security nor insecurity. Defense-in-depth still applies.

## 7. OSINT and theHarvester

Aggregating public emails, subdomains, and hosts shows what an attacker can assemble passively. Lesson for defenders: monitor and minimize public exposure, train staff on phishing, manage subdomain sprawl.

## 8. Google Indexing (GHDB)

Search engines index what is reachable and linked. Misconfigurations (open directories, backup/config files, unprotected portals) become discoverable. Defenders should inventory external assets, control indexing, enforce auth, and periodically run GHDB-class queries against their own domains.

## 9. Maltego Relationship Analysis

Linking domains, DNS records, netblocks, and emails into a graph reveals relationships invisible in flat lists — shared infrastructure, forgotten assets, trust paths. Redact PII; focus on structural insight.

## 10. Network Discovery (Nmap / Zenmap)

Ping/host discovery (`nmap -sn`) on an authorized lab subnet answers: what is alive, what addresses exist, how the topology looks. Lessons: know your own network, segment, watch for rogue devices, restrict scanning to authorized scope.

## 11. Why Reconnaissance Matters to Defenders

Attackers start with reconnaissance; defenders must do it first — inventory, exposure review, hardening, monitoring — so there is less for an adversary to find. Evidence discipline (raw output + screenshots + scope notes) makes findings trustworthy and actionable.

---
*My takeaways so far (updating as I finish each PM):*

* W2-PM1: haven’t run the full set yet, but even the `--version` checks reminded me how much a banner/version leak gives away. Will write more once whois/whatweb outputs are in.
* W2-PM2 → W2-PM5: pending — filling in after the labs.
