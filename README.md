# 01 - Google Cybersecurity Fundamentals - SOC L1 Hands-On Lab
> Documented as a real SOC L1 case - 100% mobile lab (Motorola Edge 70 Fusion + Termux)

**Author:** Jamerson Dantas | Aspiring SOC Analyst L1 | Pouso Alegre, MG - Brazil
**Certificate:** Google Cybersecurity Certificate - Course 1/8 Completed
**Lab:** LetsDefend SOC001 - Alert Triage Simulation

### 📌 Executive Summary
Hands-on lab focused on Security Operations Center Level 1 (SOC L1) workflows. This project simulates a real alert triage, investigation, and response cycle, proving that Blue Team studies can be performed without a high-end PC, using only a smartphone.

### 🚨 SOC L1 Workflow Executed

**Alert ID:** SOC001 - Suspicious Domain / Potential Phishing

**1. Initial Triage**
- Received alert from SIEM: suspicious domain detected
- Collected IOC: suspicious domain
- Prioritized alert based on severity and context

**2. Investigation & Enrichment (100% Termux)**
- **WHOIS Investigation:** Validated domain registration date, registrar, and ownership reputation
- **DNS Investigation:** Used `dig` and `nslookup` to validate IP resolution and name servers
- **Linux Validation:** Used essential SOC commands: `whois`, `dig`, `nslookup`, `ping`, `cat`, `grep`
- **Context Enrichment:** Correlated domain age and registrar pattern with phishing indicators

**3. Verdict & Action**
- **Verdict:** True Positive - Suspicious/Malicious Domain Pattern
- **Action:** Block domain/IP on perimeter, add to blocklist, create incident ticket
- **Documentation:** Created incident playbook following NIST Cybersecurity Framework (Identify, Protect, Detect, Respond)

**4. SIEM & SOC Simulation**
- Simulated full alert lifecycle in LetsDefend Security Operations Center
- Practiced MTTR (Mean Time To Respond) awareness: 12m target
- Followed SOC L1 playbook: Triage > Investigate > Document > Escalate

### 🛠️ Stack & Tools
`Linux (Termux)` `WHOIS` `dig` `nslookup` `LetsDefend` `NIST Framework` `SIEM` `Incident Response` `Networking` `SQL` `Blue Team`

### 💡 Key Differentiator
All labs executed on Motorola Edge 70 Fusion + Termux, demonstrating adaptability and resourcefulness in low-resource scenarios - a critical skill for SOC analysts operating in constrained environments.

### 📸 Evidence
- `whois-termux.png` - WHOIS lookup via Termux
- `dns-investigation.png` - dig/nslookup results
- `letsdefend-soc001.png` - Alert triage in LetsDefend

### 🔗 Links
- Certificate: [Google Cybersecurity - Course 1](https://lnkd.in/d3-93XbR)
- LinkedIn: [Add your LinkedIn post link here]

### ➡️ Next Steps
- Course 2: Playbooks and SIEM
- TryHackMe: SOC Level 1 Path
- LetsDefend: SOC Analyst Learning Path

---
#BlueTeam #SOCAnalyst #CyberSecurity #SIEM #Linux #TryHackMe #LetsDefend #GoogleCybersecurity #Termux
