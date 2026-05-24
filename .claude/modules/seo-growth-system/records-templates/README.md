# SEO Records Templates

Templates SEO do plugin [`seo-growth-system`](../README.md). **Vivem dentro do plugin** (para o plugin ser autossuficiente ao exportar).

## Para que servem
Servem para criar records SEO consistentes: **auditorias, reports, decisões, tasks e go-live**.

## Importante
- Estes ficheiros são **templates**, não records reais. Copiar para a pasta de records do projeto-alvo (ex.: `.claude/records/audits/seo/`), datar e preencher.
- Vivem dentro do plugin para que, ao instalar noutro repo, os templates venham junto.

## Templates disponíveis
- [`SEO_AUDIT_TEMPLATE.md`](SEO_AUDIT_TEMPLATE.md) — auditoria SEO (completa ou por área).
- [`SEO_TASK_TEMPLATE.md`](SEO_TASK_TEMPLATE.md) — tarefa/lote SEO acionável.
- [`SEO_REPORT_TEMPLATE.md`](SEO_REPORT_TEMPLATE.md) — relatório datado genérico (audit/competitor/keyword/etc.).
- [`SEO_DECISION_TEMPLATE.md`](SEO_DECISION_TEMPLATE.md) — decisão SEO duradoura.
- [`SEO_GO_LIVE_CHECKLIST.md`](SEO_GO_LIVE_CHECKLIST.md) — checklist de go-live SEO.

## Convenção de nome (no destino)
`YYYY-MM-DD__report-type.md` (data ISO 8601 + `__` + kebab-case). Markdown sempre.

## Depois de criar um record datado
Atualizar os ficheiros de estado vivos do projeto (status/backlog/opportunities/decisions) sem duplicar o relatório inteiro. Ver [`REPORTING_MODEL.md`](../project/REPORTING_MODEL.md) do module.
