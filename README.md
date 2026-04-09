# Project 01 - Basic Network Scan (Nmap)

## Objective
Perform a basic network scan to identify open ports and services.

## Tool Used
- Nmap

## Target
scanme.nmap.org

## Command Used
nmap scanme.nmap.org

## Scan Results
(See scan-results.txt)

## Findings
- Host is up with low latency (28ms)
- 4 open ports detected:
  - 22 (SSH)
  - 80 (HTTP)
  - 9929 (Nping service)
  - 31337 (Unusual service)

## Analysis
- Port 22 (SSH): Allows remote login, risk of brute force attack
- Port 80 (HTTP): Web server present, possible web vulnerabilities
- Port 9929: Used for Nmap testing, not common in production
- Port 31337: Unusual port, may indicate custom or backdoor service

## Conclusion
The target exposes multiple services, increasing the attack surface.

----------------------------------------------------
## Service Version Scan (-sV)

### Observation
- All ports show "tcpwrapped"
- No version information detected

### Analysis
- "tcpwrapped" means the service is protected or not revealing its details
- This usually happens due to firewall rules or access restrictions

### Insight
- Basic scan showed service names (ssh, http)
- Version scan hid details → indicates defensive mechanism

### Conclusion
The target is limiting service information exposure, which is a security measure to reduce attack surface.
