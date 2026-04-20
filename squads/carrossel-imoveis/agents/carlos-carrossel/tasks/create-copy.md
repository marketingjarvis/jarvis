---
task: "Create Carousel Copy"
order: 2
input: |
  - angles: Os 5 ângulos gerados
  - selected_angle: Ângulo confirmado pelo usuário no checkpoint
  - research_report: Relatório com todos os dados disponíveis
output: |
  - carousel_copy: Copy completa de 7 slides + legenda Instagram + hashtags
---

# Create Carousel Copy

Escrever a copy completa do carrossel: 7 slides estruturados (capa + 5 conteúdo + CTA) com profundidade analítica de 3 camadas, dados verificados e CTA com keyword. Esta copy passa por checkpoint de aprovação do usuário ANTES do HTML ser gerado.

## Process

1. **Identificar o ângulo selecionado** em angles.md e o driver emocional que o ancora.

2. **Executar análise em 3 camadas** para o tema:
   - Camada 1 — Superfície: o que todo mundo está vendo (a notícia em si)
   - Camada 2 — Estrutura: os movimentos econômicos, demográficos ou regulatórios por trás
   - Camada 3 — Significado: o que muda no jogo do comprador/investidor em Maceió

3. **Escrever slide a slide**, seguindo a estrutura do ângulo escolhido:
   - Slide 1 (Capa): Hook visual + headline de impacto. Max 15 palavras. Uma palavra em accent color.
   - Slide 2 (Contexto): Dado atual com fonte. Introduz o que está acontecendo.
   - Slide 3 (Aprofundamento): A camada 2 — o que poucos percebem por trás do dado.
   - Slide 4 (Dados/Prova): Tabela, comparativo ou segundo dado de autoridade. Fonte nomeada.
   - Slide 5 (Impacto): O que muda para o comprador/investidor em Maceió. Consequência prática.
   - Slide 6 (Ação): O que fazer agora com essa informação. Orientação concreta.
   - Slide 7 (CTA): Keyword box + legenda. "Comenta [KEYWORD] e recebe [benefício] na DM."

4. **Testar cada slide** contra estes critérios antes de avançar:
   - Uma ideia central por slide?
   - Tom jornalístico (não motivacional)?
   - Dado com fonte quando aplicável?
   - Palavra em accent color identificada?
   - Fundo sugerido (escuro/claro) para alternância?

5. **Escrever a legenda Instagram**:
   - Gancho (primeiras 125 chars — antes do "ver mais")
   - 2-3 parágrafos de contexto
   - Fontes usadas
   - CTA com keyword
   - Hashtags (10-15, mix nicho + médio + amplo)

## Output Format

