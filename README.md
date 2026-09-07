# [Lab 01] SOC Fundamentals - Google Cybersecurity Certificate

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Focus](https://img.shields.io/badge/Focus-SOC%20Analyst%20L1-blue)
![Lab](https://img.shields.io/badge/Lab-Termux%20%7C%20TryHackMe%20%7C%20LetsDefend-orange)
![Tools](https://img.shields.io/badge/Tools-WHOIS%20%7C%20VirusTotal%20%7C%20SIEM-lightgrey)

> **Objetivo:** Documentar meu aprendizado prático do Curso 1 do Google Cybersecurity com foco na rotina de um SOC L1: triagem de alertas e investigação de domínios suspeitos.
> **Diferencial:** Laboratório 100% executado via celular no Termux.

### 👤 Sobre Mim | Jamerson Dantas
Estudante de Cybersecurity com foco em **Blue Team / SOC N1**, em busca da primeira oportunidade na área. Rotina de estudos de 2h/dia.

**Meu Setup de Estudos:** Motorola Edge 70 Fusion + Termux + GitHub Mobile + TryHackMe + LetsDefend

**Links:** [LinkedIn](https://linkedin.com/in/SEU-LINK-AQUI) | [TryHackMe](https://tryhackme.com/p/SEU-USER-AQUI) | [LetsDefend](https://app.letsdefend.io/user/SEU-USER-AQUI)

---
### 📚 1. O Que Aprendi e Como Apliquei

#### Conceitos Chave do Curso 1:
- **CIA Triad (Confidencialidade, Integridade, Disponibilidade):** Usei para classificar o impacto. Ex: domínio de phishing que rouba senha = quebra de Confidencialidade.
- **NIST CSF (Identify, Protect, Detect, Respond, Recover):** Entendi que o SOC L1 atua principalmente em **Detect & Respond**.
- **SOC, SIEM, Playbooks:** Entendi a fila de alertas. SIEM (Ex: Chronicle, Splunk) coleta os logs e o Playbook é o passo-a-passo que o analista segue.

> **Minha maior lição do curso:** O analista de SOC N1 não precisa saber hackear tudo. Ele precisa saber identificar o que é normal e o que é suspeito nos logs e seguir o playbook sem pânico.

---
### 🟢 2. Laboratório Prático - TryHackMe

**Plataforma:** TryHackMe - Path: Pre-Security
**Salas Concluídas:** `Introduction to Cybersecurity` | `Principles of Security (CIA Triad)`

**Investigação Realizada:**
Análise de um domínio suspeito para identificar possível phishing.

**Comando executado no Termux:**
```bash
whois google.com
# Objetivo: Ver data de criação para diferenciar domínio legítimo de domínio recém-criado de phishing
