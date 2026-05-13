# Enumeration Methodology

## 1. Network Connectivity Verification

The attacker machine verified connectivity with the target system before beginning enumeration.

```bash
ping 192.168.19.129
```

This confirmed successful communication between the attacker and target machines.

---

## 2. Service Enumeration Using Nmap

Nmap was used to identify open ports and exposed services on the target.

```bash
nmap 192.168.19.129
```

### Key Observation
The scan identified an active HTTP service on port 80:

```text
80/tcp open http
```

This confirmed the presence of a web server suitable for directory and file discovery testing.

---

## 3. Initial Directory Discovery Using Gobuster

Gobuster was used to enumerate hidden directories and application resources.

```bash
gobuster dir -u http://192.168.19.129 -w /usr/share/wordlists/dirb/common.txt
```

### Example Discovered Resources
- /config
- /docs
- /external
- /setup
- /phpinfo

---

## 4. Recursive Enumeration

Recursive enumeration was performed against discovered directories to identify deeper application paths.

Example:

```bash
gobuster dir -u http://192.168.19.129/dvwa -w /usr/share/wordlists/dirb/common.txt
```

This process identified additional application resources within DVWA.

---

## 5. Advanced File Discovery

Extension-based fuzzing was performed to identify potentially sensitive files.

```bash
gobuster dir -u http://192.168.19.129 -w /usr/share/wordlists/dirb/common.txt -x php,txt,bak,old
```

### Extensions Tested
- .php
- .txt
- .bak
- .old

---

## 6. FFUF Fuzzing

FFUF was used for faster content discovery and response filtering.

```bash
ffuf -u http://192.168.19.129/FUZZ -w /usr/share/wordlists/dirb/common.txt -fc 404
```

This reduced noise and improved discovery efficiency.

---

## 7. HTTP Header Analysis

HTTP response headers were analyzed to identify information disclosure issues.

```bash
curl -I http://192.168.19.129
```

### Information Discovered
- Apache/2.2.8
- PHP/5.2.4
- WebDAV enabled

---

## 8. Traffic Analysis Using Burp Suite

Burp Suite was configured as an intercepting proxy to inspect HTTP requests and application behavior.

Observed:
- GET requests
- application endpoints
- HTTP headers
- session handling behavior

---

## Conclusion

The assessment successfully identified hidden application resources, exposed internal components, and information disclosure issues through directory discovery, recursive enumeration, fuzzing, and HTTP traffic analysis techniques.
