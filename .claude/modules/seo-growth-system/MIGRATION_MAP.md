# Migration Map — SEO Growth System

Mapa origem→destino de tudo o que foi migrado/consolidado para o module, a partir do **ativo** (`.claude/.../seo-growth-system/` e ficheiros SEO soltos) e do **`_archive`** (`_archive/2026-05-20__pre-redesign/.../organic-growth/` e o archive antigo).

> **Garantia:** o `.claude/_archive/` **não foi apagado nem alterado** — foi usado apenas como leitura/comparação. Nada de importante foi perdido: o que não foi materializado como ficheiro está mapeado abaixo como `covered_by_*` ou `deferred`.

## Estados
`migrated` (movido tal-qual, generalizado) · `merged` (fundido de várias fontes) · `covered_by_project_doc` · `covered_by_skill` · `covered_by_agent` · `deferred` (capacidade reconhecida, não materializada agora) · `not_applicable` (dados específicos do projeto, ficam no archive/records).

## Agents

| Origem | Destino | Estado | Notas |
|---|---|---|---|
| ativo `agents/seo-growth-system/seo-lead.md` | `agents/seo-lead.md` | merged | + archive seo-lead (equipa, priorização, WordPress). Ativo virou ponte. |
| archive `agents/organic-growth/seo-lead.md` | `agents/seo-lead.md` | merged | Estrutura de equipa, matriz quick-wins. |
| ativo `agents/seo-growth-system/technical-seo.md` | `agents/technical-seo.md` | merged | + archive technical-seo. Ativo virou ponte. |
| archive `agents/organic-growth/technical-seo.md` | `agents/technical-seo.md` | merged | Lista de responsabilidades. |
| ativo `agents/seo-growth-system/content-growth.md` | `agents/content-growth.md` | merged | + archive onpage/content. Ativo virou ponte. |
| ativo `agents/seo-growth-system/competitor-research.md` | `agents/serp-competitor-analyst.md` | merged | Renomeado; + archive serp-competitor-analyst. Ativo virou ponte. |
| archive `agents/organic-growth/serp-competitor-analyst.md` | `agents/serp-competitor-analyst.md` | merged | SERP features, tipos de página. |
| archive `agents/organic-growth/keyword-intent.md` | `agents/keyword-intent.md` | migrated | Capacidade que faltava no ativo. |
| archive `agents/organic-growth/content-brief.md` | `agents/content-brief.md` | migrated | + comando content-brief do archive. |
| archive `agents/organic-growth/onpage-seo.md` | `agents/onpage-seo.md` | migrated | — |
| archive `agents/organic-growth/internal-linking.md` | `agents/internal-linking.md` | migrated | — |
| archive `agents/organic-growth/schema-entity.md` | `agents/schema-entity.md` | merged | + playbook SCHEMA_ENTITY_MODEL. |
| archive `agents/organic-growth/local-seo.md` | `agents/local-seo.md` | merged | + playbook LOCAL_PLAYBOOK. |
| archive `agents/organic-growth/seo-data-analyst.md` | `agents/seo-data-analyst.md` | migrated | + comando gsc-analysis. |
| archive `agents/organic-growth/cwv-performance-seo.md` | `agents/cwv-performance-seo.md` | migrated | — |
| archive `agents/organic-growth/ai-search-visibility.md` | `agents/ai-search-visibility.md` | migrated | — |
| archive `agents/organic-growth/wordpress-seo-implementation.md` | `agents/wordpress-seo-implementation.md` | migrated | Articula com project/wordpress-engineering. |
| archive `agents/organic-growth/seo-qa.md` | `agents/seo-qa.md` | merged | + skill ativa seo-quality-gate. |
| archive `agents/organic-growth/README.md` | `README.md` + `seo-lead` (routing) | merged | Índice/escopo da equipa. |

## Commands

| Origem | Destino | Estado | Notas |
|---|---|---|---|
| ativo `commands/seo-growth-system/seo-audit.md` | `commands/seo.md` (modo `audit`) | merged | Ativo virou ponte → `/seo audit`. |
| ativo `commands/seo-growth-system/content-review.md` | `commands/seo.md` (modo `content`) | merged | Ponte → `/seo content`. |
| ativo `commands/seo-growth-system/competitor-review.md` | `commands/seo.md` (modo `competitor`) | merged | Ponte → `/seo competitor`. |
| archive `commands/organic-growth/competitor-analysis.md` | `commands/seo.md` (`competitor`) | merged | — |
| archive `commands/organic-growth/content-brief.md` | `commands/seo.md` (`brief`) | merged | — |
| archive `commands/organic-growth/gsc-analysis.md` | `commands/seo.md` (`data`) | merged | — |
| archive `commands/organic-growth/local-seo.md` | `commands/seo.md` (`local`) | merged | — |
| archive `commands/organic-growth/page-review.md` | `commands/seo.md` (`content`/`technical`) | merged | — |
| archive `commands/organic-growth/schema-review.md` | `commands/seo.md` (`schema`) | merged | — |
| archive `commands/organic-growth/seo-go-live.md` | `commands/seo.md` (`go-live`) | merged | + records_template/SEO_GO_LIVE_CHECKLIST. |
| archive `commands/organic-growth/seo-strategy.md` | `commands/seo.md` (`keywords`/`audit`) | merged | — |
| archive `commands/organic-growth/technical-audit.md` | `commands/seo.md` (`technical`) | merged | — |
| (novo) | `.claude/commands/seo.md` | migrated | Ponte global nativa para o module. |

