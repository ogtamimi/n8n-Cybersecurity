# 🔐 Security Policy

## Supported Versions

We provide security updates only for the latest published version of this project.

| Version        | Supported | Notes |
|----------------|-----------|-------|
| Latest (v2+)   | ✅ Yes    | Actively maintained, receives fixes and updates |
| Older versions | ❌ No     | Please upgrade to the latest release |

---

## Reporting a Vulnerability

If you discover a security issue or suspicious behavior in this project, **please DO NOT open a public GitHub issue**.

Instead, contact us privately:

- **Email:** security@yourdomain.com *(replace with your real email)*
- **Alternative (optional):** Create a private GitHub security advisory

We appreciate responsible disclosure and will respond as fast as possible.

---

## Disclosure Process

When you report a vulnerability, please include:

1. A clear description of the issue  
2. Steps to reproduce  
3. Expected vs. actual behavior  
4. Screenshots or logs (if available)  
5. Suggested fix (optional)

**Timeline:**

- **Acknowledgment:** within 48 hours  
- **Initial assessment:** 3–7 days  
- **Fix or mitigation:** depending on complexity  
- **Public disclosure:** coordinated with the reporter

---

## Security Best Practices for Users

To keep your deployment secure, we recommend:

- Always run the latest image version  
- Avoid exposing n8n directly to the internet  
- Use reverse proxies (NGINX/Traefik) with SSL  
- Change default environment variables immediately  
- Use strong webhook secrets and credentials  
- Restrict container permissions whenever possible  
- Update system packages regularly

---

## Hardening the Container

Our Kali-n8n image includes:

- Minimal required capabilities  
- Latest Linux security patches  
- Isolated environment for command execution  
- Support for additional tools installed by the user  
- Non-root execution where possible  
- Optional root mode for full Kali workflows

If you notice unsafe defaults or want to suggest improvements, contact us privately.

---

## Responsible Usage

This project is intended **only for legal penetration testing, automation, and research purposes**.

You must comply with all applicable laws and obtain authorization before running any security tools.

We do **NOT** condone or support illegal activities.

---

## Thank You

We appreciate all contributions that help keep this project secure.  
Your feedback helps us improve and maintain a safe ecosystem for everyone.

