# UC-002 - Monitoramento de Login Bem Sucedido

## Objetivo

Validar se o Wazuh identifica tentativas de autenticação bem sucedidas

---

## Cenário

Foi realizado testes utilizando o comando em máquina windows Win + L. 

Após bloqueio de tela, foi fornecido a senha correta para o logon com sucesso. 

---

## Resultado Esperado

O Windows tende a registrar as tentativas de logon bem sucedidas.

O Wazuh deve identificar os eventos e alertas além de registra-los, categorizando os devidamente em sua severidade correta. 

---

## Resultado Obtido

Foram identificados eventos relacionados à autenticação realizada com sucesso. 

Rule ID:
60106

Descrição:
Windows Logon Success

Nível:
3

---

## Evidências

![Dashboard](../../images/dashboard/Agent.logs.filter%20logon%20success.JPG)

---

## Análise

As tentativas de autenticação com credenciais corretas foram registradas com sucesso pelo sistema operacional com o agente wazuh inserido. 

Os eventos foram coletados pelo wazuh, onde foi aplicado pelo mesmo a regra de correlação e gerou os alertas classificados e categorizados como nível 3. 
---

## Lições Aprendidas

Foi possível compreender o fluxo completo de geração, coleta, e correlação de eventos de autenticação com sucesso no Wazuh.