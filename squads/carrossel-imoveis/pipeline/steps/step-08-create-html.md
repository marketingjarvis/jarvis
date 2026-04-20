---
step: 8
id: "step-08-create-html"
type: execution
agent: carlos-carrossel
title: "Geração do HTML"
next_step: "step-09-review"
---

# Step 08 — Execução: Geração do HTML

**Agente:** Carlos Carrossel (inline)
**Pré-requisito absoluto:** Aprovação do usuário no Step 07

## Trigger

Executado APENAS após aprovação explícita no Step 07.

## Input

- `output/carousel-copy.md` — copy aprovada
- `output/research-report.md` — dados e fontes para verificação

## Task

Executar a task `create-html.md` com a skill carrossel-infinito:
1. Extrair todos os dados da copy aprovada (7 slides, legenda, keyword, palavras accent, fundos)
2. Gerar HTML completo com identidade visual Jarvis
3. Aplicar paleta: #1B2A4A / #0D1B2A / #F5F0E8 / #C9A84C
4. Montserrat via Google Fonts @import
5. Header bar @jarvisimoveis.br em todos os slides
6. Preview grid 30% acima dos slides completos
7. Legenda Instagram no HTML abaixo dos slides

## Output

Salvar em `output/` com nome: `CARROSSEL-{AAAA-MM-DD}-{tema-resumido}.html`

Também registrar o path em `output/carousel.html` (symlink ou referência para o runner).

## Quality Gate

Antes de encerrar:
- [ ] 7 slides gerados com fundos corretos
- [ ] Palavra accent visível em cada slide
- [ ] Header bar @jarvisimoveis.br presente
- [ ] Legenda incluída no HTML
- [ ] Arquivo salvo com nome correto em output/

## Transition

Após salvar o HTML, acionar **Vera Veredito** para o Step 09 (revisão).
