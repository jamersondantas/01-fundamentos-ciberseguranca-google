# [Lab 01] SOC L1 Fundamentals - Google Cybersecurity Certificate

![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Lab](https://img.shields.io/badge/Lab-SOC001%20Alert%20Triage-blue?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-100%25%20Mobile%20Termux-black?style=for-the-badge&logo=linux)
![Focus](https://img.shields.io/badge/Focus-SOC%20L1%20%2F%20Blue%20Team-red?style=for-the-badge)

> Documented as a real SOC L1 case - 100% executed on **Motorola Edge 70 Fusion + Termux**. Proving Blue Team operations don't require high-end hardware.

**Author:** Jamerson Dantas | Aspiring SOC Analyst L1 | Pouso Alegre, MG - Brazil
**Certificate:** Google Cybersecurity Certificate - Course 1/8 Completed
**Lab Environment:** TryHackMe + LetsDefend + Termux (Linux)

---

### 📌 Executive Summary

Hands-on lab focused on **Security Operations Center Level 1 (SOC L1)** workflows. This project simulates a real alert triage, investigation, and response cycle from a SIEM alert to containment recommendation.

**Main Goal:** Demonstrate practical skills in alert triage, IOC enrichment (WHOIS/DNS), and incident documentation following the NIST framework.

---

### 🚨 SOC L1 Case: SOC001 - Suspicious Domain / Potential Phishing

**Alert ID:** SOC001
**Severity:** High
**Category:** Phishing / Typosquatting
**MITRE ATT&CK:** T1566.002 - Phishing: Spearphishing Link

#### 1. Initial Triage
- Received alert from SIEM: `Suspicious domain detected`
- Collected IOC: suspicious domain mimicking legitimate brand
- Prioritized based on severity and potential user impact

#### 2. Investigation & Enrichment (100% Termux)

**Commands executed on Termux:**
```bash
whois suspicious-domain.com
dig suspicious-domain.com
nslookup suspicious-domain.com
