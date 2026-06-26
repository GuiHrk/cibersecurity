# 🛡️ Implementação de SIEM Wazuh em virtual box

objetivo
tecnologias
arquitetura
funcionalidades
resultados


##  1. Escopo Técnico e Objetivos 


---

## 2. Arquitetura do Ambiente e Tecnologias
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

## 3. funcionalidades

---
## 4. Resultados
