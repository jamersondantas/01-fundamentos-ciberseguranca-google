# 01 - Fundamentos de Cibersegurança | Google Cybersecurity

> **Status:** Em andamento | **Objetivo:** Entender o papel do SOC Analyst e os pilares da segurança

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
- [ ] Introduction to Cybersecurity
- [ ] Principles of Security (CIA Triad)

**O que eu fiz:**
Usei o comando `whois` no Termux para investigar quem é dono de um domínio suspeito.
Comando usado: `whois google.com`
Aprendizado: Descobri como ver data de criação do domínio, importante para detectar domínios de phishing recém-criados.

**Evidência:**
[Coloque aqui um print do seu Termux - no GitHub app clica em Add file > Upload files]

---

### 🔵 3. Laboratório Prático - LetsDefend

**Plataforma:** LetsDefend - SOC Analyst Learning Path
**Módulo:** What is SOC?

**Alerta praticado:** SOC001 - Exemplo
- **Título do Alerta:** Suspicious Domain Detected
- **Minha Análise:** Verifiquei o domínio no VirusTotal e no WHOIS. Domínio criado há 2 dias, parece phishing.
- **Classificação:** True Positive
- **Ação:** Bloquear domínio no firewall e reportar.

**O que aprendi:** Como funciona uma fila de alertas de um SOC real.

---

### 🐧 4. Comandos no Termux - Meu Lab Linux

Comandos que pratiquei nesse módulo:

```bash
# Ver informações de um domínio
whois example.com

# Ver meu IP e conexão
ifconfig
ping 8.8.8.8

# Navegar no Linux
pwd
ls -la
cat arquivo.txt

# Ajuda de qualquer comando
whois --help