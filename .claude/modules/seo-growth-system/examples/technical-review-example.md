# Technical SEO Review Example

## Technical SEO Review

### Escopo
Validacao de canonical e indexacao de uma pagina de servico.

### Problemas encontrados

| Problema | Evidencia | Impacto |
|---|---|---|
| Canonical aponta para outra URL | HTML renderizado | Alto |
| Sitemap inclui ambas as URLs | sitemap.xml | Medio |

### Recomendacao
Confirmar qual URL deve indexar. Corrigir canonical, sitemap e internal links.

### Risco
Alto se a URL errada estiver indexada.

### Validacao
- Ver source/render.
- Ver sitemap.
- URL Inspection se autorizado.

### Precisa de autorizacao?
Sim, se for alterar producao.
