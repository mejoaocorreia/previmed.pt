# Skill: Task Brief Builder

<!--
NOTA EXPLICATIVA PARA HUMANOS:
Esta skill transforma pedidos naturais, vagos, longos ou misturados do
utilizador em briefings claros para o Supervisor, agentes, Code ou Codex.

Não muda a intenção original do utilizador.
Apenas organiza o pedido em campos claros.
-->

Objetivo:
Transformar pedidos naturais, vagos, longos ou misturados do utilizador em
briefings claros para o Supervisor, agentes, Code ou Codex.

Regra base:
Esta skill não muda a intenção do utilizador. Apenas organiza o pedido.

---

## Quando usar

Usar quando o pedido for:

- vago;
- longo;
- multi-área;
- sensível;
- relacionado com ficheiros;
- relacionado com execução;
- relacionado com WordPress;
- relacionado com SEO;
- relacionado com dados;
- relacionado com agentes/skills/commands;
- pedido para Code/Codex/Claude Code;
- tarefa que pode precisar de validação ou rollback.

---

## Quando não usar

Não usar para:

- perguntas simples;
- nomes de commits;
- correção de frases;
- explicações curtas;
- pedidos sem risco e sem execução.

---

## Processo

1. Ler o pedido bruto.
2. Identificar objetivo real.
3. Distinguir planning mode vs implementation mode.
4. Identificar áreas envolvidas.
5. Classificar risco.
6. Identificar dados pessoais/sensíveis.
7. Identificar produção/credenciais/comandos/connectors.
8. Definir escopo.
9. Definir fora de escopo.
10. Escolher agente/skill/command.
11. Definir output esperado.
12. Definir critérios de aceitação.
13. Indicar se precisa de record/log.
14. Criar Brief Decision Note curta quando útil.

---

## Output obrigatório

Usar este formato:

```md
# Task Brief

## Objective
...

## Mode
[Planning / Implementation]

## Areas
...

## Recommended Agent
...

## Supporting Skills / Commands
...

## Risk Level
[Low / Medium / High / Critical]

## Context Needed
...

## Context Not Needed
...

## Scope
...

## Out of Scope
...

## Relevant Files
...

## Tools Allowed
...

## Tools Forbidden
...

## Expected Output
...

## Acceptance Criteria
...

## Records / Logs
[None / CURRENT_TASK / decision log / sensitive data log / audit report]

## Brief Decision Note
Escolhi `[opção]` porque `[motivo breve]`.
Não escolhi `[alternativa]` porque `[motivo breve]`.
```

---

## Regras

1. Não inventar contexto. Se faltar informação, deixar campo vazio ou pedir.
2. Não mudar a intenção original do utilizador.
3. Não transformar pedido de planeamento em implementação sem confirmação.
4. Não pedir esclarecimento se existir suposição segura razoável — assumir o
   mínimo seguro e dizê-lo explicitamente no briefing.
5. Pedir esclarecimento apenas quando faltar informação crítica
   (objetivo, escopo, risco, dados envolvidos, ambiente).
6. Aplicar System Safety quando houver dados pessoais, dados de saúde,
   credenciais ou informação confidencial.
7. Parar e pedir autorização explícita em produção, credenciais ou
   comandos destrutivos.
8. Evitar burocracia em tarefas pequenas — para pedidos triviais, não
   produzir briefing completo.

---

## Exemplos

### Exemplo 1 — Pedido vago

Pedido bruto:
"Melhora o site."

Briefing curto:

```md
# Task Brief

## Objective
Identificar pontos de melhoria no site (visual, SEO ou conteúdo) sem alterar
ficheiros ainda.

## Mode
Planning

## Areas
Visual Experience & Accessibility, SEO Growth System

## Recommended Agent
Supervisor (em Planning Mode)

## Risk Level
Low

## Scope
Diagnóstico de páginas-chave.

## Out of Scope
Implementação, alterações em produção, mexer em WordPress.

## Expected Output
Lista priorizada de melhorias possíveis.

## Acceptance Criteria
3–5 áreas concretas, com justificação curta.

## Brief Decision Note
Escolhi Planning Mode porque o pedido é genérico.
Não escolhi Implementation porque ainda não há decisão de o que alterar.
```

### Exemplo 2 — Pedido multi-área

Pedido bruto:
"Revê SEO, visual e WordPress da homepage."

Ação:
Dividir por áreas e produzir 3 briefings curtos (um para `SEO Growth System`,
um para `Visual Experience & Accessibility`, um para `WordPress Engineering`),
com escopo limitado à homepage e regra explícita de "não alterar produção".

### Exemplo 3 — Pedido sensível

Pedido bruto:
"Analisa esta lista de trabalhadores."

Ação:
**Parar antes de criar briefing.** Aplicar GDPR Access Gate do
System Safety & Data Protection. O briefing só é construído depois da
autorização explícita e dentro dos limites aprovados.

### Exemplo 4 — Pedido para Code

Pedido bruto:
"Cria três ficheiros vazios em `.claude/skills/foo/`."

Briefing curto:

```md
# Task Brief

## Objective
Criar 3 ficheiros vazios em `.claude/skills/foo/`.

## Mode
Implementation

## Areas
Agent Architecture & Delegation

## Recommended Agent
Code (execução direta)

## Risk Level
Low

## Scope
Apenas criar os 3 ficheiros no caminho indicado.

## Out of Scope
Editar outros ficheiros, mexer em WordPress, instalar nada.

## Tools Allowed
Filesystem write dentro de `.claude/skills/foo/`.

## Tools Forbidden
Tudo fora do caminho.

## Acceptance Criteria
3 ficheiros existem, vazios, no caminho correto.
```

---

## Ficheiros relacionados

- [[REQUEST_INTAKE_MODEL]] — [REQUEST_INTAKE_MODEL.md](../../../project/agent-architecture/REQUEST_INTAKE_MODEL.md)
- [[TASK_ROUTING_MATRIX]] — [TASK_ROUTING_MATRIX.md](../../../project/agent-architecture/TASK_ROUTING_MATRIX.md)
- [[SUBAGENT_BRIEFING_PROTOCOL]] — [SUBAGENT_BRIEFING_PROTOCOL.md](../../../project/agent-architecture/SUBAGENT_BRIEFING_PROTOCOL.md)
- [[PROMPT_QUALITY_RUBRIC]] — [PROMPT_QUALITY_RUBRIC.md](../../../project/agent-architecture/PROMPT_QUALITY_RUBRIC.md)
