# 🛡️ Implementação de SIEM Wazuh em virtual box

objetivo
tecnologias
arquitetura
funcionalidades
resultados


##  1. Escopo Técnico e Objetivos 


---

## 2. Arquitetura do Ambiente e Tecnologias
implementação **All-in-One (Single-Node)**, centralizando os três componentes fundamentais do ecossistema no mesmo Host Virtualizado para fins de validação de conceito (PoC):
* **Wazuh Indexer:** busca analítica e armazenamento de alertas criptografados e logs processados pelo servidor.
* **Wazuh Server:** recebe logs, realiza a leitura e filtragem, aplica regras de segurança para relacionar a eventos e disparar alertas.
* **Wazuh Dashboard:** Interface web para gerenciamento baseado e visualização gráfica contectada ao indexer e ao server.

### 💻 Parâmetros de Recursos do Hypervisor (Oracle VirtualBox)
* **Sistema Operacional Base:** Ubuntu 24.04 LTS
* **Processamento Virtual (vCPU):** 2 Cores dedicados
* **Memória Volátil (RAM):** 6 GB (6144 MB)
* **Armazenamento:** 50 GB

---

## 3. funcionalidades

---
## 4. Resultados
