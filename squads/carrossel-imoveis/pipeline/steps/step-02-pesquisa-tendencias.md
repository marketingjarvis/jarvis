---
step: 2
id: "step-02-pesquisa-tendencias"
type: execution
agent: tiago-tendencias
title: "Pesquisa de Tendências"
next_step: "step-03-selecao-noticia"
---

# Step 02 — Execução: Pesquisa de Tendências

**Agente:** Tiago Tendências (subagent)

## Trigger

Executado automaticamente após o Step 01 (Checkpoint de Foco).

## Input

- `output/research-focus.md` — foco e período definidos pelo usuário

## Task

Executar a task `find-and-rank-trends.md`:
1. Ler research-focus.md
2. Executar 6 buscas focadas com WebSearch
3. Verificar fontes e extrair dados de gancho
4. Avaliar score editorial (1-10) para cada tendência
5. Montar relatório com 5 tendências classificadas

## Output

Salvar em `output/research-report.md` no formato padrão do task file.

## Quality Gate

Antes de encerrar, verificar:
- [ ] 5 tendências distintas entregues
- [ ] Cada tendência tem dado de gancho com fonte e URL
- [ ] Score editorial atribuído a cada tendência
- [ ] Pelo menos 3 tendências com dado local de Maceió/AL

## Transition

Após salvar research-report.md, retornar ao pipeline para o Step 03 (checkpoint de seleção).
