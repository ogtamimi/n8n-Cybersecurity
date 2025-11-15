# N8NKALI --- Kali Linux + n8n (Root Access)

This Docker image contains **Kali Linux (rolling)** combined with the
**n8n Automation Platform**, running with **full root access**.\
It allows you to automate and execute penetration-testing, Web-CTF
tools, and command-line operations directly from inside the **n8n
Execute Command Node** or from the **bash shell** inside the container.

A collection of essential Web-CTF and pentest tools is preinstalled, and
you can install additional tools anytime.

## 🧰 Included Tools

-   sudo\
-   wget\
-   curl\
-   git\
-   nano\
-   python3 + pip\
-   nodejs + npm\
-   sqlmap\
-   dirsearch\
-   gobuster\
-   wfuzz\
-   nikto\
-   whatweb\
-   httpie\
-   httpx\
-   SecLists (wordlists)

## 🚀 How to Run

``` bash
docker run -d --name n8nkali -p 5678:5678 ogtamimi/n8nkali:latest
```

## 🖥️ Access the Container Shell

``` bash
docker exec -it n8nkali bash
```

## ➕ Install Additional Tools

### From inside the container:

``` bash
apt update
apt install <tool>
```

### From n8n Execute Command node:

``` bash
apt install -y ffuf
```
## How to build 
just use this command
``` bash
docker push ogtamimi/n8nkali:v2
```

## ❤️ Summary

**N8NKALI = Kali Linux + n8n + Root Access + Web-CTF Tools**\
Made With ❤️ by **Omar Al Tamimi**
