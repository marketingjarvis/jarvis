---
step: 3
id: "step-03-selecao-noticia"
type: checkpoint
title: "Checkpoint — Seleção de Tendência"
next_step: "step-04-generate-angles"
---

# Step 03 — Checkpoint: Seleção de Tendência

Apresentar ao usuário as 5 tendências pesquisadas por Tiago Tendências e aguardar a seleção de qual desenvolver no carrossel.

## Apresentação

Exibir um resumo das 5 tendências no formato:

```
TENDÊNCIAS ENCONTRADAS

1. {título} — Score: {X}/10
   Dado de gancho: "{dado principal}"
   Confiança: {alta/média/baixa}

2. {título} — Score: {X}/10
   Dado de gancho: "{dado principal}"
   Confiança: {alta/média/baixa}

... (repetir para 5)

Recomendação de Tiago: Tendência {N} — {justificativa}
```

## Checkpoint Question

**Qual tendência você quer desenvolver no carrossel?**

Opções:
1. Tendência 1 — {título resumido}
2. Tendência 2 — {título resumido}
3. Tendência 3 — {título resumido}
4. Tendência 4 — {título resumido}
5. Tendência 5 — {título resumido}
6. Pesquisar novamente com outro foco

## Output

Salvar em `output/selected-trend.md`:

```markdown
# Tendência Selecionada

Tendência: {título completo}
Score: {X}/10
Dado de gancho: "{dado}"
Fonte: {publicação}, {data}
```

## Transition

Após confirmação, ativar **Carlos Carrossel** para o Step 04.
