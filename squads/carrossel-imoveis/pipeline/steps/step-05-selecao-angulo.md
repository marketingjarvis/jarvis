---
step: 5
id: "step-05-selecao-angulo"
type: checkpoint
title: "Checkpoint — Seleção de Ângulo"
next_step: "step-06-create-copy"
---

# Step 05 — Checkpoint: Seleção de Ângulo

Apresentar os 5 ângulos gerados por Carlos Carrossel e aguardar a escolha do usuário antes de qualquer copy ser escrita.

## Apresentação

Exibir os 5 ângulos com hook de capa e driver emocional para cada um:

```
ÂNGULOS DISPONÍVEIS
Tendência: {tendência selecionada}

1. {Nome do ângulo}
   Driver: {gatilho emocional}
   Hook de capa: "{headline de exemplo}"
   Arco: {1 frase}

2. {Nome do ângulo}
   ...

(Repetir para os 5 ângulos)
```

## Checkpoint Question

**Qual ângulo você quer para este carrossel?**

Opções (dinâmicas — nomes dos 5 ângulos gerados):
1. Ângulo 1 — {nome}
2. Ângulo 2 — {nome}
3. Ângulo 3 — {nome}
4. Ângulo 4 — {nome}
5. Ângulo 5 — {nome}

## Output

Salvar em `output/selected-angle.md`:

```markdown
# Ângulo Selecionado

Ângulo: {nome do ângulo}
Driver emocional: {gatilho}
Hook de capa: "{headline}"}
Arco narrativo: {frase}
```

## Transition

Após confirmação, Carlos Carrossel inicia o Step 06 (escrita da copy).

**Regra crítica**: Nenhum slide de copy deve ser escrito antes desta confirmação. O ângulo é a lente emocional de todo o carrossel — mudar de ângulo depois da copy desperdiça tudo.
