# Workspaces

Espaços concretos de trabalho da Previmed.

## Objetivo
Representar *onde* o trabalho acontece — frentes de trabalho reais, cada uma com o seu contexto, departamentos, tools e manuais relevantes.

## O que vai guardar aqui
- um workspace por frente de trabalho concreta;
- contexto e estado de cada workspace;
- ligações a departamentos, tools e manuais.

Workspaces iniciais:
- **previmed_pt** — o site Previmed.pt.
- **careview** — trabalho relacionado com a plataforma Careview.
- **archive/** — workspaces encerrados ou históricos.

## Nota importante sobre o termo
Aqui, **`workspaces` NÃO significa VS Code workspace**. Um workspace pode representar um site, sistema, automação, campanha, frente de trabalho ou produto em desenvolvimento.

## Departamentos relacionados
Um workspace é normalmente servido por **vários departamentos** (ex.: Previmed.pt envolve `web`, `communications`, `commercial`, `compliance`).

## Tools relacionadas
Os workspaces **usam** tools de `tools/`, mas não as contêm: tools reutilizáveis ficam fora dos workspaces.

## Como os agentes vão usar
Depois de identificar o departamento, o agente identifica o **workspace** concreto onde o trabalho vive e lê o seu contexto antes de agir.

> Não usar `projects` nem `initiatives` como nome principal.

## Estado atual
Base inicial com Previmed.pt e Careview.

## Próximos passos
- [ ] preencher contexto real de cada workspace
- [ ] ligar workspaces às tools e manuais ativos
