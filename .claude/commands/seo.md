# Command: /seo (ponte global)

Este é o **ponto de entrada nativo** para o module SEO Growth System.

O Claude Code descobre comandos em `.claude/commands/`, mas **não** descobre o conteúdo dentro de `.claude/modules/`. Por isso este ficheiro existe aqui e **encaminha** para o module.

## Fonte da verdade
[`.claude/modules/seo-growth-system/commands/seo.md`](../modules/seo-growth-system/commands/seo.md)

## Como usar
`/seo <modo>` — modos disponíveis: `audit`, `technical`, `content`, `brief`, `keywords`, `local`, `schema`, `competitor`, `data`, `performance`, `ai-search`, `wordpress`, `go-live`, `qa`.

Sem modo, trata como `/seo audit` (auditoria/diagnóstico) e o SEO Lead clarifica o objetivo.

## Encaminhamento
1. Carregar o SEO Lead: [`.claude/modules/seo-growth-system/agents/seo-lead.md`](../modules/seo-growth-system/agents/seo-lead.md).
2. O SEO Lead lê o modo no comando do module e coordena subagentes/skills/project docs.
3. Governação (supervisor/system-safety) vence sempre; SEO não mexe em produção/URLs sem autorização.

## Regra
Este ficheiro é **só ponte** — não duplicar aqui a lógica dos modos. Atualizar a lógica no module.
