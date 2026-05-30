# Project Docs — SEO Growth System

Regras, operating system e playbooks do module. Estes ficheiros sao a **fonte de detalhe operacional** que agentes, skills e o comando [`/seo`](../commands/seo.md) consultam.

Project docs nao sao agentes e nao executam acoes. Definem standards, limites, gates e criterios de decisao.

---

## Fontes De Verdade Por Area

| Area | Fonte principal | Quando consultar | Componentes que dependem |
|---|---|---|---|
| Operating model | [`OPERATING_SYSTEM.md`](OPERATING_SYSTEM.md) | fluxo geral, handoff, priorizacao, persistencia | `/seo`, `seo-lead`, todos os agentes |
| Estrategia | [`STRATEGY_RULES.md`](STRATEGY_RULES.md) | page types, clusters, intencao, roadmap, AI Search, criar/consolidar/remover paginas | `seo-lead`, `keyword-intent`, `content-growth`, `internal-linking`, `ai-search-visibility` |
| Tecnica | [`TECHNICAL_RULES.md`](TECHNICAL_RULES.md) | crawl, indexacao, URLs, robots, sitemap, canonical, redirects, WordPress tecnico | `technical-seo`, `wordpress-seo-implementation`, `seo-qa` |
| Conteudo | [`CONTENT_RULES.md`](CONTENT_RULES.md) | E-E-A-T, claims, estrutura, refresh, conteudo AI-assisted | `content-growth`, `content-brief`, `onpage-seo`, `seo-qa` |
| Quality gate | [`QUALITY_GATE.md`](QUALITY_GATE.md) | aprovar, bloquear, pedir dados/autorizacao, go-live | `seo-qa`, `seo-quality-gate`, `/seo` |
| Tooling | [`TOOLING_MODEL.md`](TOOLING_MODEL.md) | ferramentas, MCPs, autorizacoes, dados pagos/autenticados | todos os agentes com ferramentas |
| Reporting | [`REPORTING_MODEL.md`](REPORTING_MODEL.md) | records, relatorios, status, backlog, decisions | `seo-lead`, `seo-data-analyst`, records templates |
| KPIs | [`KPI_MODEL.md`](KPI_MODEL.md) | medicao, KPI por fase, limites dos dados | `seo-data-analyst`, `seo-lead` |
| Schema/entity | [`SCHEMA_ENTITY_MODEL.md`](SCHEMA_ENTITY_MODEL.md) | structured data, entidades, sameAs, NAP | `schema-entity`, `technical-seo`, `local-seo` |
| Local SEO | [`LOCAL_SEO_PLAYBOOK.md`](LOCAL_SEO_PLAYBOOK.md) | GBP, NAP, paginas locais, areas de servico | `local-seo`, `schema-entity`, `seo-qa` |
| Concorrencia/SERP | [`COMPETITOR_RESEARCH_PLAYBOOK.md`](COMPETITOR_RESEARCH_PLAYBOOK.md) | concorrentes, gaps, SERP features, AI Overviews observaveis | `serp-competitor-analyst`, `keyword-intent`, `content-brief` |
| Routing | [`ROUTING_MATRIX.md`](ROUTING_MATRIX.md) | escolher modo, agentes, skills, record e QA | `/seo`, `seo-lead` |
| Safety escalation | [`SAFETY_ESCALATION.md`](SAFETY_ESCALATION.md) | producao, RGPD, credenciais, ferramentas pagas, WordPress admin, rollback | todos os agentes |
| MCP capabilities | [`MCP_CAPABILITIES.md`](MCP_CAPABILITIES.md) | mapear ferramentas reais disponiveis no projeto consumidor | `/seo`, `TOOLING_MODEL`, todos os agentes |

---

## Como Ler Por Tipo De Pedido

