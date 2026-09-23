# W2-PM5 — Network Scanning with Zenmap

> Lab subnet only — I'm only scanning my own VirtualBox/host network, nothing else.
> Still need to confirm my actual subnet with ipconfig, not assuming 10.0.0.0/24.

## Task 1 — Install Zenmap / Nmap

Install from the official source (nmap.org). Record version.

```text
Nmap version: [INSERT RESULT]
Zenmap version: [INSERT RESULT]
Install source: [official source URL / package]
```

## Task 2 — Find Local IP and Subnet

Windows:

```cmd
ipconfig
```

Linux:

```bash
ip addr / ip route
```

Screenshot: `screenshots/01-ipconfig.png` → [INSERT RESULT]

Record in [report/findings.md](report/findings.md):

```text
IP Address: [ACTUAL RESULT]
Subnet: [ACTUAL RESULT]
```

Do not hardcode `10.0.0.0/24` — document the actual authorized subnet used.

## Task 3 — Host Discovery (Ping Scan, Authorized Subnet Only)

Example (replace with YOUR actual subnet):

```bash
nmap -sn [YOUR_SUBNET]
```

Full command history: [commands/nmap-commands.txt](commands/nmap-commands.txt)

Screenshots:

* `screenshots/02-ping-scan.png` — scan configuration / command → [INSERT RESULT]
* `screenshots/03-live-hosts.png` — live hosts list → [INSERT RESULT]
* `screenshots/04-host-details.png` — selected host details → [INSERT RESULT]
* `screenshots/05-topology.png` — Zenmap topology view → [INSERT RESULT]

## Task 4 — Live Host Count

```text
Number of live hosts: [ACTUAL RESULT]
```

## Task 5 — Live Host IPs

```text
Live host IP addresses:
[ACTUAL RESULTS — authorized lab only]
```

## Task 6 — MAC Addresses

Record MAC addresses only where legitimately available from your own / local lab. Do not publish unrelated users' device information.

```text
MAC addresses (authorized lab only):
[ACTUAL RESULTS or N/A]
```

## Task 7 — Topology Export

Save the Zenmap topology as:

```text
topology/topology.pdf
```

→ [INSERT FILE — export from Zenmap: Topology tab → save/export]

Document the topology (star / tree layout, hops, key nodes) in [report/findings.md](report/findings.md).

## Evidence Checklist

```text
[ ] commands/nmap-commands.txt contains actual commands
[ ] screenshots/01-ipconfig.png added
[ ] screenshots/02-ping-scan.png added
[ ] screenshots/03-live-hosts.png added
[ ] screenshots/04-host-details.png added
[ ] screenshots/05-topology.png added
[ ] topology/topology.pdf exported and added
[ ] report/findings.md completed
[ ] Only authorized lab subnet scanned
```
