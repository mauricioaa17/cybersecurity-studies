# Blue Team Introduction

Humans as Attack Vectors :
Nesse path vamos aprender como e porque humanos são alvos de attacks ciberneticos.

# the human element
Foi dito que o elo mais fraco da seguraça cibernética são aqueles que ajudam os agentes de ameaça.

# Why Humans Are Targeted
Porque eles podem da acesso a websites, datacente, caixa de emails e acesso a áreas não autorizadas. "Humans are targeted because of the access they can provide"

# Defending Humans
A melhor maneira de defender a parte humano da empresa e treinar os funcionarios a ter diciplina e como reconhecer oq e phishing e também usar Anti-phishing, ter um bom antivirus e manter sempre a equipe treinada para certas situações.

"Trust but verify"
<img width="2347" height="310" alt="image" src="https://github.com/user-attachments/assets/3994375b-7a9d-4f83-8d46-477066deb2b4" />


# Systems as Attack Vectors

* Learn the role of a system in a modern digital world
* Explore a variety of real-world attacks targeting systems
* Practice the acquired knowledge in two realistic scenarios

# Definition of System
Um bom exemplo e do castelo onde o garda sabe oq e phishing e também deepfake, mas nada disso importa se a fechadura do portão for fragil. ele pode facilmente entrar quando não tiver monitorando.

# Attacks on Systems
Treis exemplos de attacks on systems:

* Human-Led Attacks
* Vulnerabilities
* Supply chain

# Misconfigurations
Não são erros de software ou bug mas sim erro na configuração do sistema. geralmente cometido pela equipe de IT.

# Events and Alerts

* SOC L1 analysts:  Review the alerts, distinguish bad from good, and notify L2 analysts in case of a real threat
* SOC L2 analysts:  Receive the alerts escalated by L1 analysts and perform deeper analysis and remediation
* SOC engineers:  Ensure the alerts contain enough information required for efficient alert triage
* SOC manager:  Track speed and quality of alert triage to ensure that real attacks won't be missed

# Alert Triage

<img width="1210" height="450" alt="image" src="https://github.com/user-attachments/assets/44e0ce21-595e-445b-ad87-2e0545daef29" />

# SOC Workbooks and Lookups

Workbook basicamento e um guia/livro que ajuda pessoas mais iniciantes a entender melhor como distinguir os alertas.

SOAR = (Security Orchestration, Automation, and Response) é uma categoria de ferramentas de cibersegurança que centraliza, automatiza e orquestra a resposta a incidentes de segurança.

# Introduction to EDR

* Execução e término de processos:
Ele monitora todos os processos em execução e ociosos, o que ajuda a identificar relações suspeitas entre processos pai e filho, executáveis ​​suspeitos que iniciam um processo, cargas maliciosas, etc.

* Conexões de rede:
 Todas as conexões de rede dos endpoints são monitoradas, o que ajuda a identificar qualquer conexão com um servidor C2 , uso incomum de portas, exfiltração de dados ou movimentação lateral dentro da rede.

* Atividade da Linha de Comando: Captura todos os comandos executados nos endpoints em CMD, PowerShell , etc., o que ajuda a identificar a execução de comandos maliciosos e scripts PowerShell ofuscados , que geralmente passam despercebidos por antivírus tradicionais.

* Modificações de Arquivos e Pastas:
Os agentes de ameaças modificam diferentes arquivos e pastas durante a preparação de dados, a execução de ransomware e a instalação de arquivos maliciosos. O EDR monitora essas atividades.

* Modificações no Registro
O registro é uma mina de ouro de informações sobre as configurações de um sistema Windows. Muitas modificações no registro ocorrem durante uma atividade maliciosa, e a maioria delas é monitorada pelo EDR .

# Splunk: The Basics

Splunk has three main components: Forwarder, Indexer, and Search Head.

* Pesquisa (index=* NOT "france")


# Resumo KQL Overview (Task 5)


O KQL permite filtrar logs de forma simples ou complexa usando campos e valores.

1. Busca por Termo Livre (Free Text Search)
Se você digitar apenas uma palavra na barra de busca, o Kibana procurará essa palavra em todos os campos de todos os logs.

Exemplo: France (retorna qualquer log que mencione a França em qualquer lugar).

2. Busca por Campo Específico (Field Search)
É a forma mais eficiente de pesquisar. Você define o nome do campo, seguido de dois pontos e o valor.

Sintaxe: nome_do_campo : "valor".

Exemplo: Source_Country : "France".

3. Operadores Lógicos (Booleans)
Para refinar sua investigação, você combina termos usando operadores:

AND (E): Retorna logs que atendem a todas as condições ao mesmo tempo.

Exemplo: Source_Country : "France" AND UserName : "James".

OR (OU): Retorna logs que atendem a pelo menos uma das condições.

Exemplo: Source_Country : "France" OR Source_Country : "Brazil".

NOT (NÃO): Exclui termos específicos dos seus resultados.

Exemplo: Source_Country : "France" AND NOT UserName : "James".

4. Uso de Curingas (Wildcards)
O símbolo asterisco (*) serve para buscar variações de uma palavra.

Exemplo: UserName : Jam* encontrará "James", "Jamile", "Jamal", etc.

Dica Visual para o TryHackMe:
No laboratório, você verá que pode adicionar esses filtros clicando nos botões + e - diretamente nos campos da barra lateral (Available Fields), o que gera a query KQL automaticamente para você no topo da tela.

Esse resumo ajudou a clarear como montar as pesquisas? Se quiser, podemos praticar a busca para a pergunta da "Emanda" usando essa lógica de campos!
