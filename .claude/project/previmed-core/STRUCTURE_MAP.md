# Structure Map

Mapa da estrutura do repositório Previmed e o significado de cada parte.

## Objetivo
Dar à equipa de agentes uma visão única do que existe e do papel de cada pasta, para navegar sem ambiguidade.

## Mapa de topo
```text
previmed/
├── 000_previmed.md     # entrada principal
├── README.md           # identidade do repo
├── SOURCES.md          # fontes e pesquisa
├── departments/        # estrutura/departamentos (quem/que área) — contém as frentes de trabalho ("workspaces"), ex.: departments/web/previmed_pt/, departments/operations/careview/
├── tools/              # ferramentas reutilizáveis (com o quê)
├── manuals/            # manuais e procedimentos (como se faz)
├── shared/             # contexto, glossário, marca, referências, templates (base comum)
└── .claude/            # equipa: agents, commands, connectors, modules, project, records, skills
```

### Dentro de `.claude/`
- **modules/** — unidades reutilizáveis e exportáveis. Module ativo: `seo-growth-system` (SEO Lead + 14 subagentes, comando `/seo`, project docs, skills). Fonte da verdade do SEO. Cada module/plugin **inclui os seus próprios templates de records** (ex.: `records-templates/`), para ser autossuficiente ao exportar.
- O SEO é um **plugin** (`modules/seo-growth-system/.claude-plugin/plugin.json`); depois de `/plugin install`, os seus agentes, o comando `/seo` e as skills são descobertos nativamente. **Não há pontes nativas** (removidas para evitar duplicação).
- **project/seo-growth-system/**, **skills/seo-growth-system/** e **commands/seo-growth-system/** — **removidas**; conteúdo consolidado no module (fonte da verdade).
- **records/** — registos reais + `architecture/` (decisões estruturais + logs absorvidos da antiga `decisions/`, que já não existe). Templates de records vivem dentro do module/plugin que os usa. Ver `records/README.md`.

## Significado de cada parte
- **departments/** — responsabilidade. commercial, operations, communications, web, compliance, health_safety, training. (`web` inclui SEO/WordPress como capacidade.)
- **workspaces** — frentes de trabalho concretas, **dentro do department**: `departments/web/previmed_pt/`, `departments/operations/careview/`. (Já não existe pasta `workspaces/` na raiz.)
- **tools/** — capacidades reutilizáveis: browser_rules_engine, email_escape, archive.
- **manuals/** — procedimentos por área (commercial, operations, communications, web, compliance, careview, archive).
- **shared/** — context, glossary, brand, references, templates.
- **.claude/** — agents, commands, connectors, project, records, skills (preservados da base existente).

## Relação department ↔ workspace ↔ tool
- Departamentos descrevem *responsabilidade* e **contêm** as frentes de trabalho (workspaces).
- Um workspace descreve *onde o trabalho acontece*; vive dentro do department dono e pode envolver vários departamentos.
- Tools são *reutilizáveis* e vivem em `tools/` (fora dos departments); os workspaces apenas as referenciam num `tools.md`.

## Estado atual
Mapa alinhado com a estrutura base inicial.

## Próximos passos
- [ ] atualizar este mapa sempre que a estrutura mudar