## Project docs

| Origem | Destino | Estado | Notas |
|---|---|---|---|
| ativo `project/seo-growth-system/SEO_GROWTH_OPERATING_SYSTEM.md` | `project/OPERATING_SYSTEM.md` | merged | + archive _system/OPERATING_SYSTEM (anti-token-waste). |
| ativo `project/seo-growth-system/SEO_STRATEGY_RULES.md` | `project/STRATEGY_RULES.md` | merged | + archive strategy (generalizado). |
| ativo `project/seo-growth-system/TECHNICAL_SEO_RULES.md` | `project/TECHNICAL_RULES.md` | merged | + archive playbook TECHNICAL_AUDIT. |
| ativo `project/seo-growth-system/CONTENT_GROWTH_RULES.md` | `project/CONTENT_RULES.md` | merged | + archive CONTENT_SYSTEM + QUALITY_BAR. |
| ativo `project/seo-growth-system/COMPETITOR_RESEARCH_PROTOCOL.md` | `project/COMPETITOR_RESEARCH_PLAYBOOK.md` | merged | + archive playbook COMPETITOR_RESEARCH. |
| ativo `project/seo-growth-system/GROWTH_QUALITY_GATE.md` | `project/QUALITY_GATE.md` | merged | + skill ativa + archive QUALITY_BAR. |
| archive `_system/OPERATING_SYSTEM.md` | `project/OPERATING_SYSTEM.md` + `project/REPORTING_MODEL.md` | merged | Persistence/living-vs-dated → REPORTING_MODEL. |
| archive `_system/KPI_MODEL.md` | `project/KPI_MODEL.md` | migrated | — |
| archive `_system/QUALITY_BAR.md` | `project/CONTENT_RULES.md` + `project/QUALITY_GATE.md` | merged | — |
| archive `_system/TOOLING_MCP_STACK.md` | `project/TOOLING_MODEL.md` | merged | Generalizado (decisão de orçamento Previmed → not_applicable). |
| archive `_system/GLOSSARY.md` | — | not_applicable | Glossário Previmed-específico; fica no archive (dados do projeto). |
| archive `_system/playbooks/SCHEMA_ENTITY_MODEL.md` | `project/SCHEMA_ENTITY_MODEL.md` | merged | — |
| archive `_system/playbooks/LOCAL_PLAYBOOK.md` | `project/LOCAL_SEO_PLAYBOOK.md` | merged | — |
| archive `_system/playbooks/COMPETITOR_RESEARCH.md` | `project/COMPETITOR_RESEARCH_PLAYBOOK.md` | merged | — |
| archive `_system/playbooks/CONTENT_SYSTEM.md` | `project/CONTENT_RULES.md` | merged | — |
| archive `_system/playbooks/TECHNICAL_AUDIT.md` | `project/TECHNICAL_RULES.md` + skill `technical-seo-crawl-audit` | merged | — |
| archive `strategy/*` (AUDIENCES, COMPETITORS, INFORMATION_ARCHITECTURE, KEYWORDS, STRATEGY) | `project/STRATEGY_RULES.md` (estrutura) | not_applicable (dados) | Ideias de estrutura migradas; dados Previmed ficam no archive. |
| archive `setup/*` (BASELINE_AUDIT, GSC_GA4_SETUP, KEYWORD_DATA_DECISION) | `project/TOOLING_MODEL.md` + `records_template/SEO_AUDIT_TEMPLATE.md` | covered_by_project_doc | Decisões/setup específicos ficam no archive/records. |
| archive `_living/*` (CURRENT_STATUS, BACKLOG, OPPORTUNITIES, DECISION_LOG) | `project/REPORTING_MODEL.md` (modelo vivo-vs-datado) | covered_by_project_doc | Conteúdo vivo é do projeto (records reais), não do module. |

## Skills

