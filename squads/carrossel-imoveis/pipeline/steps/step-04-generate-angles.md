---
step: 4
id: "step-04-generate-angles"
type: execution
agent: carlos-carrossel
title: "Geração de Ângulos"
next_step: "step-05-selecao-angulo"
---

# Step 04 — Execução: Geração de Ângulos

**Agente:** Carlos Carrossel (inline)

## Trigger

Executado após o Step 03 (seleção de tendência).

## Input

- `output/research-report.md` — relatório completo de tendências
- `output/selected-trend.md` — tendência selecionada pelo usuário

## Task

Executar a task `generate-angles.md`:
1. Identificar a tendência selecionada e seu dado de gancho
2. Mapear os 6 gatilhos emocionais disponíveis para esta tendência
3. Gerar 5 ângulos distintos com drivers emocionais diferentes
4. Garantir diversidade: tendência interpretada, contraintuitiva, urgência, educativo, previsão
5. Escrever hook de capa de exemplo e arco narrativo para cada ângulo

## Output

Salvar em `output/angles.md` no formato padrão do task file.

## Quality Gate

Antes de apresentar ao usuário, verificar:
- [ ] 5 ângulos distintos com drivers emocionais diferentes
- [ ] Nenhum ângulo com driver emocional repetido
- [ ] Hook de capa específico para o dado de gancho desta tendência (não genérico)
- [ ] Arco narrativo em 1 frase para cada ângulo

## Transition

Após salvar angles.md, apresentar os 5 ângulos ao usuário no Step 05.
