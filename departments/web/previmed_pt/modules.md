# Previmed.pt — Modules

Modules reutilizáveis que este workspace usa.

## Objetivo
Listar os modules de `.claude/modules/` que servem o site Previmed.pt e quando entram.

## Modules em uso
### seo-growth-system
- **Onde:** [`.claude/modules/seo-growth-system/`](../../../.claude/modules/seo-growth-system/README.md).
- **Quando entra:** tarefas de conteúdo, pesquisa orgânica, WordPress SEO, performance web, schema, local SEO, análise de concorrentes e AI search.
- **Como:** o supervisor encaminha para o **SEO Lead** do module (ou comando `/seo`). O SEO Lead coordena os subagentes e passa por SEO QA.

## SEO não é o único sistema do workspace
SEO entra **só** para web/search/content. No Previmed.pt também atuam, conforme o caso:
- **WordPress** (implementação técnica/tema/plugins);
- **visual / UX** (qualidade visual, mobile);
- **performance** (em articulação com SEO/CWV);
- **compliance** (dados de formulários, RGPD) — transversal.

## Regra
O workspace **referencia** os modules; não copia agentes/skills para dentro de si. Dados/decisões específicas do Previmed.pt ficam no workspace e em records reais (`.claude/records/`).

## Estado atual
Um module em uso: `seo-growth-system`.

## Próximos passos
- [ ] ligar tarefas SEO reais do site ao comando `/seo`
- [ ] avaliar outros modules conforme surgirem
