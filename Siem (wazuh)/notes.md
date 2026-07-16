# Comandos Linux

## Monitoramento do processo analítico do gerente
sudo systemctl status wazuh-manager

## Reinicialização estruturada em cadeia do ecossistema
sudo systemctl restart wazuh-indexer wazuh-manager wazuh-dashboard

## Verificar todos os serviços Wazuh
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-indexer
sudo systemctl status wazuh-dashboard

## Se algum estiver parado:
sudo systemctl start wazuh-manager
sudo systemctl start wazuh-indexer
sudo systemctl start wazuh-dashboard

## Listar agentes ativos
sudo /var/ossec/bin/agent_control -l

## Iniciar agente no windows

restart-service wazuhsvc || Net Start wazuhsvc


# Como ler um alerta:

- Exemplo: 
{
  "timestamp": "2024-12-10T02:15:33.000+0000",

  "rule": {
    "level": 10,
    "id": "5763",
    "description": "SSH brute force attempt.",
    "mitre": {
      "id": ["T1110"],
      "tactic": ["Credential Access"],
      "technique": ["Brute Force"]
    },
    "groups": ["authentication_failures", "sshd"]
  },

  "agent": {
    "id": "000",
    "name": "wazuh-server",
    "ip": "127.0.0.1"
  },

  "data": {
    "srcip": "192.168.1.100",
    "dstuser": "root",
    "program_name": "sshd"
  },

  "full_log": "Dec 10 02:15:33 server sshd[1234]: Failed password for root from 192.168.1.100 port 44123 ssh2"
}

--

# Níveis de Alerta

| Nível | Significado/Severidade | Ação a ser realizada |
|----------:|--------|------------|
| 1 - 3 | Informacional | Comportamento normal do sistema|
| 4 - 6 | Baixo | Anotar e revisar comportamento |
| 7 - 9 | Médio | Investigar e documentar |
| 10 - 12 | Alto | Investigar Imediatamente, escalar ao L2(time superior) se reportado como verdadeiro |
| 13 - 15 | Critico| Escalação Imediata |
