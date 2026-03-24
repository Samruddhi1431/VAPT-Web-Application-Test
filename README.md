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
- `nmap -sV -Pn testphp.vulnweb.com`
- `nmap -p 80,443 -sV -Pn testphp.vulnweb.com`

### 3. Scan Analysis
The scan results showed that the target host was reachable, but the tested ports were filtered. This suggests the presence of network-level protections such as a firewall or traffic filtering mechanism.

### 4. Application-Level Testing
Because direct service enumeration was restricted, manual testing was performed on a demo web application. A basic SQL injection payload was tested in the authentication form.

**Payload used**
- `' OR '1'='1`

### 5. Observation
During testing, access to an admin-level interface was observed after authentication attempts. This indicates a possible authentication bypass or weak input validation in the application.

## Findings
- The target system showed filtered ports, indicating network-level security controls
- Manual testing revealed weak authentication behavior in the web application
- A possible authentication bypass vulnerability was observed

## Conclusion
This project demonstrated a basic VAPT workflow involving reconnaissance, scan interpretation, and manual authentication testing. The assessment showed that although network-level protections may be present, application-level weaknesses can still exist.

## Screenshots
- `nmap-basic-scan.png`
- `nmap-filtered-ports.png`
- `admin-access-result.png`
- `nmap-basic-scan.png`
- `nmap-filtered-ports.png`
- `admin-access-result.png`
