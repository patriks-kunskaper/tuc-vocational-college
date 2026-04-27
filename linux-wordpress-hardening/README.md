# Hardened WordPress Server on Ubuntu 24.04

**Course:** IT Security in Linux/Unix/Mac — TUC Yrkeshögskola, IT-säkerhetsspecialist Year 1  
**Stack:** Apache2 · MariaDB · PHP 8.3 · mkcert SSL · Ubuntu 24.04 Desktop (Hyper-V)

## Overview

A production-ready WordPress server built and hardened from baseline, using the STRIDE 
threat model mapped to CIS Ubuntu 24.04 Benchmark controls. Measurements taken at 
baseline and post-hardening using Lynis, a custom bash script, and OpenSCAP.

## Hardening Approach

Controls implemented across all six STRIDE categories:

| STRIDE Category      | Key Controls |
|----------------------|--------------|
| Spoofing             | SSH on port 2222, root login disabled, fail2ban (3 attempts/5 min/24h ban) |
| Tampering            | HTTPS apt sources, package verification, openssl pinning, AIDE file integrity |
| Repudiation          | auditd enabled, rkhunter baseline scan |
| Information Disclosure | UFW deny-all, HTTPS only (443), IPv6 disabled, umask 027 |
| Denial of Service    | UFW rate limiting, fail2ban, Wordfence, XML-RPC disabled, SYN cookies |
| Elevation of Privilege | Root SSH disabled, unattended-upgrades, unused services/packages removed, PAM pwquality |

## Measurement Results

| Metric        | Baseline | Post-Hardening |
|---------------|----------|----------------|
| Lynis Score   | 65       | 71             |
| Open Ports    | 4        | 7*             |
| Updates       | 18       | 2              |
| Services      | 31       | 28             |

*Increase reflects deliberate addition of Apache (80/443) and SSH (2222); HTTP port 80 subsequently removed.

**OpenSCAP Compliance**

| Profile       | Score  | Rules Passed |
|---------------|--------|--------------|
| CIS Level 1   | 60.3%  | 231/368      |
| CIS Level 2   | 50.8%  | 243/470      |
| STIG          | 52.3%  | 58/220       |

## Key Takeaway

Remaining OpenSCAP failures are predominantly architectural ie separate disk partitions, 
AppArmor profiles, granular sudo configuration. These require secure-by-design decisions 
at installation time, not post-deployment patches. Practical security improvements and 
Lynis/OpenSCAP scores measure different things.

## Files

- `- [WordPress Hardening Guide]([wordpress-hardening-guide.pdf](https://github.com/patriks-kunskaper/tuc-vocational-college/blob/main/linux-wordpress-hardening/Linux-wordpress-hardening.pdf))` — Full assignment submission in English
