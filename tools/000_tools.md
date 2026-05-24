# Tools

Ferramentas reutilizáveis da Previmed.

## Objetivo
Guardar ferramentas pensadas para serem **reutilizáveis** entre workspaces e departamentos — *com o quê* se trabalha.

## O que vai guardar aqui
- uma pasta por tool, com um `000_<tool>.md` explicativo;
- a classificação da tool (interna / pública futura / open source futura / por definir);
- ligação aos workspaces que a usam.

Tools iniciais:
- **browser_rules_engine** — navegação e automação em websites/plataformas.
- **email_escape** — escape/tratamento automático de emails/textos.
- **archive/** — tools descontinuadas ou históricas.

## Regras
- Tools **não** devem ficar dentro de workspaces como regra.
- Uma tool pode **nascer** da necessidade de um workspace, mas deve ser **reutilizável**.
- Uma tool pode ser interna, pública futura, open source futura ou produto futuro.
- A classificação explica-se no próprio `.md` — **sem** criar subpastas `public/internal` agora.

## Como os agentes vão usar
Quando uma tarefa precisa de uma capacidade reutilizável (navegar/automatizar, tratar texto/emails), o agente procura primeiro uma tool aqui antes de improvisar dentro de um workspace.

## Estado atual
Base inicial com duas tools como placeholders explicativos. **Sem código funcional.**

## Próximos passos
- [ ] amadurecer cada tool antes de qualquer implementação
- [ ] decidir quais tools podem tornar-se repos/produtos próprios
