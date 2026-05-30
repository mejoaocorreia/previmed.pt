# SEO Quality Gate Example

## SEO Quality Gate

### Escopo validado
Revisao de proposta para alterar slug de uma pagina de servico.

### Evidencia usada
- URL atual fornecida.
- Proposta de novo slug.
- Sem dados GSC.
- Sem plano de redirects.

### Resultado
Bloqueado

### Problemas encontrados
- Alteracao de slug sem plano 301.
- Sem avaliacao de trafego/indexacao da URL atual.
- Sem plano para atualizar internal links e sitemap.

### Correcoes obrigatorias
1. Criar plano 301.
2. Verificar GSC/URL Inspection se autorizado.
3. Atualizar internal links.
4. Definir rollback.

### Precisa de autorizacao?
Sim. Envolve URL indexada e possivel producao.

### Proximo passo
Encaminhar para `/seo technical` e depois `/seo go-live`.
