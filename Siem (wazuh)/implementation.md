# 🛡️ Implementação de SIEM Wazuh em virtual box

objetivo
tecnologias
arquitetura
funcionalidades
resultados


##  1. Escopo Técnico e Objetivos 
 Este documento formaliza o processo de provisionamento, provisionamento de hardware, gerenciamento de incidentes e estabilização de um ambiente centralizado de SIEM (Security Information and Event Management) utilizando a plataforma **Wazuh (Versão 4.9)**. 

O propósito deste laboratório de segurança é estabelecer uma base sólida para a atuação como Analista de SOC (Security Operations Center), focando no entendimento prático de administração de sistemas Linux, depuração de erros de infraestrutura e correlação e ingestão de logs de auditoria.

---

## 2. Arquitetura do Ambiente e Dimensionamento de Ativos
Optou-se pelo modelo de implementação **All-in-One (Single-Node)**, centralizando os três componentes fundamentais do ecossistema no mesmo Host Virtualizado para fins de validação de conceito (PoC):
* **Wazuh Indexer:** Cluster para indexação, busca analítica e armazenamento de alertas criptografados.
* **Wazuh Server:** Motor analítico encarregado na coleta de logs, decodificação de regras, inteligência de ameaças e detecção de vulnerabilidades.
* **Wazuh Dashboard:** Interface web para gerenciamento baseado e visualização gráfica.

### 💻 Parâmetros de Recursos do Hypervisor (VirtualBox)
* **Sistema Operacional Base:** Ubuntu 24.04 LTS
* **Processamento Virtual (vCPU):** 2 Cores dedicados
* **Memória Volátil (RAM):** 6 GB (6144 MB)
* **Armazenamento:** 50 GB (VDI Dinamicamente Alocado)

---

## 3. Evidências Técnicas do Ambiente (Galeria de Validação)

Abaixo constam os registros cronológicos do laboratório de segurança que comprovam o atingimento do status operacional esperado:

### ⚙️ Aborto de Instalação (Falta de Recursos)
Instalação interrompida e expurgo automático de pacotes pelo assistente de deploy do Wazuh.
![Instalação Interrompida](images/erro%20de%20espaco.png)

### 🚀 Orquestração Sequencial Concluída com Sucesso
Estrutura de microsserviços levantada perfeitamente após redimensionamento de recursos.
![Orquestração Concluída](images/instalacao%20completa.png)

### 🔐 Manifesto de Credenciais Administrativas (OPSEC Aplicada)
Geração das credenciais de acesso locais para as contas padrão do sistema. 
*(Lembre-se de colocar a tarja preta na senha antes de subir!)*
![Manifesto de Credenciais](images/obtencao%20de%20senha.png)

### 📊 Painel de Controle Operacional do SOC (Dashboard Inicial)
Interface administrativa do Wazuh Web totalmente funcional e estável após o handshake inicial.
![Wazuh Dashboard](images/dashboard.png)

---
## Comandos Utilizados
# Monitoramento do processo analítico do gerente
sudo systemctl status wazuh-manager

# Reinicialização estruturada em cadeia do ecossistema
sudo systemctl restart wazuh-indexer wazuh-manager wazuh-dashboard

# Verificar todos os serviços Wazuh
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-indexer
sudo systemctl status wazuh-dashboard

# Se algum estiver parado:
sudo systemctl start wazuh-manager
sudo systemctl start wazuh-indexer
sudo systemctl start wazuh-dashboard

# Listar agentes ativos
sudo /var/ossec/bin/agent_control -l
