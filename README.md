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
WHOIS Investigation: Validated domain registration date (created 2 days ago), registrar reputation. Legitimate domains like google.com are from 1997, phishing domains are usually <30 days. • DNS Investigation: Validated IP resolution and name servers. • OSINT Enrichment: Checked VirusTotal - 5/90 engines flagged as malicious. Pattern consistent with typosquatting. 
IOCs Collected:
• Domain: suspicious-domain.com (example) • Creation Date: 2 days ago • Registrar: Low-reputation registrar • VT Score: 5/90  3. Verdict & Action • Verdict: True Positive - Confirmed Phishing Attempt • Recommended Actions: ◦ Block domain/IP on perimeter Firewall / DNS Filter[x] ◦ Isolate host that attempted to access the domain[x] ◦ Add to blocklist and create incident ticket[x] ◦ Escalate to L2 with full evidence[x]  4. Documentation
Followed NIST Cybersecurity Framework: Identify > Protect > Detect > Respond > Recover. SOC L1 focus is on Detect & Respond.
📸 Evidence - Mobile Lab 1. WHOIS Investigation via Termux
![WHOIS Investigation via Termux](./images/whois-termux.png)
2. DNS Investigation (dig / nslookup)
![DNS Investigation results](./images/dns-investigation.png)
3. LetsDefend - SOC Alert Triage Simulation
![Alert triage in LetsDefend](./images/letsdefend-soc001.png)
🛠️ Stack & Tools
Linux (Termux) WHOIS dig nslookup LetsDefend NIST CSF SIEM Incident Response MITRE ATT&CK VirusTotal TryHackMe
💡 Key Differentiator - Why Mobile?
All labs executed on Motorola Edge 70 Fusion + Termux, demonstrating:
• Adaptability in low-resource / constrained environments • Real Blue Team mindset: using available tools to get the job done • Linux fundamentals without needing a high-end machine  🔗 Links • Certificate: Google Cybersecurity - Course 1 • LinkedIn Post: View my LinkedIn post about this lab • TryHackMe: My TryHackMe Profile • LetsDefend: LetsDefend Platform  ➡️ Next Steps • [ ] Course 2: Playbooks, SIEM and Incident Management • [ ] TryHackMe: SOC Level 1 Path - Complete • [ ] Learn KQL for Microsoft Sentinel • [ ] LetsDefend: SOC Analyst Learning Path
Made by Jamerson Dantas - Future SOC Analyst L1

#BlueTeam #SOCAnalyst #CyberSecurity #SIEM #Linux #TryHackMe #LetsDefend #GoogleCybersecurity #Termux
