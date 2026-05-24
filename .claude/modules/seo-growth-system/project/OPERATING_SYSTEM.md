# SEO Growth Operating System

Define como o module SEO Growth System trabalha. É a fonte principal de detalhe operacional.

## Objetivo
Quando usado, construir um ativo orgânico que: seja tecnicamente rastreável/indexável; responda melhor às intenções de pesquisa; represente serviços com clareza; transmita confiança; tenha conteúdo útil e diferenciado; seja rápido e bom em mobile; esteja preparado para Search clássico e AI Search; converta; e possa ser medido e melhorado.

## Quando usar
Sempre que o SEO Lead inicia trabalho médio/grande. Para microtarefas, basta a regra relevante.

## Regras principais
- Não há SEO sem intenção clara.
- Não há página nova sem papel na arquitetura.
- Não há alteração de slug sem plano de redirect.
- Não há schema sem conteúdo visível correspondente.
- Não há conteúdo SEO genérico.
- Não há design que esconda conteúdo crítico.
- Não há dependência pesada sem performance review.
- Não há análise grande sem record persistente (ver REPORTING_MODEL).
- SEO não passa por cima de segurança, produção, rollback, performance, acessibilidade, marca ou dados pessoais.

## Áreas de trabalho
Estratégia · pesquisa/intenção · concorrência/SERP · arquitetura de informação · SEO técnico · conteúdo · on-page · internal linking · schema/entidades · local SEO · performance/CWV · acessibilidade (qualidade SEO indireta) · WordPress implementation · medição/reporting · AI Search · refresh/manutenção · governance editorial.

## Processo (workflow padrão)
1. Objetivo de negócio. 2. Público e serviço. 3. Mapear intenção. 4. Concorrência/SERP. 5. Arquitetura/página. 6. Brief de conteúdo. 7. Validar SEO técnico. 8. Validar visual/mobile/performance. 9. Validar schema quando aplicável. 10. Implementar com WordPress Engineering se necessário. 11. Testar indexabilidade e experiência. 12. Medir (GSC/GA4). 13. Atualizar backlog/decisões. 14. Refresh quando necessário.

## Inputs
Objetivo, público, páginas/URLs, dados disponíveis, restrições (produção, marca, RGPD).

## Outputs
Diagnóstico/plano com evidência, prioridade (impacto/esforço/risco), próximos passos, e record persistente para análises grandes.

## Handoff entre áreas
SEO recomenda · WordPress Engineering implementa técnica · Visual Experience valida experiência · System Safety valida risco · supervisor aprova mudanças sensíveis.

## Priorização
- **Impacto:** tráfego potencial, intenção comercial, conversão, autoridade, risco técnico, nº de páginas, prioridade do negócio.
- **Esforço:** conteúdo, design, WordPress, desenvolvimento, aprovação, ferramentas, dependências.
- **Risco:** produção, slugs/redirects, indexação, performance, marca, RGPD/dados, acessibilidade.
- **Output recomendado:** quick wins · high-impact projects · technical blockers · content opportunities · long-term authority work.

## Anti-token-waste / persistência
Análise longa sem record persistente = desperdício de contexto. Antes de continuar uma análise grande, confirmar: "isto está a ser persistido?". Se não, criar o record a partir do template e só depois continuar. Ver [`REPORTING_MODEL.md`](REPORTING_MODEL.md).

## Agentes relacionados
Todos os do module, coordenados pelo [`seo-lead`](../agents/seo-lead.md).

## Skills relacionadas
Todas — ver [`../skills/`](../skills/).

## Ferramentas/MCPs possíveis
Ver [`TOOLING_MODEL.md`](TOOLING_MODEL.md).

## Critérios de qualidade
SEO só é bom se melhora utilidade, clareza para motores, confiança, performance, conversão e sustentabilidade. (Ver [`QUALITY_GATE.md`](QUALITY_GATE.md).)

## Notas de consolidação
Fusão do operating system SEO do conteúdo ativo com a versão anterior do pacote SEO (anti-token-waste, living vs dated, persistence rule). A mecânica de ficheiros vivos/datados foi generalizada para `REPORTING_MODEL`.


---

## Legacy/imported notes

### From .claude/project/seo-growth-system/SEO_GROWTH_OPERATING_SYSTEM.md

# SEO Growth Operating System

Este ficheiro define como a área **SEO Growth System** trabalha.

## Definição

SEO Growth System é a camada de crescimento orgânico e visibilidade digital vista ao nível de direção.

Não significa marca pessoal do CEO.
Significa olhar para SEO, conteúdo, reputação, autoridade, confiança, concorrência,
conversão, medição e AI Search como temas estratégicos de negócio.

---

## Source of Truth

Este ficheiro é a fonte principal da área.

