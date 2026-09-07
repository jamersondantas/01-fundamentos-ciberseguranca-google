# [SOC Lab 01] Fundamentos de Cibersegurança - Google Certificate

![Status](https://img.shields.io/badge/Status-Concluído-green) ![Focus](https://img.shields.io/badge/Focus-SOC%20L1-blue) ![Lab](https://img.shields.io/badge/Lab-Termux%20%7C%20TryHackMe%20%7C%20LetsDefend-orange)

> Projeto prático do Curso 1 do Google Cybersecurity Certificate. Foco em entender a rotina de um SOC Analyst: triagem de alertas, análise de domínio e fundamentos de SIEM.

### 👤 Sobre mim
Estudante de Cybersecurity com foco em Blue Team / SOC N1. Estudando 2h/dia pelo celular (Motorola Edge 70 Fusion) usando Termux como laboratório Linux. Objetivo: primeiro emprego em SOC.

**Meu Setup:** Termux + GitHub Mobile + TryHackMe + LetsDefend

---

### 📚 1. O que aprendi no Google - Curso 1

#### Conceitos Chave:
- **CIA Triad:** Confidencialidade, Integridade, Disponibilidade - A base de tudo.
- **NIST CSF:** Framework que organiza a segurança em Identificar, Proteger, Detectar, Responder, Recuperar.
- **SOC (Security Operations Center):** O time que monitora e defende a empresa 24/7.
- **SIEM:** Ferramenta que coleta logs de tudo e gera alertas. Ex: Google Chronicle, Splunk.
- **Playbooks e Runbooks:** O passo-a-passo que o analista segue quando um alerta dispara.

#### Minha maior lição do curso:
> O analista de SOC N1 não precisa saber hackear tudo, ele precisa saber identificar o que é normal e o que é suspeito nos logs e seguir o playbook sem pânico.

---

### 🟢 2. Laboratório Prático - TryHackMe

**Plataforma:** TryHackMe - Path: Pre-Security
**Salas feitas:**
- [✅] Introduction to Cybersecurity
- [✅] Principles of Security (CIA Triad)

**O que eu fiz:**
Usei o comando `whois` no Termux para investigar quem é dono de um domínio suspeito.
Comando usado: `whois google.com`
Aprendizado: Descobri como ver data de criação do domínio, importante para detectar domínios de phishing recém-criados.

**Evidência:**
[ https://github.com/jamersondantas/01-fundamentos-ciberseguranca-google/blob/main/Screenshot_20260906-232942_Termux.png ]

---

### 🔵 3. Laboratório Prático - LetsDefend

**Plataforma:** LetsDefend - SOC Analyst Learning Path
**Módulo:** What is SOC?

### Alerta SOC001 - Suspicious Domain Detected

**1. Triagem (Enrichment):**
- WHOIS: domínio criado há 2 dias (2026-09-04)
- VirusTotal: 5/90 vendors flagged como malicious
- Entropia do domínio: Alta (parece DGA)

**2. Veredito:** True Positive - Phishing

**3. Ação (Playbook):**
- [✅] Bloquear domínio no DNS Firewall
- [✅] Isolar host que acessou
- [✅] Criar regra no SIEM

**O que aprendi:** Como funciona uma fila de alertas de um SOC real.

---

### 🐧 4. Comandos no Termux - Meu Lab Linux

Comandos que pratiquei nesse módulo:

ip a  # ver interfaces
ping -c 4 8.8.8.8
whois -h whois.registro.br exemplo.com.br
