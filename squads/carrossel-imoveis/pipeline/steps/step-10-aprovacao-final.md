---
step: 10
id: "step-10-aprovacao-final"
type: checkpoint
title: "Checkpoint — Aprovação Final"
next_step: null
---

# Step 10 — Checkpoint: Aprovação Final

Apresentar o relatório de revisão de Vera Veredito e o carrossel finalizado ao usuário para aprovação e entrega.

## Apresentação

Exibir:
1. O veredito de Vera Veredito (aprovado / aprovado com ajustes / reprovado)
2. Lista de flags identificados (se houver)
3. Localização do arquivo final: `output/CARROSSEL-{AAAA-MM-DD}-{tema}.html`

## Fluxo por veredito

### Veredito ✅ APROVADO

Apresentar:
```
✅ Carrossel aprovado por Vera Veredito.

Arquivo: output/CARROSSEL-{data}-{tema}.html
Abra o arquivo em um navegador para capturar os slides.

Legenda Instagram incluída no HTML, abaixo dos slides.
```

→ Checkpoint: **Publicar ou arquivar?**

Opções:
1. Encerrar — carrossel pronto para captura manual
2. Gerar novo carrossel — iniciar pipeline do zero

### Veredito ⚠️ APROVADO COM AJUSTES

Apresentar flags e perguntar:

Opções:
1. Publicar assim mesmo — aceitar com os ajustes pendentes
2. Aplicar ajustes agora — Carlos Carrossel corrige os slides sinalizados e regera o HTML
3. Revisar manualmente — encerrar e o usuário ajusta o HTML diretamente

### Veredito ❌ REPROVADO

Apresentar a veto condition violada e perguntar:

Opções:
1. Corrigir e regenerar — Carlos Carrossel reescreve o slide problemático e regera o HTML
2. Reescrever a copy do zero — voltar ao Step 05 (novo ângulo)
3. Abandonar este carrossel — encerrar o pipeline

## Output Final

Após encerramento, salvar em `_memory/runs.md` o registro desta execução:

```markdown
## Run {data}

Tendência: {título}
Ângulo: {nome}
Keyword: {keyword}
Veredito: {✅/⚠️/❌}
Arquivo: output/CARROSSEL-{data}-{tema}.html
Notas: {observações relevantes para o próximo run}
```
