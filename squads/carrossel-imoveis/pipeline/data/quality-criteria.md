# Critérios de Qualidade — Carrossel Imóveis

Checklist consolidada aplicada em cada etapa do pipeline.

## Critérios de Pesquisa (Step 02 — Tiago Tendências)

- [ ] 5 tendências distintas (temas diferentes, não variações do mesmo)
- [ ] Cada tendência tem dado de gancho com fonte nomeada e URL
- [ ] Score editorial (1-10) com justificativa para cada tendência
- [ ] Confiança (alta/média/baixa) atribuída a cada tendência
- [ ] Pelo menos 3 tendências com dado local de Maceió/AL
- [ ] Nenhum dado com mais de 12 meses sem sinalização de data

### Veto Conditions — Pesquisa
1. Alguma tendência sem dado específico com fonte nomeada
2. Menos de 5 tendências entregues
3. Mais de 3 tendências sobre o mesmo tema

---

## Critérios de Ângulos (Step 04 — Carlos Carrossel)

- [ ] 5 ângulos distintos com drivers emocionais diferentes
- [ ] Hook de capa de exemplo para cada ângulo (específico, não genérico)
- [ ] Cada ângulo usa o dado de gancho da tendência selecionada
- [ ] Arco narrativo claro em 1 frase por ângulo
- [ ] Nenhum ângulo repete o driver emocional de outro

### Veto Conditions — Ângulos
1. Dois ou mais ângulos com o mesmo driver emocional
2. Algum hook de capa genérico (poderia ser de qualquer cidade/imobiliária)

---

## Critérios de Copy (Step 06 — Carlos Carrossel)

- [ ] 7 slides exatos: capa + 5 conteúdo + CTA
- [ ] Pelo menos 3 slides têm dado numérico com fonte nomeada
- [ ] Fundo alterna entre escuro e claro (não 3 iguais seguidos)
- [ ] Palavra em accent color (#C9A84C) identificada em cada slide
- [ ] Keyword box no slide 7 com benefício específico
- [ ] Legenda com gancho < 125 chars, fontes e hashtags (10-15)
- [ ] Tom jornalístico em todos os slides (zero frase motivacional)

### Veto Conditions — Copy
1. Algum slide com frase motivacional ("realize seu sonho", "conquiste seu imóvel")
2. Dado numérico sem fonte nomeada em qualquer slide
3. Menos de 7 slides ou mais de 7 slides

---

## Critérios de HTML (Step 08 — Carlos Carrossel)

- [ ] 7 slides exatos gerados na ordem da copy aprovada
- [ ] Alternância de fundo escuro/claro respeitada
- [ ] Palavra accent em #C9A84C destacada em cada slide
- [ ] Header bar com @jarvisimoveis.br em todos os 7 slides
- [ ] Footer com número do slide e "JARVIS INTELIGÊNCIA IMOBILIÁRIA"
- [ ] Legenda Instagram incluída abaixo dos slides
- [ ] Preview grid de 7 slides a 30% acima dos slides completos
- [ ] HTML auto-contido (sem CSS/JS externos além de Google Fonts)
- [ ] Arquivo salvo como CARROSSEL-{AAAA-MM-DD}-{tema}.html em output/

### Veto Conditions — HTML
1. Algum slide com background errado (não correspondendo à copy)
2. Palavra accent ausente em qualquer slide
3. Dependências externas além de Google Fonts

---

## Critérios de Revisão (Step 09 — Vera Veredito)

- [ ] Todos os 7 slides revisados individualmente
- [ ] Legenda Instagram revisada
- [ ] Revisão estrutural completa
- [ ] Cada flag tem critério citado
- [ ] Veredito final sem ambiguidade

---

## Escala de Veredito Final

| Status | Significado | Ação |
|---|---|---|
| ✅ Aprovado | Passa em todos os critérios | Publicar |
| ⚠️ Aprovado com ajustes | Problemas não-críticos | Ajustar antes de publicar |
| ❌ Reprovado | Veto condition ativada | Refazer slide(s) ou copy |
