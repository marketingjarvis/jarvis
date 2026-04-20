---
step: 9
id: "step-09-review"
type: execution
agent: vera-veredito
title: "Revisão Editorial"
next_step: "step-10-aprovacao-final"
---

# Step 09 — Execução: Revisão Editorial

**Agente:** Vera Veredito (inline)

## Trigger

Executado automaticamente após o Step 08 (geração do HTML).

## Input

- `output/carousel-copy.md` — copy aprovada (referência)
- `output/carousel.html` — HTML gerado (objeto de revisão)

## Task

Executar a task `review.md`:
1. Revisar cada um dos 7 slides contra critérios de qualidade
2. Verificar legenda Instagram
3. Verificar critérios estruturais (total de slides, alternância, dados + fontes)
4. Checar veto conditions
5. Emitir veredito por slide e veredito final

## Output

Salvar em `output/review-report.md` no formato padrão do task file.

## Quality Gate

O relatório de Vera deve obrigatoriamente conter:
- [ ] Revisão individual de cada um dos 7 slides
- [ ] Revisão da legenda
- [ ] Verificação estrutural
- [ ] Veredito final claro (aprovado / aprovado com ajustes / reprovado)

## Transition

Após salvar review-report.md, apresentar o relatório ao usuário no Step 10 (aprovação final).
