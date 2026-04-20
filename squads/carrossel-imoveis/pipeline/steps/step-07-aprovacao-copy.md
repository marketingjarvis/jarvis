---
step: 7
id: "step-07-aprovacao-copy"
type: checkpoint
title: "Checkpoint — Aprovação da Copy"
next_step: "step-08-create-html"
---

# Step 07 — Checkpoint: Aprovação da Copy

**Este é o checkpoint mais importante do pipeline.** A copy é apresentada ao usuário para aprovação ANTES de qualquer HTML ser gerado. Nenhuma linha de código é escrita sem aprovação explícita.

## Apresentação

Exibir a copy completa de `output/carousel-copy.md` na íntegra:
- Todos os 7 slides com conteúdo, headline, dado, palavra accent e fundo
- A legenda Instagram completa
- A keyword do CTA

## Checkpoint Question

**A copy está aprovada para gerar o HTML?**

Opções:
1. ✅ Aprovada — gerar o HTML agora
2. ✏️ Ajustar um slide específico — qual slide e o que mudar
3. 🔄 Reescrever a copy com outro ângulo — voltar ao Step 05
4. ❌ Cancelar este carrossel

## Fluxo por opção

### Opção 1 — Aprovada
→ Avançar para Step 08 (geração do HTML)

### Opção 2 — Ajustar slide específico
→ Carlos Carrossel recebe o feedback e reescreve apenas o slide indicado
→ Salvar versão atualizada em carousel-copy.md
→ Retornar ao Checkpoint de Aprovação (Step 07) com a copy revisada

### Opção 3 — Reescrever com outro ângulo
→ Retornar ao Step 05 (seleção de ângulo) para o usuário escolher outro ângulo
→ Carlos Carrossel reescreve a copy do zero com o novo ângulo

### Opção 4 — Cancelar
→ Encerrar o pipeline. Arquivos parciais permanecem em output/ para referência.

## Regra crítica

**O HTML nunca é gerado sem aprovação explícita do usuário neste checkpoint.** Esta regra não tem exceções. Mesmo que a copy seja tecnicamente perfeita e passe em todos os critérios, sem o "✅ Aprovada" do usuário, o Step 08 não executa.