Para detalhe:
- estratégia: [SEO_STRATEGY_RULES.md](./SEO_STRATEGY_RULES.md)
- técnica: [TECHNICAL_SEO_RULES.md](./TECHNICAL_SEO_RULES.md)
- conteúdo: [CONTENT_GROWTH_RULES.md](./CONTENT_GROWTH_RULES.md)
- concorrência: [COMPETITOR_RESEARCH_PROTOCOL.md](./COMPETITOR_RESEARCH_PROTOCOL.md)
- aprovação: [GROWTH_QUALITY_GATE.md](./GROWTH_QUALITY_GATE.md)

Se houver conflito com segurança, produção, RGPD, rollback ou escopo,
vence o Supervisor:
[supervisor.md](../../agents/supervisor.md)

---

## Objetivo

Construir um website que:

- seja tecnicamente rastreável e indexável;
- responda melhor às intenções de pesquisa;
- represente serviços com clareza;
- transmita confiança institucional;
- tenha conteúdo útil e diferenciado;
- seja rápido e bom em mobile;
- esteja preparado para Search clássico e AI Search;
- converta visitantes em leads qualificados;
- possa ser medido e melhorado.

---

## Áreas de trabalho

1. Estratégia de crescimento.
2. Pesquisa e intenção.
3. Concorrência/SERP.
4. Arquitetura de informação.
5. SEO técnico.
6. Conteúdo.
7. On-page.
8. Internal linking.
9. Schema/entidades.
10. Local SEO.
11. Performance/Core Web Vitals.
12. Accessibility como qualidade SEO indireta.
13. WordPress implementation safety.
14. Medição e reporting.
15. AI Search / AI Overviews / AI Mode.
16. Refresh e manutenção de conteúdo.
17. Governance editorial.

---

## Workflow padrão

1. Definir objetivo de negócio.
2. Identificar público e serviço.
3. Mapear intenção de pesquisa.
4. Analisar concorrência/SERP.
5. Definir arquitetura/página.
6. Criar brief de conteúdo.
7. Validar SEO técnico.
8. Validar visual/mobile/performance.
9. Validar schema quando aplicável.
10. Implementar com WordPress Engineering, se necessário.
11. Testar indexabilidade e experiência.
12. Medir com Search Console/GA4.
13. Atualizar backlog e decisões.
14. Fazer refresh quando necessário.

---

## Persistence Rule

Análises grandes não devem ficar apenas no chat.

Criar ficheiro datado em:

`.claude/records/audits/seo/YYYY-MM-DD__tipo-de-analise.md`

Usar quando houver:

- auditoria SEO completa;
- análise de concorrência;
- keyword/intent research;
- technical audit;
- content gap analysis;
- AI Search visibility review;
- local SEO review;
- plano 30/60/90 dias;
- revisão de arquitetura;
- revisão pós-go-live.

Também atualizar, quando aplicável:

- `.claude/records/architecture/TASK_DECISION_LOG.md`
- `.claude/records/reviews/seo/`
- `.claude/records/audits/seo/`

---

## KPIs e medição

Quando houver acesso autorizado, acompanhar:

### Search Console

- clicks;
- impressions;
- CTR;
- average position;
- queries por intenção;
- páginas com crescimento;
- páginas com queda;
- indexação;
- problemas de cobertura;
- rich results.

### GA4 / conversão

- leads;
- eventos relevantes;
- páginas de entrada;
- engagement;
- conversão por página;
- jornada até contacto/proposta.

### Technical / UX

- Core Web Vitals;
- Lighthouse/PageSpeed;
- mobile usability;
- acessibilidade;
- erros de renderização;
- páginas lentas.

### Conteúdo

- páginas sem intenção clara;
- páginas com baixa utilidade;
- conteúdo desatualizado;
- páginas órfãs;
- oportunidades de internal linking.

Sem dados reais, marcar análise como hipótese.

---

## Priorização

Classificar recomendações por:

### Impacto

- tráfego potencial;
- intenção comercial;
- conversão;
- autoridade;
- risco técnico;
- número de páginas afetadas;
- prioridade do negócio.

### Esforço

- conteúdo;
- design;
- WordPress;
- desenvolvimento;
- aprovação;
- ferramentas;
- dependências.

### Risco

- produção;
- slugs/redirects;
- indexação;
- performance;
- marca;
- RGPD/dados;
- acessibilidade.

---

## Handoff entre áreas

SEO recomenda.
WordPress Engineering implementa técnica.
Visual Experience valida experiência.
System Safety valida risco.
Supervisor aprova mudanças sensíveis.

SEO não passa por cima de:
- segurança;
- produção;
- rollback;
- performance;
- acessibilidade;
- marca;
- dados pessoais.

---

## Regra final

SEO só é bom se melhorar:

- utilidade para o utilizador;
- clareza para motores de pesquisa;
- confiança;
- performance;
- conversão;
- sustentabilidade do projeto.


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
