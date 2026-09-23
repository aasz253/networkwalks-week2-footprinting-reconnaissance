# Ethics and Scope

## Authorization

All work in this repository must be performed only against:

* Your own systems
* Your authorized VirtualBox lab
* Training targets explicitly authorized by the instructor
* Systems for which written permission exists

Record your scope in each module's findings report (permission source, target, date).

## Prohibited

* Unauthorized scanning, enumeration, or access of third-party networks
* Exploitation, credential collection, password guessing, or bypassing access controls
* Publishing passwords, API keys, tokens, private keys, or session data
* Publishing unnecessary personal data (emails, names, device identifiers of others)
* Publishing live exposed third-party cameras, credentials, or private systems (W2-PM2)

## Data Minimization

* Scope GHDB queries with `site:` to authorized domains; describe pattern classes rather than victim URLs.
* Aggregate theHarvester email findings (counts/patterns) instead of dumping personal addresses where avoidable.
* Record lab MACs/IPs only for your own lab; redact anything beyond scope.
* Review every file with `git diff` / `git status` before committing. The `.gitignore` blocks common secret filenames, but it cannot catch secrets pasted into notes — inspect manually.

## Fingerprinting ≠ Verdict

WAF detection, header, and banner results are heuristics. Do not claim a system is "secure" or "insecure" from a single fingerprint.

## Incident Rule

If you accidentally access, receive, or store data beyond scope: stop, do not distribute, delete local copies if appropriate, and inform the instructor.
