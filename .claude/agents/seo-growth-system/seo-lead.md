# SEO Lead (ponte)

> **Ponte de compatibilidade.** A fonte da verdade deste agente é o module:
> [`.claude/modules/seo-growth-system/agents/seo-lead.md`](../../modules/seo-growth-system/agents/seo-lead.md)

## Porque existe esta ponte
O Claude Code descobre agentes em `.claude/agents/`, mas **não** dentro de `.claude/modules/`. Este ficheiro mantém o SEO Lead descobrível e encaminha para o module, sem duplicar conteúdo.

## Papel (resumo)
Coordenador do SEO Growth System: recebe o trabalho SEO encaminhado pelo supervisor (ou pelo comando `/seo`), decide os subagentes necessários, coordena, consolida e passa por SEO QA antes de entregar. Não substitui o supervisor; governação (segurança, RGPD, produção, rollback) vence sempre.

## Como agir
1. Ler o agente completo no module (link acima) e o seu "Routing interno SEO".
2. Consultar os project docs do module conforme o pedido.
3. Chamar só os subagentes necessários (todos no module em [`agents/`](../../modules/seo-growth-system/agents/)).

## Comando relacionado
`/seo` → [`.claude/commands/seo.md`](../../commands/seo.md) → module.

## Estado
Migrado para o module (estado: merged). Conteúdo canónico no module.
