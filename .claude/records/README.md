# Records

Registos do repositório Previmed — o que aconteceu e o que foi decidido.

## Pastas
- `audits/` — auditorias (accessibility, performance, security, seo, wordpress).
- `architecture/` — decisões estruturais e evolução da arquitetura (o *porquê* da organização) **+ logs operacionais** absorvidos da antiga `decisions/`. Ver [`architecture/README.md`](architecture/README.md).
- `backups/` — políticas e checkpoints de backup.
- `drafts/` — rascunhos (briefings, prompts, reports).
- `findings/` — achados não urgentes.
- `incidents/` — incidentes (dados, segurança).
- `reviews/` — revisões (agents, commands, seo, skills, supervisor, visual, wordpress).
- `rollbacks/` — planos e logs de rollback.
- `snapshots/` — snapshots (arquitetura, supervisor, tasks).
- `tasks/` — estado e histórico de tarefas.

## Regras
- **Records reais** vivem aqui, nas pastas próprias.
- **Templates de records** vivem **dentro do module/plugin** que os usa (ex.: SEO em `.claude/modules/seo-growth-system/records-templates/`) — não há pasta `templates/` central.
- **Decisões de arquitetura** e logs operacionais vão para `architecture/` (a antiga `decisions/` foi removida e o conteúdo absorvido lá).

## Estado atual
Estrutura de records coerente. `templates/` central removida (templates vivem com o seu module/plugin); `decisions/` absorvida por `architecture/`.
