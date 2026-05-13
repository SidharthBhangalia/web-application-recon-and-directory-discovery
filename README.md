# web-application-recon-and-directory-discovery
Web application reconnaissance and directory/file discovery project using Nmap, Gobuster, FFUF, and Burp Suite to identify hidden endpoints, sensitive files, and exposed application resources.
# Web Application Reconnaissance & Directory Discovery

## Overview
This project demonstrates web application reconnaissance and directory/file discovery techniques used during penetration testing. The assessment focused on identifying hidden application endpoints, undocumented resources, administrative interfaces, and potentially sensitive files using professional web enumeration methodologies.

The project was conducted in a controlled lab environment using Metasploitable 2 and DVWA as vulnerable targets.

---

## Objectives
- Perform web reconnaissance and service enumeration
- Identify hidden directories and files
- Discover undocumented application endpoints
- Analyze exposed resources and information disclosure
- Inspect HTTP traffic using Burp Suite
- Perform recursive directory enumeration and fuzzing

---

## Tools Used
- Nmap
- Gobuster
- FFUF
- Burp Suite
- Curl
- DVWA
- Metasploitable 2

---

## Lab Environment

### Attacker Machine
- Kali Linux

### Target Machine
- Metasploitable 2
- DVWA (Damn Vulnerable Web Application)

---

## Methodology

### 1. Service Enumeration
Nmap was used to identify active services and verify the presence of a web server on the target system.

### 2. Directory Discovery
Gobuster was used to enumerate hidden directories and application resources.

### 3. Recursive Enumeration
Additional enumeration was performed against discovered directories to identify deeper application paths.

### 4. Advanced Fuzzing
FFUF was used for high-speed directory and file fuzzing with extension-based discovery.

### 5. Information Disclosure Analysis
HTTP response headers and exposed resources were analyzed for server and application information leakage.

### 6. Traffic Analysis
Burp Suite was configured as an intercepting proxy to inspect and analyze HTTP requests and responses.

---

## Key Findings
- Hidden application directories identified
- Exposed configuration/setup resources discovered
- Information disclosure through HTTP headers observed
- Multiple undocumented application paths enumerated
- Application traffic successfully intercepted and analyzed

---

## Example Discovered Resources
- /config
- /setup
- /phpinfo
- /docs
- /external

---

## Skills Demonstrated
- Web reconnaissance
- Directory and file discovery
- HTTP traffic analysis
- Application enumeration
- Attack surface mapping
- Burp Suite usage
- Security documentation

---

## Disclaimer
This project was conducted in a controlled lab environment for educational and ethical security testing purposes only.
