# Crypto DNS Recon

Simple and fast DNS reconnaissance tool for pentesting.

---

## 🚀 Features

- Domain resolution
- Name Server (NS) enumeration
- MX record enumeration
- Zone Transfer (AXFR) attempt
- Subdomain brute force (with threading)

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/MrLdx88-crypto/crypto-dns-recon.git
cd crypto-dns-recon

Create virtual environment:

python3 -m venv venv
source venv/bin/activate

Install dependencies:

pip install dnspython

🧠 Usage

Basic scan:

python crypto.py -enum target.com

🔧 Options

Option	Description
-enum	Target domain
--threads	Number of threads (default: 50)
--wordlist	Path to subdomain wordlist

📌 Examples

Run with custom threads:

python crypto.py -enum target.com --threads 20

Use custom wordlist:

python crypto.py -enum target.com --wordlist wordlists/subdomains.txt

Full example:

python crypto.py -enum target.com --threads 30 --wordlist wordlists/subdomains.txt

📂 Project Structure
Crypto-dns-recon/
│
├── crypto.py
├── core/
│   ├── resolver.py
│   ├── nameserver.py
│   ├── mx.py
│   ├── axfr.py
│   └── bruteforce.py
│
└── wordlists/
    └── subdomains.txt

⚠️ Notes

AXFR rarely works (only in misconfigured servers)
Brute force results depend on wordlist quality
High thread count may cause instability or detection

⚖️ Disclaimer

This tool is for educational purposes and authorized testing only.
Do not use against targets without permission.

💡 Future Improvements

Wildcard DNS detection
Output to file (txt/json)
Improved record parsing
Performance optimizations
