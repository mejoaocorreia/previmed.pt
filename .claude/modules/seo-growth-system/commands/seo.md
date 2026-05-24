---
description: SEO Growth System - auditorias, conteudo, tecnico, schema, local, performance, AI search (por modos)
argument-hint: [audit|technical|content|brief|keywords|local|schema|competitor|data|performance|ai-search|wordpress|go-live|qa]
---

# Command: /seo

Comando único de entrada do module **SEO Growth System**. Em vez de um ficheiro por microação, há **um comando com modos**.

## Como funciona
1. O comando encaminha sempre para o **SEO Lead** ([`../agents/seo-lead.md`](../agents/seo-lead.md)).
2. O SEO Lead lê o modo, decide os subagentes/skills/project docs e coordena.
3. Em trabalhos importantes, passa por **SEO QA** antes de entregar.
4. Análises grandes são persistidas como records (ver [`../project/REPORTING_MODEL.md`](../project/REPORTING_MODEL.md); templates em [`../records-templates/`](../records-templates/README.md)).

## Execução paralela (orquestração no topo)
Este comando corre ao **nível do agente principal**. É **aqui** que se faz o fan-out paralelo:
- Adota o papel de **SEO Lead** (lê [`../agents/seo-lead.md`](../agents/seo-lead.md) e o "Routing interno SEO").
- Para o modo pedido, **lança em paralelo** os subagentes necessários com **várias chamadas `Task()` no mesmo turno** (ex.: no `audit` → technical-seo, content-growth, serp-competitor-analyst, seo-data-analyst, cwv-performance-seo, schema-entity em paralelo).
- Recolhe os resultados, **consolida** e corre **seo-qa** antes de entregar.
- Nota técnica: o fan-out parte **do topo**, não do subagente `seo-lead` (um subagente folha não lança outros subagentes).

> **Nomes dos subagentes (namespace do plugin):** como vêm de um plugin, o `subagent_type` é **`seo-growth-system:<nome>`** — ex.: `seo-growth-system:technical-seo`, `seo-growth-system:content-growth`, `seo-growth-system:seo-qa`. Usa **sempre o nome com prefixo**. (Se o teu Claude Code resolver nomes simples — ex.: `technical-seo` — também funciona; o prefixo é o seguro.)

## Regras transversais (todos os modos)
- Não alterar o site, WordPress, indexação ou URLs sem autorização do supervisor.
- Read-only por defeito; ferramentas pagas só com autorização.
- Distinguir evidência, hipótese e recomendação. Sem dados reais → hipótese.
- Governação (segurança, RGPD, produção, rollback) vence sempre — é do supervisor/system-safety.

## Modos

### /seo audit
- **Quando:** auditoria/revisão SEO ampla.
- **Agentes:** technical-seo, content-growth, serp-competitor-analyst, seo-data-analyst, cwv-performance-seo, schema-entity, seo-qa.
- **Skills/docs:** `technical-seo-crawl-audit`, `OPERATING_SYSTEM`, `REPORTING_MODEL`.
- **Output:** diagnóstico, evidência, prioridades, riscos, plano por fases, record datado.

### /seo technical
- **Quando:** crawl/index, canonical, redirects, sitemap, robots, render, WordPress técnico.
- **Agentes:** technical-seo (+ cwv-performance-seo, wordpress-seo-implementation se aplicável).
- **Skills/docs:** `technical-seo-crawl-audit`, `TECHNICAL_RULES`.
- **Output:** Technical SEO Review (problemas, impacto, risco, validação).

### /seo content
- **Quando:** rever/criar conteúdo, E-E-A-T, páginas de serviço, refresh.
- **Agentes:** content-growth (+ onpage-seo).
- **Skills/docs:** `seo-quality-gate`, `CONTENT_RULES`.
- **Output:** Content Growth Review (intenção, lacunas, prova, estrutura, riscos).

### /seo brief
- **Quando:** preparar um brief editorial antes de escrever.
- **Agentes:** keyword-intent, content-brief, content-growth.
- **Skills/docs:** `content-brief-generation`, `keyword-cluster-map`, `CONTENT_RULES`.
- **Output:** brief completo acionável.

### /seo keywords
- **Quando:** pesquisa/cluster de keywords e mapeamento de intenção.
- **Agentes:** keyword-intent (+ serp-competitor-analyst).
- **Skills/docs:** `keyword-cluster-map`, `serp-intent-audit`, `STRATEGY_RULES`.
- **Output:** clusters com intenção, página alvo, prioridade, risco de canibalização.

### /seo local
- **Quando:** SEO local, GBP, NAP, páginas locais.
- **Agentes:** local-seo (+ content-brief).
- **Skills/docs:** `local-seo-review`, `LOCAL_SEO_PLAYBOOK`.
- **Output:** oportunidades locais, páginas necessárias, GBP/NAP, citations.

