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

- `todo` `P1` Corrigir title duplicado `/saude-no-trabalho/` ("Previmed - PrevimedPrevimed" → "Medicina do Trabalho — Previmed"). Origem: `reports/2026-05-20__competitor-deep-dive.md` §F1.
- `todo` `P2` Adicionar H2 à página `/saude-no-trabalho/` (atualmente salta H1→H3). Origem: §F3.
- `todo` `P2` Proteger URL `/saude-no-trabalho/` — já citada por AIO. Não mexer sem plano de redirect. Origem: `reports/2026-05-20__aio-expansion.md` §Q5.

## Technical blockers

- `todo` `P2` Atualizar `STRATEGY_KEYWORDS.md` cluster "Formação 35h" → 40h. Origem: `reports/2026-05-20__aio-expansion.md` §C1+§Q4.
- `todo` `P2` Auditoria rápida páginas core Previmed (`/seguranca-trabalho/`, HACCP, formação) — repetição de problemas (title duplicado, H2 ausentes, schema genérico, 0 ext links)? Origem: `reports/2026-05-20__competitor-deep-dive.md` §T1.

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

- `todo` `P1` **Regra fixa dos briefs P1:** mínimo 4 links externos institucionais por pillar (ACT + pgdlisboa Lei 102/2009 + 2 outros conforme tema: DGS, DGERT, ASAE, DGAV, FAO/Codex, EUR-Lex, APSEI, OA). Origem: `reports/2026-05-20__competitor-deep-dive.md` §C0.
- `todo` `P1` **Regra fixa dos briefs P1:** Schema por tipo de página — Article + FAQPage em pillars informacionais; HowTo em "como escolher" e HACCP 7 princípios; Service em página de serviço comercial. Origem: §C3.
- `todo` `P2` Adicionar `datePublished` + `dateModified` ao schema de todas as páginas pillar. Origem: §T2.
- `todo` `P2` Estratégia "árvore" SEPRI — cada pillar P1 deve ter 2–3 spin-offs planeados (geo / tópico). Origem: §A1.
- `todo` `P2` Adicionar `author` (Person) com identificação real ao schema Article — decidir quem assina. Origem: §C5+Decision #2.

## Local SEO

- A preencher.

## Measurement

- `todo` `P1` Decidir keyword data tool (cenários A–F) — origem: `DECISION_KEYWORD_DATA_TOOL.md`.
- `todo` `P1` Ligar GSC, GA4, Site Kit, criar API key PSI — origem: `SETUP_GSC_GA4.md`.
- `blocked` `P1` Produzir baseline metrics — bloqueado por 28d de coleta GSC.
- `todo` `P3` Recaptura AIO t+90d e t+180d pós-publicação pillars (novo relatório). Origem: `reports/2026-05-20__aio-expansion.md` §M2.
- `todo` `P3` Captura trimestral AIO Q4 (formação 35→40) — risco de query usar "35h" enquanto lei diz 40h. Origem: §M3.
