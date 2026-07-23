# Arquitetura do Laboratório

## Objetivo

Implementar um firewall utilizando o pfSense para controlar o tráfego entre uma rede interna e a Internet.

## Componentes

- Host Windows 11
- Oracle VirtualBox
- Ubuntu Server (Wazuh)
- pfSense
- Wazuh Agent

## Fluxo

Internet
↓

pfSense

↓

Rede LAN

↓

Windows

↓

Wazuh Agent

↓

Wazuh Manager

## Objetivos do laboratório

- Aprender conceitos de firewall.
- Criar regras de bloqueio.
- Criar regras de permissão.
- Gerar logs.
- Integrar posteriormente ao Wazuh.