- Auditoria ampla: `OPERATING_SYSTEM` -> `STRATEGY_RULES` -> `TECHNICAL_RULES` / `CONTENT_RULES` -> `QUALITY_GATE` -> `REPORTING_MODEL`.
- SEO tecnico: `TECHNICAL_RULES` -> `TOOLING_MODEL` -> `QUALITY_GATE`.
- Conteudo/brief: `STRATEGY_RULES` -> `CONTENT_RULES` -> `COMPETITOR_RESEARCH_PLAYBOOK` -> `QUALITY_GATE`.
- Keywords/clusters: `STRATEGY_RULES` -> `KPI_MODEL` -> `COMPETITOR_RESEARCH_PLAYBOOK`.
- Schema: `SCHEMA_ENTITY_MODEL` -> `TECHNICAL_RULES` -> `QUALITY_GATE`.
- Local SEO: `LOCAL_SEO_PLAYBOOK` -> `SCHEMA_ENTITY_MODEL` -> `QUALITY_GATE`.
- Performance: `TECHNICAL_RULES` -> `TOOLING_MODEL` -> `KPI_MODEL`.
- Dados/reporting: `KPI_MODEL` -> `REPORTING_MODEL` -> `TOOLING_MODEL`.
- Go-live: `QUALITY_GATE` -> `TECHNICAL_RULES` -> records template `SEO_GO_LIVE_CHECKLIST`.
- Pedido ambiguo: `ROUTING_MATRIX` -> `OPERATING_SYSTEM` -> `QUALITY_GATE`.
- Pedido com risco: `SAFETY_ESCALATION` -> `QUALITY_GATE` -> Supervisor/System Safety.

---

## Ordem De Leitura Recomendada Por Agente

- `technical-seo` -> `TECHNICAL_RULES` + `TOOLING_MODEL` + `QUALITY_GATE`.
- `content-growth` -> `CONTENT_RULES` + `STRATEGY_RULES` + `QUALITY_GATE`.
- `content-brief` -> `STRATEGY_RULES` + `CONTENT_RULES` + `COMPETITOR_RESEARCH_PLAYBOOK`.
- `keyword-intent` -> `STRATEGY_RULES` + `KPI_MODEL` + `COMPETITOR_RESEARCH_PLAYBOOK`.
- `serp-competitor-analyst` -> `COMPETITOR_RESEARCH_PLAYBOOK` + `TOOLING_MODEL`.
- `schema-entity` -> `SCHEMA_ENTITY_MODEL` + `TECHNICAL_RULES` + `QUALITY_GATE`.
- `local-seo` -> `LOCAL_SEO_PLAYBOOK` + `SCHEMA_ENTITY_MODEL` + `SAFETY_ESCALATION`.
- `cwv-performance-seo` -> `TECHNICAL_RULES` + `TOOLING_MODEL` + `KPI_MODEL`.
- `seo-data-analyst` -> `KPI_MODEL` + `TOOLING_MODEL` + `REPORTING_MODEL`.
- `ai-search-visibility` -> `STRATEGY_RULES` + `CONTENT_RULES` + `COMPETITOR_RESEARCH_PLAYBOOK`.
- `wordpress-seo-implementation` -> `TECHNICAL_RULES` + `SAFETY_ESCALATION` + `QUALITY_GATE`.
- `seo-qa` -> `QUALITY_GATE` + `SAFETY_ESCALATION` + docs da area em revisao.

---

## Regras De Uso

- Estes docs sao **genericos e exportaveis**.
- Dados especificos de um projeto consumidor ficam no workspace/records desse projeto, nao aqui.
- Nao guardar credenciais, tokens, dados pessoais ou dados sensiveis nestes ficheiros.
- Nao repetir referencias externas em todos os docs; referencias base ficam no [README do module](../README.md).
- Quando houver conflito entre SEO e seguranca/RGPD/producao/rollback, vence o Supervisor/System Safety.

---

## Estado Atual

Project docs operacionais para a v1.1 do module.
