# Project Findings

<!--
NOTA EXPLICATIVA PARA HUMANOS:
Este ficheiro guarda itens identificados durante o trabalho que não devem
interromper a tarefa atual.

Não é uma lista de tarefas imediatas, nem um backlog de execução.
É uma memória organizada de itens para análise futura.
-->

Este ficheiro guarda itens identificados durante o trabalho que não devem
interromper a tarefa atual.

Um finding pode ser:

- problema identificado;
- correção futura;
- melhoria;
- risco;
- inconsistência;
- dívida técnica;
- oportunidade;
- decisão adiada;
- investigação necessária;
- limpeza;
- documentação futura.

Regra:
Se não for urgente, não interromper a tarefa atual.
Registar aqui para análise futura.

Este ficheiro não é uma lista de tarefas imediatas.
É uma memória organizada de itens que devem ser avaliados mais tarde mediante
o estado atual do projeto.

---

## Quando usar

Usar quando durante uma tarefa surgir algo como:

- aviso técnico não bloqueante;
- melhoria útil mas não urgente;
- problema que não faz parte do escopo atual;
- possível dívida técnica;
- limpeza futura;
- decisão que deve ser revista depois;
- incoerência pequena;
- oportunidade de melhoria;
- necessidade de investigação futura.

---

## Quando não usar

Não usar para:

- incidentes de segurança;
- dados pessoais/sensíveis;
- decisões RGPD;
- produção;
- comandos perigosos;
- tarefas em execução;
- bugs críticos;
- alterações que bloqueiam a tarefa atual.

Nestes casos, usar os ficheiros próprios de System Safety, incidents,
decisions ou task continuity.

---

## Categorias

Categorias recomendadas:

- Correção futura
- Melhoria
- Risco
- Inconsistência
- Dívida técnica
- Investigação
- Decisão adiada
- Oportunidade
- Limpeza
- Documentação

---

## Estados

Estados recomendados:

- Por analisar
- Aprovado para fazer
- Em curso
- Feito
- Adiado
- Rejeitado

---

## Tabela

| ID | Data | Categoria | Área | Item identificado | Impacto | Urgência | Estado | Próxima análise | Origem |
|---|---|---|---|---|---|---|---|---|---|
| F-001 | 2026-05-22 | Correção futura | Git | Git reporta aviso LF/CRLF em `supervisor_min.md`; avaliar criação de `.gitattributes` para normalizar line endings | Pode gerar diffs sujos em Windows, mas não afeta funcionamento | Baixa | Por analisar | Quando houver lote de higiene técnica | aviso Git |
| F-002 | 2026-05-22 | Inconsistência | Naming / Agent Architecture | Pasta `.claude/agents/ceo-growth-system/` continha apenas agentes SEO; renomeada para `seo-growth-system/` (mesmo padrão em `project/`, `skills/`, `commands/`). Justificação "CEO=direção" no supervisor.md foi substituída por descrição estratégica neutra. | Médio — afetou supervisor.md, supervisor_min.md, project docs, agents, skills, commands | Média | Feito em 2026-05-22 | Feito | observação do utilizador |

---

## Notas

- Não guardar dados pessoais.
- Não guardar segredos.
- Não guardar conteúdo sensível.
- Descrever o problema sem expor informação privada.
- Se o finding envolver segurança ou dados, mover para System Safety / records apropriado.

---

## Distinção rápida

- **Finding** = item identificado para análise futura (este ficheiro).
- **Decision** = decisão tomada (`../decisions/`).
- **Incident** = problema sensível/crítico (`../incidents/`).
- **Task** = trabalho em execução (`../tasks/CURRENT_TASK.md`).
- **Audit / Report** = análise estruturada (`../audits/`, `../reviews/`).
