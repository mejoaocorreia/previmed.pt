# Records Templates — SEO Growth System

Templates **reutilizáveis** para records SEO. **Não são records reais.**

## Regra importante
- Os **records reais** vivem em `.claude/records/` (do repo que usa o module), **não** aqui.
- Estes ficheiros são moldes: copiar para o sítio do record real, datar e preencher.
- Não preencher estes templates com dados de um projeto.

## Templates disponíveis
- [`SEO_AUDIT_TEMPLATE.md`](SEO_AUDIT_TEMPLATE.md) — auditoria SEO (completa ou por área).
- [`SEO_TASK_TEMPLATE.md`](SEO_TASK_TEMPLATE.md) — tarefa/lote SEO acionável.
- [`SEO_REPORT_TEMPLATE.md`](SEO_REPORT_TEMPLATE.md) — relatório datado genérico (audit/competitor/keyword/etc.).
- [`SEO_DECISION_TEMPLATE.md`](SEO_DECISION_TEMPLATE.md) — decisão SEO duradoura.
- [`SEO_GO_LIVE_CHECKLIST.md`](SEO_GO_LIVE_CHECKLIST.md) — checklist de go-live SEO.

## Convenção de nome (no destino)
`YYYY-MM-DD__report-type.md` (data ISO 8601 + `__` + kebab-case). Markdown sempre.

## Depois de criar um record datado
Atualizar os ficheiros de estado vivos do projeto (status/backlog/opportunities/decisions) sem duplicar o relatório inteiro. Ver [`../project/REPORTING_MODEL.md`](../project/REPORTING_MODEL.md).

## Notas de migração
Inspirado em `_archive/.../project/organic-growth/reports/_TEMPLATE_seo-report.md` e `reports/README.md`. Os reports reais do archive (aio-expansion, competitor-deep-dive, etc.) **não** foram copiados — foram convertidos na ideia destes templates reutilizáveis.