| Origem | Destino | Estado | Notas |
|---|---|---|---|
| ativo `skills/seo-growth-system/seo-quality-gate` | `skills/seo-quality-gate` | merged | + archive. |
| ativo `skills/seo-growth-system/competitor-scan` | `skills/competitor-gap-analysis` | merged | Renomeado/fundido. |
| ativo `skills/seo-growth-system/content-quality-review` | `skills/onpage-optimization-pass` + `project/CONTENT_RULES.md` | merged | Capacidade dividida entre skill on-page e regras de conteúdo. |
| archive `skills/organic-growth/technical-seo-crawl-audit` | `skills/technical-seo-crawl-audit` | migrated | — |
| archive `skills/organic-growth/content-brief-generation` | `skills/content-brief-generation` | migrated | — |
| archive `skills/organic-growth/keyword-cluster-map` | `skills/keyword-cluster-map` | migrated | — |
| archive `skills/organic-growth/schema-entity-review` | `skills/schema-entity-review` | migrated | — |
| archive `skills/organic-growth/onpage-optimization-pass` | `skills/onpage-optimization-pass` | migrated | — |
| archive `skills/organic-growth/seo-quality-gate` | `skills/seo-quality-gate` | merged | — |
| archive `skills/organic-growth/competitor-gap-analysis` | `skills/competitor-gap-analysis` | migrated | — |
| archive `skills/organic-growth/local-seo-review` | `skills/local-seo-review` | migrated | — |
| archive `skills/organic-growth/cwv-performance-seo-review` | `skills/cwv-performance-seo-review` | migrated | — |
| archive `skills/organic-growth/gsc-ga4-analysis` | `skills/gsc-ga4-analysis` | migrated | — |
| archive `skills/organic-growth/serp-intent-audit` | `skills/serp-intent-audit` | migrated | Incluída (procedimento reutilizável). |
| archive `skills/organic-growth/ai-search-visibility-review` | agente `ai-search-visibility` + `STRATEGY_RULES`/`CONTENT_RULES` | deferred | Skill própria não criada — evitar selva. |
| archive `skills/organic-growth/internal-linking-architecture` | agente `internal-linking` + skill `onpage-optimization-pass` | deferred | — |
| archive `skills/organic-growth/wordpress-seo-implementation` | agente `wordpress-seo-implementation` + `TECHNICAL_RULES` | deferred | — |
| archive `skills/organic-growth/seo-operating-system` | `project/OPERATING_SYSTEM.md` | covered_by_project_doc | Era operating system, não skill. |
| archive `skills/organic-growth/seo-reporting-dashboard` | `project/REPORTING_MODEL.md` + `KPI_MODEL.md` | deferred | — |
| archive `skills/organic-growth/page-quality-audit` | `skills/onpage-optimization-pass` + `seo-quality-gate` | covered_by_skill | — |
| archive (antigo) `skills/{content-quality-review, internal-linking-review, local-seo-review, schema-review, seo-page-brief, seo-strategy-review, technical-seo-review}` | skills/project docs correspondentes | merged / covered | Versões antigas; substituídas pelas do organic-growth. |

## Records / reports

| Origem | Destino | Estado | Notas |
|---|---|---|---|
| archive `reports/_TEMPLATE_seo-report.md` | `records_template/SEO_REPORT_TEMPLATE.md` | merged | Convertido em template reutilizável. |
| archive `reports/README.md` | `records_template/README.md` + `project/REPORTING_MODEL.md` | merged | Convenção de nomes + living-vs-dated. |
| archive `reports/2026-05-20__*.md` (aio-expansion, architecture-map, competitor-deep-dive, execution-plan-90d, previmed-pages-audit, spin-offs-briefs) | `records_template/*` (ideias) | not_applicable | **Reports reais Previmed — não copiados.** Ideias convertidas em templates; os reports ficam no archive. |
| archive `clusters/*` (BRIEF/COPY/aio-capture.yml) | — | not_applicable | Dados de conteúdo Previmed; ficam no archive. |
| (novo) | `records_template/{SEO_AUDIT,SEO_TASK,SEO_DECISION}_TEMPLATE.md`, `SEO_GO_LIVE_CHECKLIST.md` | migrated | Novos templates reutilizáveis. |

## Pontes / pointers criados (compatibilidade, sem perda)
- `.claude/agents/seo-growth-system/{seo-lead,technical-seo,content-growth,competitor-research}.md` → pontes para o module + `README.md`.
- `.claude/commands/seo.md` (global) + `.claude/commands/seo-growth-system/*` → pontes para `/seo` + `README.md`.
- `.claude/project/seo-growth-system/README.md` e `.claude/skills/seo-growth-system/README.md` → pointers (ficheiros antigos mantidos por compatibilidade, ainda referenciados pelo `supervisor.md`).

## Não tocado
`.claude/_archive/` — intacto. Toda a equipa WordPress/visual/safety/agent-architecture/execution do ativo — intacta (fora do âmbito SEO).
