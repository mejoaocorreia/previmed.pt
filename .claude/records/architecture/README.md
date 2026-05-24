# Architecture Records

Decisões estruturais e evolução da arquitetura do repositório Previmed.

## Objetivo
Guardar **decisões de arquitetura**, as suas razões, alternativas rejeitadas e a evolução da estrutura do repo — o *porquê* da forma como o Previmed está organizado.

## O que entra aqui
- Por que usamos `departments`, `workspaces`, `tools`, `manuals`, `shared`, `modules`.
- Por que tools ficam fora dos workspaces.
- Por que os templates de records vivem dentro do module/plugin que os usa.
- Por que workspaces usam modules e não os absorvem.
- Decisões sobre limpeza estrutural (ex.: remoção de migração/archive).

## O que NÃO entra aqui
- Records de execução (audits, reviews, snapshots, incidents, rollbacks, tasks) — nas pastas próprias.

## Logs operacionais (absorvidos da antiga pasta de decisões)
A antiga pasta de decisões operacionais foi **removida** e todo o seu conteúdo movido para aqui (pendente de organização manual posterior):
- `ARCHITECTURE_DECISION_LOG.md`
- `COMMAND_APPROVAL_LOG.md`
- `MCP_ACCESS_LOG.md`
- `SENSITIVE_DATA_DECISION_LOG.md`
- `TASK_DECISION_LOG.md`

> Estes logs operacionais (tarefas, comandos, acessos, dados sensíveis) ficam temporariamente nesta pasta. A separação fina entre decisões estruturais e logs operacionais será tratada manualmente mais tarde.

## Ficheiros
- [`architecture_log.md`](architecture_log.md) — registo cronológico das decisões de arquitetura.
- Logs operacionais movidos da antiga `decisions/` (lista acima).

## Estado atual
Decisões da arquitetura modular Previmed registadas + logs operacionais absorvidos da antiga `decisions/`.
