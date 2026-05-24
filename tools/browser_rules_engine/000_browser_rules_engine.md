# Browser Rules Engine

Tool futura/reutilizável para navegação e automação em websites/plataformas.

## Objetivo
Permitir navegar e automatizar trabalho em websites e plataformas de forma segura e regrada. Conceito (ainda **não** implementado), capaz de:
- mapear páginas;
- criar regras por URL;
- distinguir partes fixas e variáveis de URLs (por exemplo, IDs);
- identificar campos de login/password;
- definir regras do que **pode** e do que **não pode** tocar;
- servir Careview, WordPress, portais e outras plataformas.

## Tipo
Interna / pública futura / open source futura / por definir.
> Nasceu da necessidade do **Careview**, mas **não pertence ao Careview**. É reutilizável e pode futuramente tornar-se repo/projeto próprio ligado ao CortexCore.

## Workspaces relacionados
- `careview` (origem da necessidade);
- `previmed_pt` e outros que envolvam navegação/automação web.

## Como os agentes vão usar
Quando uma tarefa exige navegar/automatizar uma plataforma, o agente apoia-se nas regras desta tool (o que tocar, o que evitar, como tratar URLs e campos sensíveis). Compliance valida sempre quando há credenciais ou dados sensíveis.

## Estado atual
Placeholder conceptual. **Sem implementação.**

## Próximos passos
- [ ] especificar o modelo de regras por URL
- [ ] definir limites de segurança (login/password, áreas proibidas)
- [ ] avaliar se justifica repo/produto próprio
