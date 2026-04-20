---
step: 6
id: "step-06-create-copy"
type: execution
agent: carlos-carrossel
title: "Escrita da Copy"
next_step: "step-07-aprovacao-copy"
---

# Step 06 — Execução: Escrita da Copy

**Agente:** Carlos Carrossel (inline)

## Trigger

Executado após o Step 05 (seleção de ângulo confirmada pelo usuário).

## Input

- `output/angles.md` — 5 ângulos gerados
- `output/selected-angle.md` — ângulo confirmado
- `output/research-report.md` — todos os dados disponíveis com fontes

## Task

Executar a task `create-copy.md`:
1. Identificar o driver emocional do ângulo selecionado
2. Executar análise em 3 camadas (superfície → estrutura → significado)
3. Escrever os 7 slides na estrutura: capa + 5 conteúdo + CTA
4. Testar cada slide contra: uma ideia central, tom jornalístico, dado com fonte, palavra accent, fundo sugerido
5. Escrever a legenda Instagram completa com gancho < 125 chars, fontes e hashtags

## Output

Salvar em `output/carousel-copy.md` no formato padrão do task file.

## Quality Gate

Antes de entregar ao checkpoint, verificar veto conditions:
- [ ] Nenhum slide com frase motivacional
- [ ] Todo dado numérico tem fonte nomeada
- [ ] Exatamente 7 slides entregues

Carlos Carrossel **não pede aprovação durante a escrita** — entrega o bloco completo para o checkpoint decidir.

## Transition

Após salvar carousel-copy.md, apresentar a copy completa ao usuário no Step 07 para aprovação.
