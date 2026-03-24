# Vulnerability Assessment and Penetration Testing (VAPT) on a Web Application

## Objective
To assess the security of a web application by performing basic reconnaissance, service detection, and manual authentication testing.

## Tools Used
- Kali Linux on WSL
- Nmap
- Web Browser

## Targets Used
- `testphp.vulnweb.com` for reconnaissance and port scanning
- `demo.testfire.net` for web application testing

## Methodology

### 1. Environment Setup
Kali Linux was installed using WSL on Windows. Nmap was installed and configured for reconnaissance and service detection.

### 2. Reconnaissance and Port Scanning
Initial scanning was performed on the target host to identify available services and understand network exposure.

**Commands used**
```bash
nmap -sV -Pn testphp.vulnweb.com
nmap -p 80,443 -sV -Pn testphp.vulnweb.com