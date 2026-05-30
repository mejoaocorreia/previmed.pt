# SEO Routing Matrix

Matriz operacional para ajudar o comando [`/seo`](../commands/seo.md) e o [`seo-lead`](../agents/seo-lead.md) a escolher modo, agentes, skills, records e QA.

Esta matriz nao substitui julgamento. Serve para reduzir variabilidade em pedidos semelhantes.

---

## Regra Principal

Usar o menor fluxo que resolve o pedido com seguranca.

- Pedido pequeno -> modo rapido, sem fan-out.
- Pedido medio/grande -> especialistas relevantes.
- Pedido com risco -> consultar [`SAFETY_ESCALATION.md`](SAFETY_ESCALATION.md).
- Pedido duradouro -> criar ou recomendar record.

---

## Matriz

| Pedido | Modo | Agentes | Skills/docs | Record | QA |
|---|---|---|---|---|---|
| Auditoria completa ao site | `/seo audit` | `technical-seo`, `content-growth`, `serp-competitor-analyst`, `seo-data-analyst`, `cwv-performance-seo`, `schema-entity`, `seo-qa` | `technical-seo-crawl-audit`, `QUALITY_GATE`, `REPORTING_MODEL` | `SEO_AUDIT_TEMPLATE` | Obrigatorio |
| Revisao tecnica de indexacao | `/seo technical` | `technical-seo`, opcional `wordpress-seo-implementation` | `TECHNICAL_RULES`, `TOOLING_MODEL` | Audit/task se duradouro | Sim se houver risco |
| Rever title/meta/H1 de uma pagina | `/seo content` ou `/seo qa` | `onpage-seo` ou `seo-qa` | `onpage-optimization-pass`, `QUALITY_GATE` | Nao, salvo impacto duradouro | Opcional |
| Criar brief editorial | `/seo brief` | `keyword-intent`, `content-brief`, opcional `serp-competitor-analyst` | `content-brief-generation`, `STRATEGY_RULES` | Task/report se estrategico | Sim se publicar |
| Mapear keywords e clusters | `/seo keywords` | `keyword-intent`, opcional `serp-competitor-analyst` | `keyword-cluster-map`, `serp-intent-audit` | Report/task | Opcional |
| Analise de concorrencia | `/seo competitor` | `serp-competitor-analyst` | `COMPETITOR_RESEARCH_PLAYBOOK` | Report | Opcional |
| Schema para pagina | `/seo schema` | `schema-entity`, opcional `technical-seo` | `schema-entity-review`, `SCHEMA_ENTITY_MODEL` | Task/decision se global | Sim se implementar |
| SEO local / GBP / NAP | `/seo local` | `local-seo`, opcional `schema-entity` | `LOCAL_SEO_PLAYBOOK`, `SAFETY_ESCALATION` | Report/decision | Sim se alterar GBP |
| Queda de trafego organico | `/seo data` | `seo-data-analyst`, opcional `technical-seo`, `content-growth` | `gsc-ga4-analysis`, `KPI_MODEL` | Report | Sim se recomendar mudancas |
| Core Web Vitals | `/seo performance` | `cwv-performance-seo`, opcional `technical-seo`, `wordpress-seo-implementation` | `cwv-performance-seo-review`, `TECHNICAL_RULES` | Task/report | Sim se alterar site |
| AI Search / GEO | `/seo ai-search` | `ai-search-visibility`, `content-growth`, opcional `schema-entity` | `STRATEGY_RULES`, `CONTENT_RULES` | Report/task se duradouro | Opcional |
| Implementar SEO em WordPress | `/seo wordpress` | `wordpress-seo-implementation`, `technical-seo` | `TECHNICAL_RULES`, `SAFETY_ESCALATION` | Task/decision | Obrigatorio |
| Go-live | `/seo go-live` | `seo-qa`, `technical-seo`, `wordpress-seo-implementation` | `QUALITY_GATE`, `SEO_GO_LIVE_CHECKLIST` | Go-live checklist | Obrigatorio |
| Validar recomendacao final | `/seo qa` | `seo-qa` | `seo-quality-gate`, `QUALITY_GATE` | Nao, salvo bloqueio duradouro | N/a |

---

## Modo Rapido Vs Modo Profundo

### Modo rapido

Usar para:

- rever title/meta/H1;
- classificar intencao simples;
- validar uma recomendacao isolada;
- sugerir CTA;
- identificar risco obvio;
- responder sem dados externos.

Evitar fan-out. Devolver resposta curta com limitacoes.

### Modo profundo

Usar para:

- auditoria;
- go-live;
- migracao;
- roadmap;
- analise multi-area;
- concorrencia;
- dados GSC/GA4;
- alteracao tecnica;
- decisao duradoura.

Usar especialistas, QA e records.

---

## Regra Final

Se o pedido envolve producao, RGPD, credenciais, ferramentas pagas, WordPress admin, GBP, rollback ou dados reais, consultar [`SAFETY_ESCALATION.md`](SAFETY_ESCALATION.md) antes de executar.
