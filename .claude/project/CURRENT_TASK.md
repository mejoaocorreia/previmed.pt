# Current Task

## Objetivo

Construir equipa SEO/Organic Growth para Previmed (HSST B2B nacional) e produzir estratégia greenfield SEO-first antes de instalar WordPress.

## Lote atual

**Fase 2 — Dados.** 2.1, 2.2, 2.3, 2.4 fechados. 2.5 (baseline metrics) bloqueado até GSC ter 28d de coleta.

Adicionalmente: **Change Management aplicado** — sistema Organic Growth passou a persistir análises grandes em `.claude/project/organic-growth/reports/` (regra `SEO_OPERATING_SYSTEM.md` §Persistence Rule / §Anti-token-waste).

## Estado

idle — aguarda (1) execução tua de 2.4 (ligar GSC, GA4, Site Kit, criar API key PSI + conta Google Ads ativa para Keyword Planner) e (2) decisão de ordem de produção dos 5 briefs P1 + brand voice "No/do trabalho" + autoria schema (ver `reports/2026-05-20__competitor-deep-dive.md` §Decisions Needed).

Lote 2.3 fechado: tool keyword data = **orçamento zero** (Cenário Z). Stack: GSC + GA4 + Keyword Planner + Playwright + PSI.

## Ficheiros alterados (desta sessão)

- `.mcp.json` — adicionado `--executable-path` apontando para `chromium-1224\chrome-win64\chrome.exe` (nova versão do MCP procura noutro path).
- `.claude/project/organic-growth/AUDIT_PREVIMED_BASELINE.md` — novo (Lote 2.1).
- `.claude/project/organic-growth/DECISION_KEYWORD_DATA_TOOL.md` — novo (Lote 2.3).
- `.claude/project/organic-growth/SETUP_GSC_GA4.md` — novo (Lote 2.4).
- `TASK_SNAPSHOT.md` — preenchido na transição Fase 1 → Fase 2.

## Feito

- Lote 0.1 (preparação): git init, arquivar duplicados, preencher PROJECT_CONTEXT/FILE_MAP/DECISION_LOG.
- Lote 1.1: `STRATEGY_AUDIENCES.md` — 3 personas + funis.
- Lote 1.2: `STRATEGY_INFORMATION_ARCHITECTURE.md` — mapa de site, URLs, menu, schema.
- Lote 1.3: `STRATEGY_KEYWORDS.md` — 16 clusters, ~120 queries.
- MCPs Tier A: Playwright (chrome-for-testing instalado) + Chrome DevTools.
- Lote 1.4: `STRATEGY_COMPETITORS.md` — 12 SERPs capturadas via Playwright, 5 categorias de concorrentes, 9 lacunas priorizadas, posicionamento Previmed baseline.
- Lote 1.5: `STRATEGY.md` — documento mestre da Fase 1, consolida audiences + IA + keywords + competitors + roadmap + KPIs + decisões em aberto.
- Initial commit `d2718fd` — 122 ficheiros, Fase 1 completa.
- Lote 2.1: `AUDIT_PREVIMED_BASELINE.md` — auditoria técnica do site atual, achados críticos (titles partidos, sem hub editorial, sem Service schema). Commit `89bb2e7`.
- Lote 2.3: `DECISION_KEYWORD_DATA_TOOL.md` — recomendação DataForSEO + GSC + Playwright + Keyword Planner. Aguarda decisão.
- Lote 2.4: `SETUP_GSC_GA4.md` — guia passo-a-passo para o utilizador ligar GSC, GA4, Site Kit, PSI API.
- Lote 2.2: `reports/2026-05-20__aio-expansion.md` — análise AIO em 5 queries P1 (medicina trabalho, segurança trabalho, HACCP, formação 35→40h, como escolher MT). Snapshots brutos em `aio-captures/`. Previmed citado em 1/5 (Q5). Achado crítico: lei mudou 35→40h.
- Change Management 2026-05-20: criados `reports/`, `_TEMPLATE_seo-report.md`, `SEO_CURRENT_STATUS.md`, `SEO_OPPORTUNITIES.md`, `SEO_DECISION_LOG.md`; atualizados `SEO_OPERATING_SYSTEM.md` (Persistence Rule + Anti-token-waste), `SEO_BACKLOG.md`, `README.md`.

## Próximo (a confirmar com utilizador)

Próximas ações em ordem:

1. **Reiniciar Claude Code** para reload do MCP Playwright (necessário para 2.2).
2. **Decidir** entre cenários A/B/C/D/E/F em `DECISION_KEYWORD_DATA_TOOL.md`.
3. **Executar** checklist em `SETUP_GSC_GA4.md` (lado utilizador).
4. Após reload, fechar **Lote 2.2** (AIO expandida em 5 queries via Playwright).
5. Depois de 28d coleta GSC → **Lote 2.5** (baseline metrics).
6. Quando Fase 2 fechar → escolher Fase 3 (briefs P1) ou Fase 4 (decisões técnicas WP).

## Retoma (se a sessão cair)

1. Ler este ficheiro.
2. `git status` (deve estar limpo após commit).
3. Confirmar Playwright funciona: `mcp__playwright__browser_navigate` para qualquer URL.
4. Pedir ao utilizador direção: Lote 1.5 A / B / C / outro.

## Notas técnicas

- Playwright MCP: chrome-for-testing instalado em `%LOCALAPPDATA%\ms-playwright\chromium-1224\`. Sem necessidade de flag `--browser`.
- Extrator JS para SERPs do Google.pt: ver chat history. Captura organic + ads + features. Snippets ocasionalmente sob consent dialog — não é evidência de ausência.
- AI Overview detectado em 12/12 queries mas só como "link Modo IA". Expandir é trabalho futuro.
