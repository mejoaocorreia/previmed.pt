# SEO Backlog

> Ficheiro **vivo**. Tarefas SEO **acionáveis e priorizadas**.
> Análise detalhada que justifica cada tarefa vive em [`reports/`](./reports/).
> Hipóteses ainda não validadas vivem em [`SEO_OPPORTUNITIES.md`](./SEO_OPPORTUNITIES.md).

## Como usar

- Adicionar tarefas que **já passaram** o filtro de oportunidade → têm dono, esforço estimado e impacto esperado.
- Cada tarefa deve apontar para a **origem** (relatório em `reports/` ou conversa).
- Marcar `[done]` quando concluído, ou mover para arquivo se for ruído.
- Manter **curto** — se cresce demasiado, dividir por fase ou produzir novo relatório de planeamento em `reports/`.

## Formato

```
- [estado] [prioridade] descrição curta — origem: reports/YYYY-MM-DD__*.md
```

- `estado`: `todo` | `wip` | `done` | `blocked`
- `prioridade`: `P1` | `P2` | `P3`

## Quick wins

- `todo` `P2` Proteger URL `/saude-no-trabalho/` — já citada por AIO. Não mexer sem plano de redirect. Origem: `reports/2026-05-20__aio-expansion.md` §Q5.

## Technical blockers

- `todo` `P2` Atualizar `STRATEGY_KEYWORDS.md` cluster "Formação 35h" → 40h. Origem: `reports/2026-05-20__aio-expansion.md` §C1+§Q4.

## Content opportunities

- `todo` `P1` Brief Pillar "Medicina do Trabalho" — `/servicos/medicina-trabalho/`. Origem: `reports/2026-05-20__aio-expansion.md` §Q1.
- `todo` `P1` Brief Pillar "Segurança no Trabalho" — `/servicos/seguranca-trabalho/`. Origem: §Q2.
- `todo` `P1` Brief Pillar "HACCP" — `/servicos/higiene-seguranca-alimentar/`. Origem: §Q3.
- `todo` `P1` Brief Pillar "Formação 40h obrigatória" — pillar formação (correção legal 35→40). Origem: §Q4.
- `todo` `P1` Guia "Como escolher empresa de medicina do trabalho" — `/recursos/guias/escolher-medicina-do-trabalho/`. Origem: §Q5.

## Competitor gaps

- `todo` `P2` Auditoria competitiva: forprev.pt/medicina-do-trabalho/ — entender porquê é top citada em AIO Q5. Origem: §T1.
- `todo` `P2` Auditoria competitiva: sepri.pt (3 entradas AIO Q1) + centralmed.pt (Q1+Q3+Q5). Origem: §T2.

## Performance issues

- A preencher (pendente PSI ligado — ver `SETUP_GSC_GA4.md`).

## Schema/entity improvements

- `todo` `P2` Adicionar schema FAQPage + Article (HowTo onde aplicável) em todas as páginas pillar P1, com `citation` para Lei 102/2009, ACT, ASAE. Origem: `reports/2026-05-20__aio-expansion.md` §T3.

## Local SEO

- A preencher.

## Measurement

- `todo` `P1` Decidir keyword data tool (cenários A–F) — origem: `DECISION_KEYWORD_DATA_TOOL.md`.
- `todo` `P1` Ligar GSC, GA4, Site Kit, criar API key PSI — origem: `SETUP_GSC_GA4.md`.
- `blocked` `P1` Produzir baseline metrics — bloqueado por 28d de coleta GSC.
- `todo` `P3` Recaptura AIO t+90d e t+180d pós-publicação pillars (novo relatório). Origem: `reports/2026-05-20__aio-expansion.md` §M2.
- `todo` `P3` Captura trimestral AIO Q4 (formação 35→40) — risco de query usar "35h" enquanto lei diz 40h. Origem: §M3.
