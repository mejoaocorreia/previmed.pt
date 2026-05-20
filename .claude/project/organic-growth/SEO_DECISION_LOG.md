# SEO Decision Log

> Ficheiro **vivo**. Decisões SEO **importantes e duradouras**.
> Não regista todas as decisões — só as que afetam estratégia, arquitetura, ferramentas ou políticas a médio/longo prazo.
> Análise que justifica cada decisão vive em `reports/` ou em ficheiros de decisão dedicados.

## O que entra aqui

- Decisões arquiteturais (estrutura de URLs, hubs editoriais, taxonomias).
- Escolha de ferramentas SEO core (keyword data, crawler, monitorização).
- Políticas de SEO (regras de schema, política de canonicals, política de redirect).
- Trade-offs estratégicos (priorizar HSST B2B vs formação B2C, etc.).
- Mudanças de stack/plugins SEO no WordPress.

## O que **não** entra

- Tarefas operacionais (vão para `SEO_BACKLOG.md`).
- Hipóteses não validadas (vão para `SEO_OPPORTUNITIES.md`).
- Análise detalhada (vai para `reports/`).
- Estado atual (vai para `SEO_CURRENT_STATUS.md`).

## Formato

```
## YYYY-MM-DD — [Título curto da decisão]

- **Contexto**: 1–3 linhas sobre porquê foi precisa.
- **Decisão**: o que ficou decidido.
- **Alternativas consideradas**: o que foi rejeitado e porquê.
- **Origem**: link para relatório / discussão / ficheiro de decisão.
- **Revisão**: quando reavaliar (data ou condição).
- **Decisor**: utilizador / SEO Lead / Supervisor.
```

## Decisões

### 2026-05-20 — Cluster "Formação 35h" passa a refletir 35→40h

- **Contexto**: AIO Q4 (`formação 35 horas obrigatória`) confirma que Lei 93/2019 alterou Art.º 131.º do Código do Trabalho: o mínimo de formação contínua passou de **35 para 40 horas anuais** por trabalhador. `STRATEGY_KEYWORDS.md` (linhas 213–216) ainda usa "35h" — refletia a query do utilizador, não o referencial legal atual.
- **Decisão**: manter "35 horas" no slug/título visível (pelo volume de pesquisa esperado) **mas** abrir todas as páginas pillar do cluster Formação com a correção 35→40h explícita, citando Lei 93/2019 e Nota Técnica 9 da ACT. Adicionar variantes "40 horas obrigatórias", "Lei 93/2019 formação", "40h formação contínua" no `STRATEGY_KEYWORDS.md` quando keyword data tool estiver ligado.
- **Alternativas consideradas**: (a) ignorar a correção e manter conteúdo "35h" — rejeitado, conteúdo desatualizado perde credibilidade e arrisca queda AIO; (b) migrar todo conteúdo para "40h" e perder volume da query "35h" — rejeitado, query mantém volume residual e ignorá-la deixa terreno aos competidores.
- **Origem**: [`reports/2026-05-20__aio-expansion.md`](./reports/2026-05-20__aio-expansion.md) §Q4 + §C1.
- **Revisão**: reavaliar a cada 12 meses ou quando uma nova alteração legal for publicada.
- **Decisor**: SEO Lead (sujeito a validação do utilizador na próxima revisão de keywords).

### 2026-05-20 — Persistência de análises SEO em `reports/`

- **Contexto**: análises grandes ficavam só no chat, desperdiçando contexto.
- **Decisão**: toda análise SEO grande (auditoria, keyword research, competitor, content gap, CWV, schema, local, AI/GEO, plano de ação) é persistida em `.claude/project/organic-growth/reports/YYYY-MM-DD__report-type.md`.
- **Alternativas consideradas**: deixar no chat (rejeitado, desperdiça contexto); usar `.txt` (rejeitado, renderiza pior no GitHub).
- **Origem**: instrução do utilizador 2026-05-20 (Change Management Supervisor).
- **Revisão**: rever se estrutura `reports/` cresce a ponto de exigir subpastas por ano ou por tipo.
- **Decisor**: utilizador.

<!--
Próxima decisão será adicionada acima desta linha. Manter ordem cronológica inversa (mais recente em cima).
-->

## Decisões soltas em ficheiros próprios

Algumas decisões grandes têm ficheiro dedicado e são apenas **indexadas** aqui:

- `DECISION_KEYWORD_DATA_TOOL.md` — escolha do tool de keyword data (status: **pendente decisão do utilizador**, cenários A–F).
