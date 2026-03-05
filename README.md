# ⚡ KARNA uage: python3 karna.py -d testphp.vulnweb.com/#/popular --all

### Advanced Bug Bounty Recon & Vulnerability Hunting Tool

```
╔═══════════════════════════════════════════════════════════════╗
║                        K A R N A                              ║
║           Advanced Bug Bounty Recon & Hunt Tool               ║
║                  by Aditya Bhosale                            ║
║          Focused on Overlooked, High-Impact Bugs              ║
╚═══════════════════════════════════════════════════════════════╝
```

KARNA is a **lightweight Python reconnaissance and vulnerability hunting tool** built for bug bounty hunters and penetration testers.
It focuses on **overlooked but high-impact vulnerabilities** that are often missed during traditional scans.

The tool performs multiple security checks including CORS misconfigurations, open redirects, exposed secrets, subdomain takeovers, sensitive file leaks, and more.

---

# 🚀 Features

KARNA includes several automated vulnerability detection modules:

### 🔐 Security Testing Modules

| Module                           | Description                                                 |
| -------------------------------- | ----------------------------------------------------------- |
| **CORS Misconfiguration**        | Detects dangerous cross-origin policies allowing data theft |
| **Security Headers Audit**       | Checks missing security headers like CSP, HSTS              |
| **Open Redirect Scanner**        | Finds redirect parameters vulnerable to phishing            |
| **Subdomain Takeover Detection** | Detects dangling DNS records vulnerable to takeover         |
| **Sensitive File Exposure**      | Searches for exposed `.env`, `.git`, backups, configs       |
| **Host Header Injection**        | Detects password reset poisoning vulnerabilities            |
| **JavaScript Secret Scanner**    | Extracts API keys, tokens, secrets from JS files            |
| **Cookie Security Audit**        | Identifies insecure cookie flags                            |
| **HTTP Method Tampering**        | Detects dangerous HTTP methods enabled                      |
| **Passive Subdomain Discovery**  | Collects subdomains from certificate transparency           |

---

# 🧠 Why KARNA?

Most scanners focus on **common vulnerabilities**, but many real bug bounty findings come from **misconfigurations and overlooked exposures**.

KARNA helps identify:

* Misconfigured infrastructure
* Exposed secrets in JavaScript
* Forgotten admin endpoints
* Subdomain takeover opportunities
* Dangerous CORS policies
* Hidden sensitive files

These are often **high-impact vulnerabilities**.

---

# ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/karna.git
cd karna
```

Run the tool:

```bash
python3 karna.py -h
```

No external dependencies are required.
KARNA runs using **Python standard libraries only**.

---

# 🧪 Usage

### Run full scan

```bash
python3 karna.py -t https://example.com --all
```

### Run specific modules

```bash
python3 karna.py -t https://example.com --cors --headers --js
```

### Discover subdomains

```bash
python3 karna.py -d example.com --subdomains
```

### Subdomain takeover check

```bash
python3 karna.py -d example.com --takeover
```

### Scan sensitive paths

```bash
python3 karna.py -t https://example.com --paths
```

### Generate JSON report

```bash
python3 karna.py -t https://example.com --all -o report.json
```

---

# 📊 Example Output

```
[VULN] Critical CORS! Origin=https://evil.com
[VULN] Possible takeover: blog.example.com → GitHub Pages
[HIGH] Swagger API exposed at /swagger-ui.html
[MED] Missing X-Frame-Options header
```

---

# 📂 Output Report

KARNA can generate a structured JSON report containing:

* vulnerability findings
* severity levels
* scanned modules
* timestamps

Example:

```
report.json
```

---

# ⚠️ Legal Disclaimer

This tool is intended **only for authorized security testing and educational p**
