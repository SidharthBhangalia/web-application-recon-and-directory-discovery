# Final Pentest Report

## Project Title
Web Application Reconnaissance & Directory Discovery

---

# Objective

The objective of this assessment was to perform directory and file discovery against a web application environment to identify hidden application endpoints, undocumented resources, administrative interfaces, and potentially sensitive files.

---

# Scope

Target Environment:
- Metasploitable 2
- DVWA (Damn Vulnerable Web Application)

Assessment Type:
- Web reconnaissance
- Directory enumeration
- File discovery
- Information disclosure analysis

---

# Methodology

The assessment was conducted using a structured reconnaissance and enumeration process.

## Activities Performed
- Network connectivity verification
- Service enumeration using Nmap
- Directory discovery using Gobuster
- Recursive application enumeration
- Advanced fuzzing using FFUF
- HTTP header analysis
- Traffic interception using Burp Suite
- Manual parameter observation

---

# Tools Used

- Nmap
- Gobuster
- FFUF
- Burp Suite
- Curl
- Kali Linux
- DVWA
- Metasploitable 2

---

# Key Findings

## Hidden Application Resources
Multiple hidden application paths were identified including:
- /config
- /setup
- /phpinfo
- /docs
- /external

---

## Information Disclosure
HTTP response headers disclosed:
- Apache version
- PHP version
- WebDAV support

Example:
```http
Server: Apache/2.2.8 (Ubuntu) DAV/2
X-Powered-By: PHP/5.2.4-2ubuntu5.10
```

---

## Exposed Internal Components
The assessment identified setup and configuration-related resources that may expose internal application functionality.

---

# Security Impact

The identified resources and disclosures increase application attack surface and may assist attackers in:
- technology fingerprinting
- vulnerability identification
- internal application mapping
- reconnaissance activities

---

# Conclusion

The assessment successfully demonstrated web application reconnaissance and directory/file discovery techniques to identify hidden application resources, undocumented endpoints, exposed internal components, and information disclosure issues using professional penetration testing methodologies.
