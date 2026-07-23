# Laboratório SIEM Wazuh

## Objetivo

Este laboratório foi desenvolvido para estudar monitoramento de endpoints Windows utilizando o SIEM Wazuh, simulando parte da rotina operacional de um analista SOC N1.

---

# Infraestrutura

## Host

| Item | Valor |
|------|------|
| Sistema Operacional | Windows 10 |
| Memória RAM | 16 GB Ram |
| Virtualizador | Oracle Virtual Box |
| Endereço IP   | 192.168.1.8  |

---

## Máquina Virtual

| Item | Valor |
|------|------|
| Sistema Operacional | Ubuntu Server |
| Versão |  25.04 |
| Hostname | |
| Memória RAM | 6 GB Ram |
| Disco | 50 GB |
| Endereço IP | 192.168.100.10 |

---

## Endpoint Monitorado

| Item | Valor |
|------|------|
| Sistema Operacional | Windows 10 |
| Hostname | WindowsAttacker |
| Endereço IP | 192.168.100.10 |

---

# Componentes

| Componente | Versão |
|------------|---------|
| Wazuh Manager | |
| Wazuh Dashboard | |
| Wazuh Indexer | |
| Wazuh Agent | |

---

# Topologia

```
Windows 10
        │
        │ Wazuh Agent
        │
Ubuntu Server
        │
        │
Dashboard Web
```

---

# Objetivos do Laboratório

- Monitorar eventos do Windows.
- Centralizar logs.
- Simular atividades suspeitas.
- Aprender investigação de eventos.