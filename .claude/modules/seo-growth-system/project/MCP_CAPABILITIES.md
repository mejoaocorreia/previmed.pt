# MCP Capabilities

Mapa para o projeto consumidor declarar que ferramentas/MCPs existem no ambiente real.

Este ficheiro e um template operacional. O module nao assume que qualquer ferramenta esta instalada, autenticada ou autorizada.

---

## Como Usar

No projeto consumidor, preencher uma tabela equivalente com o estado real.

Estados:

- `available`
- `available-read-only`
- `requires-authorization`
- `not-installed`
- `unknown`

---

## Matriz De Capacidades

| Ferramenta / MCP | Estado | Uso SEO | Escrita permitida? | Dados sensiveis? | Notas |
|---|---|---|---|---|---|
| Filesystem | unknown | ler repo, criar records | depende do projeto | possivel | nunca guardar segredos |
| Git | unknown | diff, branch, historico | so autorizado | baixo/medio | evitar reset/force |
| GitHub | unknown | PRs, issues, checks | so autorizado | possivel | cuidado com comentarios publicos |
| Browser/Search | unknown | SERP, concorrencia, AI Search | nao | baixo | registar data/local/dispositivo |
| Playwright | unknown | render, mobile, crawl leve | nao | possivel se autenticado | evitar areas autenticadas sem autorizacao |
| Chrome DevTools | unknown | performance, DOM, network | nao | possivel | read-only |
| Lighthouse/PageSpeed | unknown | CWV/lab data | nao | baixo | distinguir lab vs field |
| GSC | unknown | queries, indexacao, URL Inspection | nao por defeito | pode conter dados reais | requer autorizacao |
| GA4 | unknown | sessoes, conversoes, landing pages | nao por defeito | pode conter dados reais | requer autorizacao |
| Google Business Profile | unknown | local SEO, NAP, perfil | nao por defeito | medio | write exige autorizacao |
| Rich Results Test | unknown | validar schema | nao | baixo | read-only |
| Schema.org validator | unknown | validar JSON-LD | nao | baixo | read-only |
| Ahrefs/Semrush/DataForSEO/SerpAPI | unknown | paid SEO data | nao por defeito | medio | autorizacao explicita |

---

## Regra Para Agentes

Antes de usar uma ferramenta:

1. confirmar se existe;
2. confirmar se esta autenticada;
3. confirmar se ha autorizacao;
4. confirmar escopo;
5. declarar limitacoes se faltar acesso.

Se nao houver ferramenta, nao inventar dados.
