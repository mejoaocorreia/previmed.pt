# SEO Current Status

> Ficheiro **vivo e curto**. Estado atual do trabalho SEO num relance.
> Para análise detalhada, ver [`reports/`](./reports/).

## Última atualização

2026-05-20

## Fase atual

**Fase 2 — Dados.**

Fase 1 (estratégia) fechada. Fase 2 a recolher dados antes de iniciar Fase 3 (produção de conteúdo).

## Estado por área

| Área | Estado | Notas |
|---|---|---|
| Estratégia | ✅ concluída | Ver `STRATEGY.md`. |
| Auditoria técnica baseline | ✅ concluída | `AUDIT_PREVIMED_BASELINE.md`. |
| Keyword data tool | ⏳ decisão pendente | Aguarda escolha A–F em `DECISION_KEYWORD_DATA_TOOL.md`. |
| Setup GSC/GA4/PSI | ⏳ execução pendente | Checklist em `SETUP_GSC_GA4.md`. Lado utilizador. |
| AIO expansion (5 queries) | ✅ concluída | Ver `reports/2026-05-20__aio-expansion.md`. |
| Baseline metrics | ⛔ bloqueado | Precisa de 28d de GSC após ligação. |
| Briefs P1 (5 pillars) | 🟡 a iniciar | Decorrente da AIO expansion. Ver backlog. |

## Último relatório

- **2026-05-20** — [`reports/2026-05-20__competitor-deep-dive.md`](./reports/2026-05-20__competitor-deep-dive.md) — auditoria competitiva de 7 URLs (Forprev, SEPRI ×3, Centralmed ×3) + Previmed `/saude-no-trabalho/`. Achados-chave:
  - **Centralmed = padrão ouro** em citação outbound institucional (6–8 links externos a ACT/DGS/pgdlisboa/FAO/EUR-Lex por artigo). Sem schema JSON-LD detectável — o link graph é a alavanca AIO.
  - **SEPRI = padrão "árvore"** (1 pillar + spin-offs geográficos/tópicos cruzados). 3 URLs em AIO Q1.
  - **Forprev** = caso mais curto (656w) que aparece em AIO via Service schema + 28 FAQs.
  - **Previmed `/saude-no-trabalho/`** tem problemas estruturais: title duplicado, hierarquia H1→H3 quebrada, 0 links externos institucionais, schema genérico, "Medicina **No** Trabalho" no body (sem preposição "do").

- **2026-05-20** — [`reports/2026-05-20__aio-expansion.md`](./reports/2026-05-20__aio-expansion.md) — análise AIO em 5 queries P1. Previmed citado em 1/5 (Q5). Achado crítico: lei 35h→40h. Concorrentes dominantes: Centralmed, SEPRI, Forprev, Medilav, Ecosáude, Preveris.

## Próximos passos

1. Utilizador decide entre cenários A–F em `DECISION_KEYWORD_DATA_TOOL.md`.
2. Utilizador executa checklist em `SETUP_GSC_GA4.md` (ligar GSC/GA4/Site Kit + API PSI).
3. Decidir ordem de produção dos 5 briefs P1 (ver `reports/2026-05-20__aio-expansion.md` §Decisions Needed #2).
4. Atualizar `STRATEGY_KEYWORDS.md` cluster Formação para 35→40h (decisão registada em `SEO_DECISION_LOG.md`).
5. Após 28d de coleta GSC: produzir baseline metrics (novo relatório datado).
6. Auditoria competitiva: forprev.pt, sepri.pt, centralmed.pt (próximo relatório).

## Bloqueios atuais

- **Decisão keyword data tool** — bloqueia depth analysis de volumes/concorrência.
- **Setup GSC/GA4** — bloqueia baseline metrics e validação de hipóteses do `STRATEGY.md`.

## Como atualizar este ficheiro

Atualizar sempre que:
- um novo relatório é adicionado a `reports/`;
- o estado de uma área muda (concluído / bloqueado / desbloqueado);
- a fase atual muda.

Manter **curto**. Sem análise — só estado. Análise vai para `reports/`.
