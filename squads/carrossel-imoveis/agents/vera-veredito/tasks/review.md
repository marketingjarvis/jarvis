---
task: "Review Carousel"
order: 1
input: |
  - carousel_copy: Copy aprovada (carousel-copy.md)
  - carousel_html: HTML gerado (carousel.html)
output: |
  - review_report: Relatório de revisão com flags por slide e veredito final
---

# Review Carousel

Revisar o carrossel completo (copy + HTML) contra os critérios de qualidade da Jarvis Imóveis. Emitir veredito por slide e veredito final para o checkpoint de aprovação.

## Process

1. **Ler carousel-copy.md** para ter a referência de: ângulo, keyword, conteúdo esperado de cada slide, palavras accent, fundos alternados.

2. **Ler carousel.html** para verificar o que foi realmente gerado.

3. **Revisar cada slide** contra os critérios abaixo:

   **Critérios universais (todos os slides):**
   - [ ] Uma única ideia central por slide?
   - [ ] Fundo correto (escuro/claro conforme especificado na copy)?
   - [ ] Palavra accent em `#C9A84C` presente e visível?
   - [ ] Header bar com `@jarvisimoveis.br`?
   - [ ] Tom jornalístico (zero frases motivacionais)?

   **Critérios por slide:**
   - Slide 1 (Capa): Headline em maiúsculas, max 15 palavras, badge presente?
   - Slides 2, 3, 4: Dado numérico com fonte nomeada e visível?
   - Slide 4 (Dados): Comparativo, tabela ou segundo dado de autoridade?
   - Slide 7 (CTA): Keyword box com benefício específico? Nota de acesso gratuito?

   **Critérios da legenda Instagram:**
   - [ ] Gancho < 125 caracteres antes do "ver mais"?
   - [ ] Fontes citadas?
   - [ ] CTA com keyword?
   - [ ] 10-15 hashtags?

4. **Verificar critérios estruturais:**
   - [ ] Exatamente 7 slides no HTML?
   - [ ] Fundos alternam escuro/claro (não 3 iguais seguidos)?
   - [ ] Pelo menos 3 slides com dado numérico + fonte?

5. **Aplicar veto conditions automaticamente:**
   - QUALQUER slide com frase motivacional → ❌ reprovado
   - QUALQUER dado numérico sem fonte → ❌ reprovado (mínimo: ⚠️ ajuste obrigatório)
   - Número de slides diferente de 7 → ❌ reprovado

6. **Montar o relatório de revisão** no formato de output abaixo.

## Output Format

```
RELATÓRIO DE REVISÃO
Carrossel: {tema}
Ângulo: {ângulo}
Data: {data}
Revisor: Vera Veredito

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
REVISÃO POR SLIDE

SLIDE 1 — CAPA
{✅ / ⚠️ / ❌} Uma ideia central: {ok / problema}
{✅ / ⚠️ / ❌} Fundo correto (#0D1B2A): {ok / problema}
{✅ / ⚠️ / ❌} Palavra accent visível: {ok / problema}
{✅ / ⚠️ / ❌} Tom jornalístico: {ok / problema}
{✅ / ⚠️ / ❌} Headline max 15 palavras: {ok / problema}
{✅ / ⚠️ / ❌} Badge @jarvisimoveis.br: {ok / problema}
Veredito slide: ✅ aprovado / ⚠️ ajuste / ❌ reprovado

SLIDE 2 — CONTEXTO
{✅ / ⚠️ / ❌} Uma ideia central: ...
{✅ / ⚠️ / ❌} Dado com fonte nomeada: ...
{✅ / ⚠️ / ❌} Tom jornalístico: ...
Veredito slide: ...

(Repetir para slides 3, 4, 5, 6, 7)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
REVISÃO ESTRUTURAL

{✅ / ❌} Total de slides: {N}/7
{✅ / ❌} Alternância de fundos: {ok / problema: slides X, Y, Z iguais seguidos}
{✅ / ❌} Slides com dado + fonte: {N}/3 mínimo
{✅ / ❌} Keyword box no slide 7: {ok / problema}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
REVISÃO DA LEGENDA

{✅ / ⚠️ / ❌} Gancho < 125 chars: {N chars} — {ok / problema}
{✅ / ⚠️ / ❌} Fontes citadas: {ok / ausentes}
{✅ / ⚠️ / ❌} CTA com keyword: {ok / ausente}
{✅ / ⚠️ / ❌} Hashtags (10-15): {N} hashtags — {ok / problema}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
FLAGS OBRIGATÓRIOS (veto conditions)

{Lista de veto conditions violados, se houver. Se nenhum: "Nenhuma veto condition ativada."}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
VEREDITO FINAL

{✅ APROVADO — carrossel pronto para publicar.}
{ou}
{⚠️ APROVADO COM AJUSTES — X problemas não-críticos identificados. Ajustes recomendados antes de publicar: [lista]}
{ou}
{❌ REPROVADO — veto condition ativada. Motivo: [critério]. Slide afetado: [N]. Ação necessária: refazer [slide específico].}
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Quality Criteria

- [ ] Todos os 7 slides revisados individualmente com pelo menos 4 critérios verificados por slide
- [ ] Legenda revisada com todos os 4 critérios
- [ ] Revisão estrutural completa (total de slides, alternância, dado + fonte)
- [ ] Cada ⚠️ ou ❌ tem critério citado explicitamente
- [ ] Veredito final emitido sem ambiguidade (aprovado / aprovado com ajustes / reprovado)
- [ ] Relatório salvo em `output/review-report.md`
