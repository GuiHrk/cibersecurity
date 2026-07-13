# UC-001- Monitoramento de falhas de autenticação

## Objetivo

Validar se o SIEM Wazuh identifica tentativas de autenticação de usuário malsucedidas no endpoint de teste Widnows. 

---

## Cenário

Realizado o bloqueio da máquina por meio do comando Win + L; 

Em seguida, propositalmente foram realiadas algumas tentativa de autenticação utilizando uma senha incorreta. 

---

## Resultado Esperado

O Windows tem de registrar os eventos de falhas de autenticação. 

O Wazuh deve coletar esses eventos e gerar os alertas. 

---

## Resultados Obtidos

Foram coletados eventos relacionados ao teste de autenticação falho propositalmente. 

Rule ID:
60122

Descrição: 
Logon Failure - Unknown user or bad password

Nível:
5

## Evidências 

![Dashboard](../../images/dashboard/Agent.logs.filter%20failure%20logon.JPG)

![Dashboard](../../images/dashboard/Agent%20logs.JPG)

## Análise 

As tentativas falhas de autenticação foram registradas com sucesso pelo sistema operacional com o agente wazuh inserido. 

Os eventos foram coletados pelo wazuh, onde foi aplicado pelo mesmo a regra de correlação e gerou os alertas classificados e categorizados como nível 5. 

## Aplicações 
Esse tipo de alerta pode auxiliar na identiciação de: 

- Tentativas de força bruta
- Uso de credenciais inválidas
- Erros operacionais do usuário
- Ataques de password Spraying

---

## Aprendizado

Foi possível compreender o fluxo completo de geração, coleta, e correlação de eventos de autenticação falha no Wazuh. 


