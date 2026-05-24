---
name: competitor-gap-analysis
description: Analisar concorrentes e SERP para encontrar lacunas e oportunidades acionaveis.
---

# Skill: Competitor Gap Analysis

## Objetivo
Analisar concorrentes/SERP para encontrar lacunas e oportunidades acionáveis, sem copiar.

## Quando usar
Antes de definir página/cluster ou para diagnóstico competitivo (`/seo competitor`).

## Quem pode usar
[`serp-competitor-analyst`](../../agents/serp-competitor-analyst.md) (principal).

## Inputs necessários
Tema/serviço, queries prioritárias, mercado/localização, intenção alvo.

## Procedimento
1. Definir queries. 2. Listar concorrentes orgânicos reais. 3. Separar comerciais/orgânicos/autoridade. 4. Analisar top 5–10 (estrutura, conteúdo, prova, CTA, schema, UX, sinais locais). 5. Identificar padrão vencedor. 6. Encontrar gaps. 7. Propor como superar. 8. Registar data e URLs.

## Output esperado
Concorrentes (tabela: URL · tipo · forças · fraquezas) · intenção dominante · padrões SERP · gaps · oportunidades · recomendação · prioridade.

## Critérios de qualidade
Concorrentes orgânicos reais; recomendação para superar (não imitar); data registada; dados pagos só se existirem.

## Erros comuns
Copiar texto/estrutura; tratar concorrente comercial como orgânico; inventar backlinks/DA/volumes; ignorar SERP features.

## Agentes relacionados
[`serp-competitor-analyst`](../../agents/serp-competitor-analyst.md), [`keyword-intent`](../../agents/keyword-intent.md).

## Project docs relacionados
[`COMPETITOR_RESEARCH_PLAYBOOK`](../../project/COMPETITOR_RESEARCH_PLAYBOOK.md).

## Ferramentas/MCPs possíveis
Browser/Search (SERP real), Rich Results. Pagas só com autorização.

## Notas de consolidação
Fusão da skill `competitor-scan` do conteúdo SEO ativo com a skill de competitor gap analysis da versão anterior do pacote SEO.


---

## Legacy/imported notes

### From .claude/skills/seo-growth-system/competitor-scan/SKILL.md

# Skill: Competitor Scan

## Objetivo

Fazer análise rápida de concorrentes/SERP para uma página, serviço ou tópico.

## Processo

1. Definir query/tema.
2. Listar concorrentes.
3. Separar concorrentes comerciais de orgânicos.
4. Identificar intenção da SERP.
5. Comparar estrutura, conteúdo, prova, CTA.
6. Encontrar gaps.
7. Sugerir oportunidade.

## Output

```md
## Competitor Scan

### Query/Tema
...

### Concorrentes
| URL | Tipo | Força | Fraqueza |

### Intenção dominante
...

### Oportunidades
...

### Recomendação
...
```

## Regra

Não copiar texto de concorrentes.
Usar como referência estratégica, não como modelo para clonar.
Se faltar dado, dizer.