```
COPY DO CARROSSEL
Ângulo: {ângulo selecionado}
Driver emocional: {gatilho}
KEYWORD: {palavra para CTA}
Identidade: Jarvis Inteligência Imobiliária | @jarvisimoveis.br | Montserrat

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 1 — CAPA
Fundo: escuro (#0D1B2A)
Headline: {headline em maiúsculas, max 15 palavras}
Palavra accent: [{palavra em dourado #C9A84C}]
Subtítulo: {frase de contexto, opcional}
Badge: "✦ @jarvisimoveis.br ✓"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 2 — CONTEXTO
Fundo: escuro (#1B2A4A)
Título do slide: {título em negrito}
Palavra accent: [{palavra}]
Texto: {conteúdo do slide}
Dado: "{dado específico}" — Fonte: {publicação}, {data}
Seta items: → {ponto 1} / → {ponto 2} (opcional)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 3 — APROFUNDAMENTO
Fundo: claro (#F5F0E8)
Título do slide: {título}
Palavra accent: [{palavra}]
Texto: {conteúdo — camada 2, o que poucos veem}
Dado: "{dado}" — Fonte: {publicação}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 4 — DADOS / PROVA
Fundo: escuro (#0D1B2A)
Título do slide: {título}
Palavra accent: [{palavra}]
Texto: {comparativo, tabela ou dado de autoridade}
Fonte: {publicação + data}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 5 — IMPACTO
Fundo: claro (#F5F0E8)
Título do slide: {título}
Palavra accent: [{palavra}]
Texto: {o que muda para o comprador/investidor em Maceió}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 6 — AÇÃO
Fundo: escuro (#1B2A4A)
Título do slide: {título}
Palavra accent: [{palavra}]
Texto: {o que fazer agora — orientação concreta, não venda}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 7 — CTA
Fundo: escuro (#0D1B2A)
Marca: JARVIS INTELIGÊNCIA IMOBILIÁRIA
Headline CTA: {headline de fechamento}
Keyword box: "Comenta [{KEYWORD}] e recebe {benefício} direto na DM."
Nota: "(Acesso gratuito por tempo limitado)"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
LEGENDA INSTAGRAM

{Gancho — máx 125 chars, antes do "ver mais"}

{Parágrafo 1 — contexto em 2-3 frases}

{Parágrafo 2 — análise em 2-3 frases}

Fontes: {publicação 1}, {publicação 2}

Conteúdo produzido com IA por Jarvis Inteligência Imobiliária.

💬 Comenta "{KEYWORD}" e recebe {benefício} direto na DM.

#{hashtag1} #{hashtag2} #{hashtag3} ... (10-15 hashtags)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Output Example

```
COPY DO CARROSSEL
Ângulo: Urgência — O Custo de Esperar Para Comprar em Maceió
Driver emocional: Medo de perda / urgência baseada em dado
KEYWORD: MACEIO
Identidade: Jarvis Inteligência Imobiliária | @jarvisimoveis.br | Montserrat

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 1 — CAPA
Fundo: escuro (#0D1B2A)
Headline: "MACEIÓ CRESCEU 122%. QUEM ESPEROU PERDEU [QUANTO]."
Palavra accent: [122%] e [QUANTO]
Badge: "✦ @jarvisimoveis.br ✓"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 2 — CONTEXTO
Fundo: escuro (#1B2A4A)
Título: O MERCADO QUE NINGUÉM ESTAVA OLHANDO
Palavra accent: [122%]
Texto: "O mercado imobiliário de Maceió acumulou 122% de crescimento. O metro quadrado que estava a R$8.000 em 2022 chegou a R$13.260 em 2025."
Dado: "10,5% de valorização em 12 meses" — Fonte: Brain Consultoria, fev/2026
→ Nordeste lidera intenção de compra em 2026
→ Estoque caiu 24% — menos opções, maior pressão de preço

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 3 — APROFUNDAMENTO
Fundo: claro (#F5F0E8)
Título: A CONTA QUE NINGUÉM FAZ
Palavra accent: [esperar]
Texto: "Esperar 12 meses para comprar um imóvel de R$500 mil em Maceió custou, em média, R$52.500 a mais — só em valorização. Sem contar a inflação, a correção do financiamento e os aluguéis pagos no período."
Dado: "R$3,7 bilhões em VGV lançado em 2025" — Fonte: movimentoeconomico.com.br, fev/2026

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 4 — DADOS / PROVA
Fundo: escuro (#0D1B2A)
Título: O ESTOQUE QUE ESTÁ ACABANDO
Palavra accent: [24%]
Texto: "O estoque disponível em Maceió caiu 24% em 2025. Restam 3.745 unidades. Em bairros como Jatiúca e Ponta Verde, a disponibilidade é crítica. Quando a oferta cai e a demanda sobe, a fórmula é uma só."
Fonte: Brain Consultoria, movimentoeconomico.com.br, fev/2026

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 5 — IMPACTO
Fundo: claro (#F5F0E8)
Título: O QUE ISSO SIGNIFICA PARA VOCÊ
Palavra accent: [comprar]
Texto: "Se você está na fase de pesquisa, saiba: cada mês que passa, há menos imóveis disponíveis e os que restam custam mais. Não é pressão de vendedor. É matemática de mercado. Compradores bem informados usam isso a seu favor."

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 6 — AÇÃO
Fundo: escuro (#1B2A4A)
Título: 3 COISAS QUE COMPRADORES INTELIGENTES ESTÃO FAZENDO AGORA
Palavra accent: [inteligentes]
Texto:
"→ Definiram orçamento real (não o sonhado) antes de visitar qualquer imóvel
→ Compararam custo de alugar vs. financiar no nível atual de juros
→ Mapearam os bairros com maior liquidez — não apenas o mais bonito"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SLIDE 7 — CTA
Fundo: escuro (#0D1B2A)
Marca: JARVIS INTELIGÊNCIA IMOBILIÁRIA
Headline CTA: "QUER SABER SE AGORA É A HORA DE COMPRAR EM MACEIÓ?"
Keyword box: "Comenta [MACEIO] e recebe nosso Guia de Compra Inteligente direto na DM."
Nota: "(Acesso gratuito por tempo limitado)"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
LEGENDA INSTAGRAM

Maceió cresceu 122% no mercado imobiliário. Quem esperou para comprar pagou R$52 mil a mais por um imóvel de R$500 mil.

O metro quadrado foi de R$8.000 em 2022 para R$13.260 em 2025. Valorização de 10,5% só nos últimos 12 meses. E o estoque disponível caiu 24% no mesmo período.

Não é pressão de vendedor — é a matemática do mercado. Compradores que entendem os dados tomam decisões melhores. Por isso fizemos esse carrossel.

Fontes: Brain Consultoria, movimentoeconomico.com.br, apartamentoavendaemmaceio.com

Conteúdo produzido com IA por Jarvis Inteligência Imobiliária.

💬 Comenta "MACEIO" e recebe nosso Guia de Compra Inteligente direto na DM.

#mercadoimobiliario #maceio #alagoas #investimentoimobiliario #comprardeimovel #imoveisnordeste #valorizacao #jarvisimoveis #inteligenciaimobiliaria #imoveis2026 #nordeste #financiamentoimobiliario
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Quality Criteria

- [ ] 7 slides exatos: capa + 5 conteúdo + CTA
- [ ] Pelo menos 3 slides têm dado numérico com fonte nomeada
- [ ] Fundo alterna entre escuro e claro (não 3 iguais seguidos)
- [ ] Palavra em accent color (#C9A84C) identificada em cada slide
- [ ] Keyword box no slide 7 com benefício específico
- [ ] Legenda com gancho < 125 chars, fontes e hashtags (10-15)
- [ ] Tom jornalístico em todos os slides (zero frase motivacional)

## Veto Conditions

Rejeitar e refazer se QUALQUER uma for verdade:
1. Algum slide tem frase motivacional ("realize seu sonho", "conquiste seu imóvel")
2. Dado numérico sem fonte nomeada em qualquer slide
3. Menos de 7 slides ou mais de 7 slides entregues
