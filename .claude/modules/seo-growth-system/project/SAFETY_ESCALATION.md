# SEO Safety Escalation

Guia curto para saber quando SEO deve parar, pedir autorizacao ou escalar para Supervisor/System Safety.

Este ficheiro nao autoriza nada. Define gatilhos de escalamento.

---

## Escalar Sempre

Escalar para Supervisor/System Safety quando houver:

- producao;
- deploy;
- rollback;
- credenciais, tokens ou API keys;
- dados pessoais;
- dados sensiveis;
- dados de trabalhadores;
- dados de saude;
- WordPress admin;
- instalacao de plugins/dependencias;
- Google Business Profile;
- ferramentas pagas;
- alteracoes de URL, slug, redirect, canonical, robots, sitemap, noindex;
- GSC/GA4 com dados reais sem autorizacao confirmada;
- risco legal, compliance, saude, seguranca ou claims sensiveis.

---

## Estados Recomendados

| Situacao | Resultado |
|---|---|
| Producao sem autorizacao | Precisa de autorizacao |
| Alteracao de slug sem redirect plan | Bloqueado |
| Schema com reviews inventadas | Bloqueado |
| Claim sensivel sem prova | Bloqueado |
| Falta de GSC/GA4 mas analise pode continuar como hipotese | Precisa de dados ou Aprovado com notas |
| Ferramenta paga solicitada sem autorizacao | Precisa de autorizacao |
| Dados pessoais no record | Bloqueado |
| WordPress admin solicitado | Precisa de autorizacao |
| GBP write solicitado | Precisa de autorizacao |
| Go-live sem rollback | Bloqueado |

---

## Como Responder

Quando escalar, devolver:

```md
## Safety Escalation

### Motivo
[producao / RGPD / credenciais / ferramenta paga / WordPress / GBP / rollback / outro]

### Risco
[baixo / medio / alto / critico]

### O que seria feito
[acao proposta]

### Autorizacao necessaria
[quem/qual autorizacao]

### Alternativa segura
[read-only / hipotese / plano sem executar]

### Proximo passo
[pedir autorizacao / criar plano / bloquear]
```

---

## Regra Final

SEO pode recomendar. SEO nao autoriza producao, dados, credenciais, rollback, ferramentas pagas ou alteracoes sensiveis.
