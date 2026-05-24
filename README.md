# Previmed

Este repositório organiza o trabalho digital, técnico e operacional da Previmed dentro do ecossistema CortexCore.

Deixou de ser apenas um pacote de SEO/Organic Growth: é agora a **base operacional modular** da Previmed.

## O que este repo inclui
- **departments/** — a estrutura/departamentos da empresa. **As frentes de trabalho concretas ("workspaces") vivem dentro do department respetivo** (ex.: `departments/web/previmed_pt/`, `departments/operations/careview/`). Já não há pasta `workspaces/` na raiz.
- **tools/** — ferramentas reutilizáveis.
- **manuals/** — manuais e procedimentos.
- **shared/** — conhecimento e contexto comum.
- **.claude/** — a equipa de agentes, comandos, skills, connectors, records e regras operacionais.
- **.claude/modules/** — **unidades reutilizáveis e exportáveis** de agentes/comandos/regras/skills. O primeiro module estruturado é o **`seo-growth-system`**.

## Princípios da nova base
- **Modules** são unidades reutilizáveis (agents + commands + project + skills); podem servir vários workspaces e ser exportados para outros projetos.
- **Workspaces usam modules; não absorvem modules** — referenciam, não copiam agentes/skills/regras.
- **Records reais** vivem em `.claude/records/`; **decisões arquiteturais** em `.claude/records/architecture/`. **Templates de records** vivem dentro do module/plugin que os usa (ex.: SEO em `.claude/modules/seo-growth-system/records-templates/`), para o module ser autossuficiente ao exportar.
- **SEO / organic growth** continua importante e profissional, mas é apenas **uma capacidade** — vive no module `seo-growth-system`, não é a identidade do repo. O Previmed.pt usa esse module; outros workspaces podem usar modules conforme necessário.
- **WordPress / web development** é **uma parte** do sistema, não o sistema inteiro (vive no departamento `web`).
- **Careview** é um **workspace próprio** em `departments/operations/careview/`.
- **Previmed.pt** é um **workspace próprio** em `departments/web/previmed_pt/`.
- **Tools** podem nascer por necessidade da Previmed, mas são pensadas para serem **reutilizáveis** — e podem tornar-se públicas, open source ou produtos próprios mais tarde. Por isso vivem em `tools/`, não dentro de workspaces.
- **.claude/** guarda agentes, comandos, skills, connectors, records e regras operacionais.

## Entrada principal
Ver [`000_previmed.md`](000_previmed.md) para a visão geral e as regras de navegação.

## Estado atual
Base modular inicial. Estrutura criada como documentação explicativa — **sem código funcional e sem comandos funcionais ainda**.
