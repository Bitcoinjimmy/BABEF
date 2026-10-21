<div align="center">

# B.A.B.E.F

<img src="https://readme-typing-svg.demolab.com?font=Orbitron&size=28&pause=1000&color=00F5FF&center=true&vCenter=true&width=700&lines=Researcher:+dontaskmehow;Bitcoinj;Transaction+Spoofing;Payment+Hijacking" alt="BABEF banner" />

[![Status](https://img.shields.io/badge/Status-Research-red)](https://github.com/Bitcoinjimmy/BABEF)
[![Target](https://img.shields.io/badge/Target-bitcoinj-blue)](https://github.com/Bitcoinjimmy/BABEF)
[![Impact](https://img.shields.io/badge/Impact-Auth_Bypass-orange)](https://github.com/Bitcoinjimmy/BABEF)

# B.A.B.E.F - A BITCOINJ AUTHENTICATION BYPASS EXPLOIT FRAMEWORK

> **Researcher: dontaskmehow**

> CVE-2026-44714 | bitcoinj | Transaction Spoofing | Payment Hijack

</div>

`BABEF` is a research-focused exploit framework targeting a critical signature verification flaw in the `bitcoinj` library used by Java-based Bitcoin wallet and payment systems.

This project is built around **CVE-2026-44714**, a vulnerability in bitcoinj’s transaction validation path that can allow spoofed transaction behavior, authentication bypass conditions, and payment-flow manipulation in affected implementations.

----------------------------------------

**THREAT OVERVIEW** 

**This** framework explores the impact of the flaw across:

- wallet authentication layers
- transaction verification logic
- payment channel behavior
- downstream services relying on bitcoinj validation

**Impact profile**

- Attack Vector: Local / Application-level
- Privilege Requirement: Low
- User Interaction: Minimal / None
- Confidentiality: High
- Integrity: High
- Availability: High

---

**ATTACHED COMPONENTS** 

**1.** Python Exploit

`bitcoinj_spoof.py`

- A Python-based proof-of-concept focused on transaction spoofing behavior and vulnerability validation against vulnerable bitcoinj implementations.

**2.** JavaScript Payload

`bitcoinj_hijack.js`

- A JavaScript payload designed to simulate payment channel hijack behavior in affected web-facing wallet or payment environments.

### 3. Ruby C2 Server

`bitcoinj_c2.rb`

- A Ruby-based command-and-control harness used to model attack orchestration and stolen-funds tracking in a lab environment.

---

**INSTALL & RUN**

***Requirements***

- Python 3.10+
- Node.js 18+
- Ruby 3.0+
- Git
- Access to a vulnerable bitcoinj-backed target environment for authorized testing

### 1) Clone repository

```bash
git clone https://github.com/Bitcoinjimmy/BABEF.git
cd BABEF
```

### 2) Python exploit setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Run the Python exploit:

```bash
python3 bitcoinj_spoof.py <target_wallet> <recipient_address> <amount>
```

Example:

```bash
python3 bitcoinj_spoof.py 1BoatSLRHtKNngkdXEeobR76b53LETtpyT 1J7mdg5rbQyUHENYdx39WVWK7fs5ZQ7VQ 0.25
```

### 3) JavaScript payload setup

```bash
npm install
```

Run the hijack payload:

```bash
node bitcoinj_hijack.js
```

### 4) Ruby C2 server

```bash
ruby bitcoinj_c2.rb
```

----------------------------------------

## / RESEARCH FOCUS /

The project is intended to:

- authentication bypass risk in bitcoinj-backed services
- spoofed transaction injection
- payment channel manipulation
- exploitation pathways in vulnerable wallet stacks

This repo is structured as a red-team / security research showcase and is intended for authorized testing and defensive analysis only.

----------------------------------------

## / DISCLAIMER /

This repository is for security research, red-team validation, and defensive assessment in environments where such activities are explicitly authorized. Use responsibly and in accordance with applicable law and governance policies. Researcher dontaskmehow is not responsible!

----------------------------------------

## / STATUS /

`BABEF` is a bitcoinj-focused exploitation framework centered on **CVE-2026-44714**, designed to surface the impact of signature verification weaknesses in wallet and payment systems.
