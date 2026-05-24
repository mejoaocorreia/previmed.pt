---
name: seo-quality-gate
description: Avaliar se uma recomendacao ou alteracao SEO pode avancar; veredito com correcoes.
---

# Skill: SEO Quality Gate

## Objetivo
Avaliar se uma recomendação, alteração ou implementação SEO pode avançar.

## Quando usar
Antes de entregar/implementar trabalho SEO relevante e antes de go-live (`/seo qa`).

## Quem pode usar
[`seo-qa`](../../agents/seo-qa.md) (principal); SEO Lead na consolidação.

## Inputs necessários
Pedido, página/ficheiro afetado, recomendação, risco, dados disponíveis.

## Procedimento
1. Verificar intenção. 2. Impacto no utilizador. 3. Impacto no negócio. 4. Risco técnico. 5. Risco WordPress/produção. 6. Conteúdo e confiança. 7. Performance/mobile/acessibilidade. 8. AI Search sem manipulação. 9. Necessidade de autorização. 10. Decisão.

## Output esperado
```md
## SEO Quality Gate
Resultado: [Aprovado / Aprovado com notas / Bloqueado / Precisa de dados / Precisa de autorização]
### O que está bom
### O que bloqueia
### Correções obrigatórias
### Próximo passo
```

## Critérios de qualidade
Veredito claro com evidência; correções acionáveis; risco residual explícito; validação honesta.

## Erros comuns
Aprovar slug/redirect/indexação sem plano; aprovar schema enganador; aprovar conteúdo genérico; aprovar SEO que estraga UX/performance; aprovar com dados inventados.

## Agentes relacionados
[`seo-qa`](../../agents/seo-qa.md), [`seo-lead`](../../agents/seo-lead.md).

## Project docs relacionados
[`QUALITY_GATE`](../../project/QUALITY_GATE.md).

## Ferramentas/MCPs possíveis
Playwright, Lighthouse, Rich Results, URL Inspection. Read-only.

## Notas de consolidação
Fusão da skill de quality gate do conteúdo SEO ativo (skill + project doc) com a capacidade de QA da versão anterior do pacote SEO.


---

## Legacy/imported notes

### From .claude/skills/seo-growth-system/seo-quality-gate/SKILL.md

# Skill: SEO Quality Gate

## Objetivo

Avaliar se uma recomendação, alteração ou implementação SEO pode avançar.

## Entrada

- pedido;
- página/ficheiro afetado;
- recomendação;
- risco;
- dados disponíveis.

## Processo

1. Verificar intenção.
2. Verificar impacto no utilizador.
3. Verificar impacto no negócio.
4. Verificar risco técnico.
5. Verificar risco WordPress/produção.
6. Verificar conteúdo e confiança.
7. Verificar performance/mobile/accessibility.
8. Verificar AI Search sem manipulação.
9. Verificar se precisa de autorização.
10. Dar decisão.

## Output

```md
## SEO Quality Gate

Resultado: [Aprovado / Aprovado com notas / Bloqueado / Precisa de dados / Precisa de autorização]

### O que está bom
...

### O que bloqueia
...

### Correções obrigatórias
...

### Próximo passo
...
```

## Regras

- Não aprovar alteração de slug/redirect/indexação sem plano.
- Não aprovar schema enganador.
- Não aprovar conteúdo genérico.
- Não aprovar SEO que estrague UX/performance.
- Não aprovar recomendação baseada em dados inventados.
