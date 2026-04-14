![N8NKALI Banner](https://github.com/ogtamimi/n8n-kali/blob/main/banner.png?raw=true)
 
# N8NKALI — Automated Pentesting & CTF Platform
 
![Security](https://img.shields.io/badge/Security-Responsible%20Disclosure-blue) ![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg) ![Docker](https://img.shields.io/badge/Docker-Hub-blue?logo=docker)
 
**N8NKALI** is a ready-to-use Docker environment that combines **Kali Linux** with the **n8n automation platform**, giving you a visual workflow engine with full access to penetration testing and Web-CTF tools no setup required.
 
> ⚠️ **For authorized security testing, CTF competitions, and educational use only.**
 
---
 
## Quick Start
 
Pull and run the container with a single command:
 
```bash
docker run -d --name n8nkali -p 5678:5678 ogtamimi/n8nkali:latest
```
 
Then open your browser and navigate to:
 
```
http://localhost:5678
```
 
That's it. n8n is running with full access to all preinstalled pentest tools.
 
---
 
## Accessing the Terminal
 
Drop into a root shell inside the container at any time:
 
```bash
docker exec -it n8nkali bash
```
 
From here you can run any tool manually, inspect output, or test commands before adding them to a workflow.
 
---
![Execute Command Node](https://github.com/ogtamimi/n8n-Cybersecurity/blob/a62bd4ff8e3aa026880b602aa6c01745ce5ce7ab/Assets/Screenshot%202026-01-05%20060604.png)
 

## Running Tools via n8n Workflows
 
The main power of N8NKALI is chaining tools together visually. Use the **Execute Command** node in n8n to run any tool.
 
### Example Directory Bruteforce with Gobuster
 
```bash
gobuster dir -u http://target.com -w /usr/share/seclists/Discovery/Web-Content/common.txt
```
 
### Example SQL Injection Scan with SQLMap
 
```bash
sqlmap -u "http://target.com/page?id=1" --batch --level=3
```
 
### Example Web Recon with Nikto
 
```bash
nikto -h http://target.com
```
 
### Example Technology Fingerprinting with WhatWeb
 
```bash
whatweb http://target.com
```
 
### Example HTTP Probing with httpx
 
```bash
echo "target.com" | httpx -status-code -title -tech-detect
```
 
Paste any of these into an **Execute Command** node in n8n, connect it to HTTP Request or Webhook nodes, and build full automated recon or CTF-solving pipelines.
 
---
 ![n8n Workflow View](https://github.com/ogtamimi/n8n-Cybersecurity/blob/a62bd4ff8e3aa026880b602aa6c01745ce5ce7ab/Assets/Screenshot%202026-01-05%20055847.png)

## Preinstalled Tools
 
| Category | Tools |
|---|---|
| Recon & Scanning | `nikto`, `whatweb`, `httpx`, `httpie` |
| Directory Fuzzing | `gobuster`, `dirsearch`, `wfuzz` |
| Injection Testing | `sqlmap` |
| Wordlists | `SecLists` |
| Scripting & Dev | `python3`, `pip`, `nodejs`, `npm` |
| Utilities | `curl`, `wget`, `git`, `nano` |
 
---
 
## Installing Additional Tools
 
### From the container shell:
 
```bash
apt update && apt install -y <tool-name>
```
 
### Directly from an n8n Execute Command node:
 
```bash
apt install -y ffuf
```
 
This lets you install tools on-the-fly as part of a workflow, without ever leaving n8n.
 
---
 
 
![CTF Workflow Example](https://github.com/ogtamimi/n8n-Cybersecurity/blob/a62bd4ff8e3aa026880b602aa6c01745ce5ce7ab/Assets/Screenshot%202026-01-13%20122827.png)
 
---
 
## Links
 
- [Docker Hub](https://hub.docker.com/repository/docker/ogtamimi/n8nkali/general)
- [Prebuilt Workflows](https://github.com/ogtamimi/n8n-Cybersecurity/tree/main/Workflows)
 
---
 
## License
 
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)
 
Licensed under the **MIT License** free to use, modify, and distribute with proper credit.
 
---
 
Made with ❤️ by **Omar Al Tamimi**
 