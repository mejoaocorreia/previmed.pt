---
name: onpage-optimization-pass
description: Otimizar elementos on-page de uma pagina (titles, metas, headings, copy, links, alt).
---

# Skill: On-page Optimization Pass

## Objetivo
Otimizar os elementos on-page de uma página (titles, metas, headings, copy, links, alt) mantendo leitura humana.

## Quando usar
Otimizar/rever uma página específica (`/seo content`, parte on-page).

## Quem pode usar
[`onpage-seo`](../../agents/onpage-seo.md) (principal), [`content-growth`](../../agents/content-growth.md).

## Inputs necessários
Página/URL, brief/intenção, tom de marca.

## Procedimento
1. Confirmar intenção e keyword principal. 2. Title (≤ ~60 chars, orientado a CTR). 3. Meta description (~155 chars, persuasiva). 4. H1 único + hierarquia H2/H3. 5. Melhorar copy à intenção (sem stuffing). 6. FAQs úteis. 7. Links internos contextualizados. 8. Alt text das imagens. 9. Notas de UX/SEO.

## Output esperado
Title · meta description · H1 · estrutura H2/H3 · melhorias de texto · links internos · FAQs · notas de UX/SEO.

## Critérios de qualidade
Title/meta dentro de limites; hierarquia correta; texto legível e específico; links úteis; sem stuffing.

## Erros comuns
Keyword stuffing; headings só por estilo; meta genérica; títulos duplicados; alt vazio/keyword-spam.

## Agentes relacionados
[`onpage-seo`](../../agents/onpage-seo.md), [`internal-linking`](../../agents/internal-linking.md), [`wordpress-seo-implementation`](../../agents/wordpress-seo-implementation.md).

## Project docs relacionados
[`CONTENT_RULES`](../../project/CONTENT_RULES.md), [`TECHNICAL_RULES`](../../project/TECHNICAL_RULES.md).

## Ferramentas/MCPs possíveis
Browser (preview/SERP), Search Console (CTR). Read-only.

## Notas de consolidação
Consolidado da versão anterior do pacote SEO (skill on-page + capacidade de onpage-seo).


---

## Legacy/imported notes

### From .claude/skills/seo-growth-system/content-quality-review/SKILL.md

# Skill: Content Quality Review

## Objetivo

Rever conteúdo SEO/comercial antes de publicar ou implementar.

## Avaliar

- intenção;
- clareza;
- utilidade;
- originalidade;
- prova/confiança;
- E-E-A-T;
- CTA;
- estrutura H1/H2/H3;
- linguagem;
- risco de claims falsos;
- adequação à marca;
- ligação interna;
- duplicação/canibalização;
- necessidade de revisão humana.

## Output

```md
## Content Quality Review

Score: [0-100]

### Pontos fortes
...

### Problemas
...

### Riscos
...

### Melhorias propostas
...

### Veredito
[Aprovar / Rever / Bloquear]
```

## Regra

Se o conteúdo parecer genérico, inventar provas ou tocar em temas legais/saúde sem base, bloquear ou pedir revisão humana.
