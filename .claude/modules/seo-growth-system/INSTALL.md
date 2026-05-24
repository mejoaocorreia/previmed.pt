# Instalar o plugin `seo-growth-system`

Este module é um **plugin Claude Code**. Os agentes, o comando `/seo` e as skills só passam a ser **descobertos nativamente depois de o plugin ser instalado** (não basta os ficheiros existirem).

## Estrutura do plugin
```
seo-growth-system/
├── .claude-plugin/plugin.json   # manifesto (obrigatório)
├── agents/                      # 15 subagentes (com frontmatter)
├── commands/seo.md              # comando /seo (orquestrador)
├── skills/<nome>/SKILL.md       # 11 skills (com frontmatter)
├── project/                     # regras/playbooks (referência, lida pelos agentes)
├── manifest.md · README.md · INSTALL.md
```

## Instalar NESTE repo (Previmed) — marketplace local
O repo já tem `.claude-plugin/marketplace.json` na raiz a apontar para este module.

```
/plugin marketplace add .
/plugin install seo-growth-system@previmed-marketplace
```
(ou usar o menu interativo: `/plugin`)

> **Recomendado (mais robusto para o `source` relativo):** adicionar o marketplace via **Git**, já que este repo está no GitHub. Os caminhos relativos do `source` resolvem de forma fiável quando o marketplace é adicionado por git:
> ```
> /plugin marketplace add https://github.com/mejoaocorreia/previmed
> /plugin install seo-growth-system@previmed-marketplace
> ```

Depois recarrega (`/reload-plugins`) e confirma:
```
/agents   → devem aparecer os agentes do plugin (com namespace, ex.: seo-growth-system:seo-lead)
```

> **Namespace (já tratado nos ficheiros):** componentes de plugin ficam com namespace `seo-growth-system:`.
> - Comando: **`/seo-growth-system:seo`** (não `/seo` puro).
> - Subagentes: **`seo-growth-system:technical-seo`**, etc. O comando `/seo` já instrui o uso do prefixo no `subagent_type`.
> - **Após instalar, confirma com `/agents`** os nomes exatos. Se diferirem, ajusta a nota de "Execução paralela" em `commands/seo.md`.

### Ordem correta: instalar → reiniciar
1. `/plugin marketplace add …` + `/plugin install …` (acima).
2. **Depois** `/reload-plugins` (ou reiniciar o Claude Code) para os componentes ficarem ativos.
3. (Reiniciar **antes** de instalar não faz nada — não há nada para carregar ainda.)
4. Confirmar: `/agents` mostra os agentes `seo-growth-system:*` e `/seo-growth-system:seo` corre.

> **Nota — paralelismo (confirmado na doc):** um subagente **não** pode lançar outros subagentes. O fan-out paralelo parte do **agente principal** quando invocas o comando `/seo` (várias `Task()` no mesmo turno; opcionalmente `background: true` para correrem concorrentes). Ou seja, o paralelismo acontece em runtime ao usar `/seo`, não automaticamente.

## Instalar NOUTRO repo (exportar)
Opção A — apontar para este repo como marketplace (git):
```
/plugin marketplace add <git-url-deste-repo>
/plugin install seo-growth-system@previmed-marketplace
```
Opção B — copiar a pasta `seo-growth-system/` para um marketplace próprio e instalar a partir daí.

**Zero cópias manuais de agentes/skills, zero duplicação** — o plugin é a fonte única.

## Orquestração paralela (importante)
- O comando **`/seo` corre no topo** (agente principal). É ele que faz o **fan-out de `Task()` em paralelo** para os subagentes (technical-seo, content-growth, etc.).
- **Não** se conta com o `seo-lead` (subagente folha) para spawnar outros subagentes — um subagente normalmente não lança subagentes. Por isso a coordenação multi-agente paralela vive no `/seo`, não dentro do `seo-lead`.
- O `seo-lead` continua útil quando invocado diretamente para planear/consolidar.

## Notas
- `project/` não é um "componente" de plugin; vai junto como referência e é lido pelos agentes por caminho relativo.
- Templates de records SEO vivem **dentro do plugin** em `records-templates/` (vêm junto ao instalar). Os **records reais** ficam no projeto-alvo em `.claude/records/`.
- Confirmar na doc oficial do Claude Code os campos exatos de `plugin.json`/`marketplace.json` se algum comando `/plugin` devolver erro de schema.
