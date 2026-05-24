# Departments

A estrutura/departamentos da empresa Previmed.

## Objetivo
Representar a organização real da Previmed por departamentos — *quem/que área* é responsável por cada tipo de trabalho. Serve de ponto de partida para os agentes saberem a quem pertence um pedido.

## O que vai guardar aqui
- um ficheiro `000_<departamento>.md` por departamento;
- contexto, responsabilidades e limites de cada departamento;
- as frentes de trabalho ("workspaces") do departamento, como subpastas (ex.: `web/previmed_pt/`, `operations/careview/`);
- ligações a manuais e tools relevantes.

Departamentos iniciais:
- **commercial** — área comercial, propostas, clientes e acompanhamento comercial.
- **operations** — operação interna (substitui a ideia limitada de "backoffice").
- **communications** — emails, comunicação, campanhas, linguagem e templates.
- **web** — sites, web development, WordPress, SEO, performance, UX/UI, landing pages e integrações.
- **compliance** — RGPD, dados sensíveis, permissões e risco.
- **health_safety** — SST, medicina do trabalho, segurança no trabalho e serviços relacionados.
- **training** — formação / Previforma, quando fizer sentido.

## Como os agentes vão usar
Ao receber um pedido, o agente identifica **primeiro o departamento** responsável. Um pedido pode tocar mais do que um departamento (ex.: `web` + `compliance`). `compliance` é frequentemente transversal.

> Usamos **departments** porque é a expressão usada internamente. Não usar `areas` nem `domains`.

## Workspaces (frentes de trabalho dentro dos departments)
Um **workspace** é uma frente de trabalho concreta (um site, sistema, automação, campanha, frente ou produto). **Deixou de ser uma pasta de raiz** — cada workspace vive **dentro do department dono**, como subpasta:
- `departments/web/previmed_pt/` — o site Previmed.pt.
- `departments/operations/careview/` — trabalho da plataforma Careview.

Notas:
- Departamentos descrevem *responsabilidade*; o workspace descreve *onde o trabalho acontece*. Um workspace pode envolver vários departamentos (ex.: Previmed.pt toca `web`, `communications`, `commercial`, `compliance`), mas vive na subpasta do department dono.
- Aqui, `workspace` **não** significa VS Code workspace; não usar `projects` nem `initiatives`.
- Um workspace **usa** tools de `tools/` (referenciadas num `tools.md`), mas **não** as copia para dentro de si.

## Estado atual
Base inicial com os 7 departamentos definidos como documentação.

## Próximos passos
- [ ] detalhar responsabilidades e donos de cada departamento
- [ ] ligar cada departamento às suas frentes de trabalho e manuais ativos
