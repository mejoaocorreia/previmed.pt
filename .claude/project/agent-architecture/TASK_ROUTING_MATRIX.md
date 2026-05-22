# Task Routing Matrix

<!--
NOTA EXPLICATIVA PARA HUMANOS:
Este ficheiro ajuda o Supervisor a escolher a área, agente, skill ou command
certo para cada tipo de pedido.

A matriz não substitui o julgamento do Supervisor.
Serve para evitar escolhas inconsistentes em pedidos semelhantes.
-->

Objetivo:
Ajudar o Supervisor a escolher a área, agente, skill ou command certo para
cada tipo de pedido.

A matriz não substitui o julgamento do Supervisor.
Serve para reduzir variabilidade e evitar escolhas inconsistentes.

---

## Matriz principal

| Tipo de pedido | Área principal | Agente recomendado | Skill/Command recomendado | Risco típico | Quando escalar | Output esperado |
|---|---|---|---|---|---|---|
| Segurança / RGPD / dados pessoais | System Safety & Data Protection | `security-review` ou `data-protection-review` | `data-access-gate` / `risk-classification` | médio a crítico | dados de saúde, produção, credenciais, envio externo | gate, risco, autorização necessária |
| SEO estratégico / crescimento | SEO Growth System | `seo-lead` | `seo-quality-gate` | médio | alterações a slugs, redirects, schema, sitemap, produção | diagnóstico, prioridades, riscos |
| SEO técnico | SEO Growth System | `technical-seo` | `seo-quality-gate` | médio a alto | indexação, redirects, canonical, schema global | technical SEO review |
| Conteúdo / copy / páginas de serviço | SEO Growth System | `content-growth` | `content-quality-review` | baixo a médio | claims legais, saúde, certificações, conteúdo sensível | estrutura, melhorias, riscos |
| Concorrência / SERP | SEO Growth System | `competitor-research` | `competitor-scan` | baixo | dados pagos/ferramentas externas | gaps, oportunidades, padrões |
| WordPress técnico | WordPress Engineering | `wordpress-engineering` | `wordpress-safety-check` (se existir) | médio a alto | functions.php, plugins, produção, base de dados | plano técnico, ficheiros, validação |
| Visual / layout / experiência premium | Visual Experience & Accessibility | `visual-quality` ou `visual-experience` | `visual-review` (se existir) | baixo a médio | alterações globais, performance, accessibility | revisão visual, recomendações |
| Acessibilidade | Visual Experience & Accessibility | `accessibility` ou `visual-quality` | `accessibility-check` (se existir) | médio | componentes globais, navegação, formulários | problemas e correções |
| Prompt / briefing / agentes / skills | Agent Architecture & Delegation | `prompt-agent-architect` | `task-brief-builder` / `prompt-quality-review` / `subagent-briefing` | baixo a médio | alterações ao Supervisor ou estrutura central | briefing, prompt melhorado, recomendação |
| Tarefa longa / vários ficheiros | Execution Workflows | `supervisor` / execution workflow | `task-continuity` (se existir) | médio a alto | risco alto, execução por lotes, rollback | plano por fases, current task, checkpoints |
| Pedido ambíguo | Agent Architecture & Delegation | `prompt-agent-architect` ou Supervisor | `task-brief-builder` | variável | se houver risco médio/alto | briefing ou pergunta de clarificação |
| Comandos / permissões | System Safety & Data Protection | `security-review` | `command-risk-review` | médio a crítico | comandos destrutivos, produção, credenciais | aprovar, bloquear ou pedir autorização |
| Connectors / MCPs | System Safety & Data Protection | `security-review` | `risk-classification` | médio a crítico | dados pessoais, write access, execute access | permissão, escopo, limites |
| Documentação / records | Execution Workflows ou Agent Architecture | Supervisor | `task-brief-builder` (se necessário) | baixo | dados sensíveis em logs | ficheiro atualizado, resumo, localização |

---

## Regra de desempate

Se houver dúvida entre duas áreas, escolher a área de maior risco primeiro.

Exemplos:

- **SEO + produção** → System Safety primeiro, depois CEO Growth.
- **WordPress + dados pessoais** → System Safety primeiro, depois WordPress Engineering.
- **Visual + performance** → Visual Experience com validação de performance.

Razão:
Reverter um erro de SEO ou visual é mais barato do que reverter uma fuga de
dados, uma quebra de produção ou um comando destrutivo.

---

## Ficheiros relacionados

- [[REQUEST_INTAKE_MODEL]] — [REQUEST_INTAKE_MODEL.md](./REQUEST_INTAKE_MODEL.md)
- [[SUBAGENT_BRIEFING_PROTOCOL]] — [SUBAGENT_BRIEFING_PROTOCOL.md](./SUBAGENT_BRIEFING_PROTOCOL.md)
- [[SUPERVISOR_REVIEW_PROTOCOL]] — [SUPERVISOR_REVIEW_PROTOCOL.md](./SUPERVISOR_REVIEW_PROTOCOL.md)
- [[PROMPT_QUALITY_RUBRIC]] — [PROMPT_QUALITY_RUBRIC.md](./PROMPT_QUALITY_RUBRIC.md)
- [[TOKEN_EFFICIENCY_RULES]] — [TOKEN_EFFICIENCY_RULES.md](./TOKEN_EFFICIENCY_RULES.md)
