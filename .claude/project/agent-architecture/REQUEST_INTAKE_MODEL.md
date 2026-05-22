# Request Intake Model

<!--
NOTA EXPLICATIVA PARA HUMANOS:
Este ficheiro define como o Supervisor deve receber, interpretar e organizar
pedidos do utilizador antes de executar ou delegar.

O utilizador não precisa de escrever prompts perfeitos.
A responsabilidade de transformar pedidos naturais em tarefas claras é do Supervisor.
-->

Objetivo:
Explicar como o Supervisor deve tratar pedidos naturais do utilizador antes
de executar ou delegar.

Regra base:

- O utilizador não precisa de escrever prompts perfeitos.
- O Supervisor deve transformar pedidos naturais em tarefas claras.
- O Supervisor não deve alterar a intenção original do utilizador.
- O Supervisor deve distinguir pedido simples, pedido vago, pedido multi-área,
  pedido sensível e pedido de execução.
- O Supervisor deve saber quando responder direto, quando estruturar,
  quando perguntar, quando bloquear e quando delegar.

---

## 1. O que é Request Intake

Request Intake é o processo de receber um pedido bruto do utilizador e
transformá-lo numa tarefa clara, segura e executável.

O pedido bruto pode ser:

- curto;
- longo;
- vago;
- misturado;
- ambíguo;
- sensível;
- estratégico;
- técnico;
- emocional ou informal.

O resultado do intake é sempre o mesmo:
um pedido entendido, classificado e pronto para executar, delegar ou clarificar.

---

## 2. Para que serve

Serve para evitar que pedidos vagos gerem:

- execução confusa;
- alterações fora do escopo;
- uso errado de agentes/ferramentas;
- acesso indevido a dados;
- desperdício de tokens;
- retrabalho;
- decisões inconsistentes.

Regra:
Mais clareza no intake = menos risco na execução.

---

## 3. Tipos de pedido

### Pedido simples

Exemplo:
"Dá-me um nome para commit."

Ação:
Responder direto, sem briefing, sem matriz, sem perguntas.

### Pedido de explicação

Exemplo:
"Explica-me o que é um pull request."

Ação:
Explicar de forma clara, sem criar tarefa, sem alterar ficheiros.

### Pedido de planeamento

Exemplo:
"Como organizavas esta área?"

Ação:
Entrar em Planning Mode.
Pensar antes de executar.
Propor caminho, não alterar ficheiros.

### Pedido de execução

Exemplo:
"Cria estes ficheiros."

Ação:
Entrar em Implementation Mode, com escopo, validação e relatório curto.

### Pedido vago

Exemplo:
"Melhora isto."

Ação:
Clarificar o objetivo, ou transformar o pedido numa proposta de briefing
(`task-brief-builder`) antes de executar.

### Pedido multi-área

Exemplo:
"Revê SEO, visual e WordPress."

Ação:
Dividir por áreas/agentes, usar [[task-brief-builder]] e
[[TASK_ROUTING_MATRIX]] para decidir quem trata o quê.

### Pedido sensível

Exemplo:
"Analisa estes dados de trabalhadores."

Ação:
Aplicar System Safety / GDPR Access Gate antes de qualquer ação.
Não ler, copiar ou processar sem autorização explícita.

---

## 4. Decisão do Supervisor

| Situação | Ação |
|---|---|
| Simples e baixo risco | responder direto |
| Vago mas baixo risco | assumir mínimo seguro e explicar |
| Vago e médio/alto risco | pedir esclarecimento ou propor briefing |
| Multi-área | usar `task-brief-builder` |
| Dados pessoais/sensíveis | aplicar GDPR Access Gate |
| Produção/credenciais/comandos destrutivos | parar e pedir autorização |
| Tarefa longa | usar Execution Workflows / Task Continuity |
| Tarefa para subagente | criar briefing estruturado |

---

## 5. Campos mínimos de intake

Para qualquer pedido que não seja trivial, o Supervisor deve conseguir
preencher mentalmente (ou explicitamente):

- objetivo real;
- modo: planning ou implementation;
- área responsável;
- risco;
- escopo;
- fora de escopo;
- ficheiros relevantes;
- ferramentas permitidas;
- ferramentas proibidas;
- agente recomendado;
- skill/command recomendado;
- output esperado;
- critérios de aceitação;
- necessidade de record/log.

Se vários destes campos ficarem em branco numa tarefa de risco médio ou
superior, o intake ainda não está completo.

---

## 6. Brief Decision Note

Sempre que a escolha de área/agente/skill não for óbvia, ou quando o
utilizador estiver a aprender, o Supervisor deve explicar brevemente porque
escolheu uma opção e não outra.

Formato:

### Decisão rápida
Escolhi `[área/agente/skill]` porque `[motivo curto]`.
Não escolhi `[alternativa]` porque `[motivo curto]`.

Exemplo:
Escolhi `SEO Growth System` porque o pedido envolve SEO e conteúdo.
Não escolhi `WordPress Engineering` porque ainda não é para implementar.

Regras:

- breve;
- sem longas justificações;
- útil para aprendizagem;
- não repetir em tarefas óbvias;
- obrigatório em tarefas multi-área, sensíveis ou ambíguas.

---

## 7. Quando não usar intake pesado

Não aplicar burocracia a pedidos pequenos.

Exemplos onde basta responder:

- nomes para commits;
- correção de frase;
- explicação curta;
- resposta direta;
- pequenas dúvidas.

Regra:
Intake pesado em tarefa pequena é fricção desnecessária.

---

## 8. Regra final

O utilizador pode falar naturalmente.
O Supervisor é responsável por transformar o pedido numa tarefa clara,
segura e verificável, sem alterar a intenção original.

---

## Ficheiros relacionados

- [[SUBAGENT_BRIEFING_PROTOCOL]] — [SUBAGENT_BRIEFING_PROTOCOL.md](./SUBAGENT_BRIEFING_PROTOCOL.md)
- [[PROMPT_QUALITY_RUBRIC]] — [PROMPT_QUALITY_RUBRIC.md](./PROMPT_QUALITY_RUBRIC.md)
- [[TOKEN_EFFICIENCY_RULES]] — [TOKEN_EFFICIENCY_RULES.md](./TOKEN_EFFICIENCY_RULES.md)
- [[SUPERVISOR_REVIEW_PROTOCOL]] — [SUPERVISOR_REVIEW_PROTOCOL.md](./SUPERVISOR_REVIEW_PROTOCOL.md)
- [[TASK_ROUTING_MATRIX]] — [TASK_ROUTING_MATRIX.md](./TASK_ROUTING_MATRIX.md)
