# Architecture Log

Registo cronológico das decisões de arquitetura do repositório Previmed.

---

## 2026-05-24 — Templates de records movidos para dentro do plugin

**Decisão (reverte a decisão #10 anterior):** os templates de records **passam a viver dentro do module/plugin** que os usa, em vez de centralizados em `.claude/records/templates/`.

- SEO: `.claude/records/templates/seo/` → **`.claude/modules/seo-growth-system/records-templates/`**.
- A pasta central `.claude/records/templates/` foi **removida**.
- **Porquê:** um plugin tem de ser **autossuficiente ao exportar**. Se os templates ficarem fora do plugin, ao instalar noutro repo os caminhos partem-se. Dentro do plugin, vêm junto.
- Os **records reais** continuam no projeto-alvo em `.claude/records/`.

Também: `.mcp.json` corrigido para ser portável (removido o `--executable-path` fixo do Chromium, que era específico da máquina).

---

## 2026-05-24 — Supervisor como governança de topo via CLAUDE.md

**Decisão:** o Supervisor **não** é um subagente — é o **agente principal** a seguir regras de topo. Para o tornar "sempre ligado" e nativo, criámos **`CLAUDE.md`** na raiz do repo (carregado automaticamente em todas as sessões).

**Porquê não subagente:** um subagente é folha (contexto isolado, **não pode delegar**). Tornar o Supervisor subagente despromovê-lo-ia de "chefe que orquestra" para "trabalhador fechado". O topo tem de ser o agente principal.

**O que o `CLAUDE.md` faz:** aponta para `supervisor_min.md` (runtime) e `supervisor.md` (governação), define a ordem de routing, manda encaminhar SEO para o plugin via `/seo` (fan-out paralelo no topo), e fixa os não-negociáveis (RGPD/segurança/produção/rollback + confirmar repo antes de commit).

**Mesmo princípio do SEO Lead:** chefes (Supervisor, SEO Lead) vivem no topo (agente principal); subagentes são folhas executoras.

---

## 2026-05-24 — SEO Growth System como plugin Claude Code

**Decisão:** transformar o module `seo-growth-system` num **plugin Claude Code** formal, para ter descoberta nativa de agentes/subagentes/skills/comando **sem duplicação** e mantendo-o **exportável/instalável**.

**O que foi feito:**
- Adicionado frontmatter (`name`/`description`) aos 15 agentes, 11 skills e ao comando `/seo` (só prepend — nenhum conteúdo removido).
- Criado `.claude/modules/seo-growth-system/.claude-plugin/plugin.json` (manifesto).
- Criado `.claude-plugin/marketplace.json` na raiz do repo (marketplace local) a apontar para o module.
- Criado `INSTALL.md` no module com os passos `/plugin marketplace add` + `/plugin install`.
- O comando `/seo` documenta a **orquestração paralela no topo** (fan-out de `Task()` a partir do agente principal; o subagente `seo-lead` não spawna outros).

**Porquê plugin:** é o conceito oficial do Claude Code para empacotar agents+commands+skills numa unidade descoberta nativamente após instalação. Resolve a tensão "fonte única vs descoberta nativa".

**Limite conhecido:** os componentes só são descobertos **após `/plugin install`** — ter os ficheiros não basta. A fan-out paralela parte do comando/agente principal, não de um subagente folha.

**Pendente de confirmação:** campos exatos de `plugin.json`/`marketplace.json` na doc atual do Claude Code (corrigir se algum `/plugin …` der erro de schema).

---

## 2026-05-24 — Previmed modular architecture decisions

### 1. `departments/`
Usamos `departments` porque é a linguagem real usada dentro da empresa.

### 2. `workspaces/`
Usamos `workspaces` para espaços concretos de trabalho. Neste repo, `workspaces` **não** significa VS Code workspace.

### 3. Não usamos `projects` nem `initiatives`
Rejeitados porque não representam bem a forma como queremos organizar frentes concretas de trabalho.

### 4. Não usamos `domains`
Rejeitado para evitar confusão com domínios de websites.

### 5. `tools/`
Tools são ferramentas reutilizáveis. Podem nascer por necessidade de um workspace, mas não pertencem ao workspace. Podem futuramente virar repos próprios, ferramentas públicas, open source ou produtos.

### 6. `manuals/`
Manuals centraliza procedimentos. Os procedimentos podem estar relacionados com departments ou workspaces, mas vivem num sítio próprio.

### 7. `shared/`
Shared guarda contexto comum, glossário, marca, referências e templates globais. Não deve guardar dados sensíveis em bruto nem tarefas operacionais.

### 8. `.claude/modules/`
Modules são unidades reutilizáveis/exportáveis de capacidade. Podem conter agentes, comandos, project docs e skills. O primeiro module é `seo-growth-system`.

### 9. Workspaces usam modules; não absorvem modules
Um workspace pode referenciar um module, mas não deve copiar agentes, skills ou regras para dentro dele. O workspace guarda contexto específico; o module guarda capacidade reutilizável.

### 10. Templates de records
Templates vivem em `.claude/records/templates/`. Modules podem referenciar templates, mas não devem guardar templates de records dentro do próprio module. Os templates SEO ficam em `.claude/records/templates/seo/`.

### 11. Migração e legado
O mapa de migração e a pasta de legado pré-redesenho foram úteis durante a transição, mas não fazem parte da arquitetura final. A estrutura final vive **sem dependência** desse legado. Ambos foram removidos em 2026-05-24.

---

> Adicionar novas entradas no topo (mais recente primeiro), com data e título.
