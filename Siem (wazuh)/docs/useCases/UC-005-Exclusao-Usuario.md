# UC-000 - Monitoramento de 

## Objetivo

Validar se o Wazuh identifica 

---

## Cenário

Foi realizado para a ação de exlusão o seguinte comando pelo CMD: net user "NomeDoUsuario" /delete

Para verficar os usuarios na maquina foi utilizado o comando no CMD : net user
---

## Resultado Esperado



---

## Resultado Obtido

Foram identificados eventos relacionados à: 

Rule ID:
60111

Descrição:
User account disabled or deleted

Nível:
8

---

## Evidências

Inserir:

---

## Análise



---

## Possíveis Aplicações

Esse tipo de alerta pode auxiliar na identificação de:

- Possível Ataque de negação de serviçõs (DOS). Se gerado a exclusão em massa de usuários, paralisando operações de login. 

- Possível Ataque interno sobre a exclusão de contas críticas para o negócios (Como contas administradoras ou contas de serviço), interrompendo assim as operções em seu fluxo natural.

- Possível queima de arquivos ou eliminação de evidências de atacantes sobre ações indevidas realizadas ou sobre possíveis ataques realizados. Dificultando assim o fluxo de investigação sobre os eventos gerados anteriormente. 

---

## Lições Aprendidas

Foi possível compreender 