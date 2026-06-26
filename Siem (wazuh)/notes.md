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
