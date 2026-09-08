[Lab 01] SOC L1 Fundamentals - Google Cybersecurity Certificate
Status
Lab
Platform
Focus
Documented as a real SOC L1 case - 100% mobile lab (Motorola Edge 70 Fusion + Termux)
Author: Jamerson Dantas | Aspiring SOC Analyst L1 | Pouso Alegre, MG - Brazil
Certificate: Google Cybersecurity Certificate - Course 1/8
Lab: LetsDefend SOC001 + TryHackMe
📌 Executive Summary
Hands-on lab focused on Security Operations Center Level 1 (SOC L1) workflows. This project simulates a real alert triage, investigation, and response cycle, proving that Blue Team studies can be performed without a high-end PC.
🚨 SOC L1 Case: SOC001 - Suspicious Domain
Alert ID: SOC001 | MITRE: T1566.002 - Phishing | NIST: Detect & Respond

1. Initial Triage
• Received alert from SIEM: suspicious domain detected • Collected IOC: suspicious domain (typosquatting) 
2. Investigation (100% Termux)
• WHOIS Investigation: Validated domain age (2 days vs 1997 for google.com) • DNS Investigation: Used dig and nslookup • Enrichment: VirusTotal 5/90 flagged 
IOCs:
• Domain: suspicious-domain.com • Creation: 2 days ago • VT Score: 5/90 
3. Verdict: True Positive - Phishing
Action: Block domain, Isolate host, Escalate to L2
📸 Evidence - Mobile Lab
1. WHOIS Investigation via Termux
![WHOIS Investigation](./images/whois-termux.png)

2. DNS Investigation
![DNS Investigation](./images/dns-investigation.png)

3. LetsDefend - Alert Triage
![Alert triage](./images/letsdefend-soc001.png)
🛠️ Stack & Tools
Linux (Termux) - WHOIS - dig - nslookup - LetsDefend - NIST - SIEM - MITRE ATT&CK
💡 Key Differentiator
All labs executed on Motorola Edge 70 Fusion + Termux, demonstrating adaptability in low-resource scenarios.
🔗 Links • Certificate: https://www.coursera.org/account/accomplishments/verify/DJGJW94CB0P9 • LinkedIn Post: https://www.linkedin.com/posts/jamerson-dantas-66358a191_github-jamersondantas01-fundamentos-ciberseguranca-google-activity-7502885691706630144-chN0  Next Steps • Course 2: Playbooks, SIEM • TryHackMe: SOC Level 1 Path • Learn KQL

Feito por Jamerson Dantas - Futuro SOC Analyst L1
