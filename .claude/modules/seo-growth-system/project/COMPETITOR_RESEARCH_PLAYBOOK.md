# Competitor Research Playbook

## Objetivo
Analisar concorrência para descobrir quem rankeia, que tipo de página rankeia, porque satisfaz a intenção, que conteúdo falta ao nosso site e que qualidade é preciso superar — sem copiar.

## Quando usar
Antes de definir página/cluster/serviço, ou para diagnóstico de uma SERP.

## Regras principais
- Não copiar texto/estrutura; analisar para superar.
- Separar concorrente comercial, orgânico e de autoridade.
- Distinguir evidência de hipótese; registar URLs e data.
- Sem scraping agressivo; dados pagos só com ferramenta autorizada (senão não inventar).
- Considerar marca, confiança, UX e conversão — não só ranking.

## Processo
1. Definir queries prioritárias. 2. Pesquisar SERP por localização/dispositivo quando relevante. 3. Identificar concorrentes orgânicos reais. 4. Separar tipos (negócio, orgânico, diretórios, institucionais, marketplaces, snippets/AI Overviews). 5. Analisar top 5–10 por query. 6. Registar por resultado: URL, tipo de página, title, meta, H1, estrutura, conteúdo, FAQs, schema, UX, CTA, sinais locais, performance visível, diferencial. 7. Identificar lacunas. 8. Propor página/estrutura superior.

## O que observar
title/meta · H1/H2/H3 · profundidade · FAQs · prova/confiança · CTA · links internos · entidades · schema · velocidade/mobile · clareza comercial · diferenciação · conteúdo local · reviews/GBP · tipo de conteúdo que a SERP favorece · presença em AI Overviews/AI Mode (se observável).

## Inputs
Tema/serviço, mercado/localização, queries, intenção alvo.

## Outputs
SERP snapshot · concorrentes principais (tabela) · intenção dominante · padrões SERP · gaps · oportunidades · recomendação · prioridade. Persistir como record datado para análises grandes (ver [`REPORTING_MODEL.md`](REPORTING_MODEL.md)).

## Agentes relacionados
[`serp-competitor-analyst`](../agents/serp-competitor-analyst.md), [`keyword-intent`](../agents/keyword-intent.md), [`ai-search-visibility`](../agents/ai-search-visibility.md).

## Skills relacionadas
[`competitor-gap-analysis`](../skills/competitor-gap-analysis/SKILL.md), [`serp-intent-audit`](../skills/serp-intent-audit/SKILL.md).

## Ferramentas/MCPs possíveis
Browser/Search (SERP real), Rich Results (schema dos rivais). Pagas só com autorização.

## Critérios de qualidade
Concorrentes orgânicos reais; data registada; recomendação para superar; dados pagos só se existirem.

## Notas de consolidação
Fusão do protocolo de concorrência do conteúdo ativo com o playbook de competitor research da versão anterior do pacote SEO + capacidade dos agentes de concorrência.


---

## Legacy/imported notes

### From .claude/project/seo-growth-system/COMPETITOR_RESEARCH_PROTOCOL.md

# Competitor Research Protocol

## Objetivo

Analisar concorrência para encontrar padrões, lacunas e oportunidades,
sem copiar conteúdo.

---

## Tipos de concorrentes

### Concorrente comercial

Empresa que disputa clientes.

### Concorrente orgânico

Página/domínio que aparece na SERP para as queries importantes.

### Concorrente de autoridade

Entidade reconhecida que domina confiança, mesmo sem vender o mesmo serviço.

---

## Processo

1. Definir serviço/tema.
2. Definir mercado/localização.
3. Definir queries.
4. Pesquisar SERP.
5. Listar concorrentes.
6. Classificar intenção.
7. Analisar estrutura.
8. Analisar conteúdo/prova/CTA.
9. Analisar schema/performance se possível.
10. Identificar gaps.
11. Criar recomendações.

---

## O que observar

- title/meta;
- H1/H2/H3;
- profundidade;
- FAQs;
- proof/trust;
- CTA;
- links internos;
- entidades;
- schema;
- velocidade/mobile;
- clareza comercial;
- diferenciação;
- conteúdo local;
- reviews/GBP quando aplicável;
- tipo de conteúdo que a SERP favorece;
- presença em AI Overviews/AI Mode se observável.

---

## Dados pagos/autorizados

Se houver acesso a Ahrefs/Semrush/DataForSEO/SerpAPI ou similares, pode avaliar:

- backlinks;
- autoridade de domínio;
- keywords estimadas;
- tráfego estimado;
- lacunas de conteúdo;
- SERP features.

Se não houver acesso, não inventar estes dados.

---

## Output

```md
# Competitor Research — YYYY-MM-DD

## Tema
...

## Queries analisadas
...

## Concorrentes
| Concorrente | URL | Tipo | Pontos fortes | Pontos fracos |

## Intenção dominante
...

## Padrões SERP
...

## Gaps
...

## Oportunidades
...

## Recomendação
...
```


## Referências externas base

- Google Search Essentials: https://developers.google.com/search/docs/essentials
- Google SEO Starter Guide: https://developers.google.com/search/docs/fundamentals/seo-starter-guide
- Helpful, reliable, people-first content: https://developers.google.com/search/docs/fundamentals/creating-helpful-content
- AI features and your website: https://developers.google.com/search/docs/appearance/ai-features
- Structured data general guidelines: https://developers.google.com/search/docs/appearance/structured-data/sd-policies
- Structured data introduction: https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data
- Core Web Vitals and Google Search: https://developers.google.com/search/docs/appearance/core-web-vitals
- URL Inspection API: https://developers.google.com/search/blog/2022/01/url-inspection-api
- URL Inspection Tool: https://support.google.com/webmasters/answer/9012289
- Search spam policies: https://developers.google.com/search/docs/essentials/spam-policies
- Google Business Profile local ranking: https://support.google.com/business/answer/7091