### /seo schema
- **Quando:** dados estruturados e entidades.
- **Agentes:** schema-entity (+ technical-seo).
- **Skills/docs:** `schema-entity-review`, `SCHEMA_ENTITY_MODEL`.
- **Output:** tipos recomendados, propriedades, fonte, páginas, validação.

### /seo competitor
- **Quando:** análise de concorrência/SERP.
- **Agentes:** serp-competitor-analyst.
- **Skills/docs:** `competitor-gap-analysis`, `serp-intent-audit`, `COMPETITOR_RESEARCH_PLAYBOOK`.
- **Output:** concorrentes, padrões SERP, gaps, oportunidades, recomendação (datada).

### /seo data
- **Quando:** análise de Search Console/GA4/PageSpeed.
- **Agentes:** seo-data-analyst.
- **Skills/docs:** `gsc-ga4-analysis`, `KPI_MODEL`.
- **Output:** insight, evidência, hipótese, ação, métrica a monitorizar.

### /seo performance
- **Quando:** Core Web Vitals / performance SEO.
- **Agentes:** cwv-performance-seo (+ wordpress-seo-implementation; Visual Experience se visual).
- **Skills/docs:** `cwv-performance-seo-review`, `TECHNICAL_RULES`.
- **Output:** métrica, causa, recomendação, impacto SEO/UX, teste.

### /seo ai-search
- **Quando:** visibilidade em AI Overviews / AI Mode / GEO.
- **Agentes:** ai-search-visibility, content-growth, schema-entity.
- **Skills/docs:** `STRATEGY_RULES`, `CONTENT_RULES`.
- **Output:** perguntas-alvo, entidades, conteúdo citável, lacunas, estrutura.

### /seo wordpress
- **Quando:** implementar SEO em WordPress.
- **Agentes:** wordpress-seo-implementation, technical-seo.
- **Skills/docs:** `TECHNICAL_RULES`.
- **Output:** onde implementar, ficheiros/configs, risco, teste, rollback.

### /seo go-live
- **Quando:** preparar go-live SEO seguro.
- **Agentes:** seo-qa, technical-seo, wordpress-seo-implementation.
- **Skills/docs:** [`SEO_GO_LIVE_CHECKLIST.md`](../records-templates/SEO_GO_LIVE_CHECKLIST.md), `QUALITY_GATE`.
- **Output:** checklist validada, riscos, autorização necessária.

### /seo qa
- **Quando:** revisão final antes de entregar/publicar.
- **Agentes:** seo-qa.
- **Skills/docs:** `seo-quality-gate`, `QUALITY_GATE`.
- **Output:** aprovado/bloqueado, problemas, correções, risco residual.

## Notas de consolidação
Consolida num único comando com modos os vários comandos SEO que antes existiam separados (auditoria, conteúdo, brief, concorrência, dados, local, schema, go-live, estratégia, técnico). Este comando é fornecido pelo **plugin** e fica disponível como `/seo` após instalação. O conteúdo dos comandos antigos está preservado abaixo em "Legacy/imported command notes".


---

## Legacy/imported command notes

### From .claude/commands/seo-growth-system/seo-audit.md

# Command: seo-audit (ponte → /seo audit)

> Consolidado no comando único do module. Usar **`/seo audit`**.
> Fonte da verdade: [`.claude/modules/seo-growth-system/commands/seo.md`](../../modules/seo-growth-system/commands/seo.md) · ponte global: [`.claude/commands/seo.md`](../seo.md).

Auditoria SEO controlada → SEO Lead coordena technical-seo, content-growth, serp-competitor-analyst, seo-data-analyst, cwv-performance-seo, schema-entity, seo-qa. Não alterar site/WordPress/indexação sem autorização. Estado: merged.

### From .claude/commands/seo-growth-system/content-review.md

# Command: content-review (ponte → /seo content)

> Consolidado no comando único do module. Usar **`/seo content`** (ou `/seo brief` para briefs).
> Fonte da verdade: [`.claude/modules/seo-growth-system/commands/seo.md`](../../modules/seo-growth-system/commands/seo.md).

Revisão de conteúdo/estrutura com foco em utilidade, intenção, confiança e conversão → content-growth (+ onpage-seo), com `seo-quality-gate`. Não publicar nem inventar claims; YMYL/saúde/legal exige revisão humana. Estado: merged.

### From .claude/commands/seo-growth-system/competitor-review.md

# Command: competitor-review (ponte → /seo competitor)

> Consolidado no comando único do module. Usar **`/seo competitor`**.
> Fonte da verdade: [`.claude/modules/seo-growth-system/commands/seo.md`](../../modules/seo-growth-system/commands/seo.md).

Análise de concorrentes/SERP → serp-competitor-analyst, com `competitor-gap-analysis`/`serp-intent-audit`. Não copiar concorrentes; registar data; não assumir dados pagos sem ferramenta. Estado: merged.
