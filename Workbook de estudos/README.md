# 📘 Workbook de Estudos – Email, PowerShell e Network Analysis

Este workbook foi criado para estudo prático, com foco em **TI, SOC e Cyber Security**, alinhado com cenários reais de trabalho.

---

## 📧 MÓDULO 1 – EMAIL (Análise, Segurança e Operação)

### 🎯 Objetivo

Entender o funcionamento do email, identificar ameaças (phishing/spam) e analisar headers.

### 📚 Conteúdo Teórico

* Funcionamento do email (SMTP, POP3, IMAP)
* Diferença entre Spam, Phishing e Spear Phishing
* Email spoofing
* SPF, DKIM e DMARC
* Email corporativo (Exchange / Google Workspace)

### 🧠 Conceitos-Chave

* **SPF**: valida se o servidor tem permissão para enviar emails pelo domínio
* **DKIM**: assinatura digital que garante integridade da mensagem
* **DMARC**: política que define o que fazer se SPF/DKIM falharem

### 🛠️ Ferramentas

* Google Admin Toolbox (Messageheader)
* MXToolbox
* Outlook / Gmail (ver headers)

### 🧪 Exercícios Práticos

1. Copie o header de um email suspeito e responda:

   * O domínio é legítimo?
   * SPF passou ou falhou?
   * DKIM passou ou falhou?
   * IP de origem parece confiável?

2. Classifique o email:

   * ( ) Legítimo
   * ( ) Spam
   * ( ) Phishing

### 📝 Atividade de Relatório (SOC)

* Resumo do email analisado
* Indicadores de comprometimento (IOC)
* Conclusão e recomendação

---

## 💻 MÓDULO 2 – POWERSHELL

### 🎯 Objetivo

Automatizar tarefas administrativas e realizar análises básicas em ambiente Windows.

### 📚 Conteúdo Teórico

* O que é PowerShell
* Cmdlets
* Pipeline ( | )
* Variáveis
* Execução de scripts

### 🧠 Comandos Essenciais

* Get-Help
* Get-Command
* Get-Process
* Get-Service
* Get-EventLog
* Get-Content

### 🛠️ Exemplos Práticos

* Listar processos ativos
* Verificar serviços em execução
* Ler arquivos de log
* Buscar eventos de erro

### 🧪 Exercícios Práticos

1. Liste todos os serviços em execução
2. Exporte processos ativos para um arquivo .txt
3. Verifique eventos de falha de login

### 📝 Desafio

Crie um script que:

* Verifique se um serviço está rodando
* Caso não esteja, exiba um alerta

---

## 🌐 MÓDULO 3 – NETWORK ANALYSIS

### 🎯 Objetivo

Entender tráfego de rede, identificar anomalias e possíveis ataques.

### 📚 Conteúdo Teórico

* Modelo OSI
* TCP/IP
* Portas e protocolos
* DNS, HTTP, HTTPS
* Tráfego normal vs malicioso

### 🧠 Conceitos-Chave

* Three-way handshake
* DNS Query / Response
* HTTP Status Codes
* Tráfego criptografado

### 🛠️ Ferramentas

* Wireshark
* TCPDump
* Nmap
* Netstat

### 🧪 Exercícios Práticos

1. Capture tráfego HTTP no Wireshark

2. Identifique:

   * IP de origem
   * IP de destino
   * Porta utilizada

3. Analise um possível ataque:

   * Port scan
   * DNS suspeito

### 📝 Atividade SOC

* Descrição do tráfego
* Evidências coletadas
* Impacto
* Conclusão

---

## 📌 CHECKLIST DE EVOLUÇÃO

* [ ] Entendo headers de email
* [ ] Consigo identificar phishing
* [ ] Sei automatizar tarefas com PowerShell
* [ ] Sei analisar tráfego de rede

---

## 🚀 Próximos Passos

* TryHackMe (SOC Level 1)
* Criar repositório no GitHub para anotações
* Praticar relatórios técnicos

---

📎 **Dica:** Use este workbook como base e vá adicionando exemplos reais do seu dia a dia de estudo e trabalho.
