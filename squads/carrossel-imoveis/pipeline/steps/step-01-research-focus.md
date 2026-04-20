---
step: 1
id: "step-01-research-focus"
type: checkpoint
title: "Checkpoint — Foco da Pesquisa"
next_step: "step-02-pesquisa-tendencias"
---

# Step 01 — Checkpoint: Foco da Pesquisa

Antes de iniciar a pesquisa de tendências, definir com o usuário o tema e período de interesse para o carrossel desta semana.

## Checkpoint Questions

### Questão 1: Tema da pesquisa

Perguntar ao usuário qual foco deseja para a pesquisa:

**Opções:**
1. Qualquer tendência — pesquisar o que está mais quente agora
2. Valorização e preços — foco em dados de m², altas e comparativos
3. Financiamento e juros — impacto da Selic e condições de compra
4. Novos bairros e lançamentos — onde está surgindo oferta em Maceió
5. Perfil do comprador — quem está comprando e o que está comprando
6. Outro tema específico (livre)

### Questão 2: Período da pesquisa

**Opções:**
1. Últimas 24 horas — notícia fresca
2. Últimos 7 dias — tendência da semana
3. Últimos 30 dias — tendência do mês
4. Evergreen — dado atemporal, sem urgência de data

## Output

Salvar a decisão do usuário em `output/research-focus.md`:

```markdown
# Research Focus

Foco: {foco selecionado}
Período: {período selecionado}
Data: {data atual}
```

## Transition

Após salvar research-focus.md, ativar **Tiago Tendências** para executar o Step 02.
