---
task: "Find and Rank Real Estate Trends"
order: 1
input: |
  - research_focus: Tema/foco da pesquisa definido pelo usuário no checkpoint
  - time_range: Período a ser coberto (últimas 24h / 7 dias / 1 mês / evergreen)
output: |
  - research_report: Relatório estruturado com 5 tendências classificadas, dados verificados e scores editoriais
---

# Find and Rank Real Estate Trends

Pesquisar e classificar as 5 melhores tendências do mercado imobiliário (Maceió, Nordeste, Brasil) para desenvolver em carrossel viral no Instagram.

## Process

1. **Ler o research-focus.md** para entender o tema e período definidos pelo usuário. Se o foco for amplo (ex: "qualquer tendência"), pesquisar as categorias padrão abaixo.

2. **Executar 6 buscas focadas** usando WebSearch (adaptar ao foco do usuário):
   - `"mercado imobiliário Maceió [período] dados valorização"`
   - `"imóveis Alagoas Nordeste tendência [período] compra investimento"`
   - `"SECOVI CBIC FipeZAP dados imobiliários [período]"`
   - `"financiamento imobiliário juros [período] impacto comprador"`
   - `"novos bairros lançamentos Maceió [período]"`
   - `"perfil comprador imóvel Brasil [período] pesquisa"`

3. **Filtrar por qualidade**: Aceitar apenas fontes com pelo menos um destes critérios:
   - Publicação especializada (Imobi Report, SECOVI, CBIC, FipeZAP, Brain Consultoria, movimentoeconomico.com.br)
   - Dado primário com metodologia declarada
   - Data de publicação dentro do período solicitado

4. **Extrair dados de gancho** de cada tendência: o número ou fato mais surpreendente que vai virar headline da capa do carrossel.

5. **Avaliar score editorial** de cada tendência (1-10) com base em:
   - Dado surpreendente ou contraintuitivo? (+3)
   - Relevante para compradores/investidores em Maceió? (+3)
   - Não saturado no Instagram imobiliário? (+2)
   - Tem pelo menos 2 fontes independentes? (+2)

6. **Montar o relatório** com as 5 melhores tendências no formato de output abaixo.

## Output Format

```
RESEARCH REPORT — MERCADO IMOBILIÁRIO
Foco: {foco do usuário}
Período: {período}
Preparado: {AAAA-MM-DD}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TENDÊNCIA 1: {título da tendência}
Score editorial: X/10

DADO DE GANCHO (para o hook da capa):
"{número/fato surpreendente}" — Fonte: {publicação}, {data}
URL: {url}

CONTEXTO:
{2-3 frases explicando o que está acontecendo e por quê agora}

DADOS ADICIONAIS:
- {dado 2} — Fonte: {publicação}, {data}
- {dado 3} — Fonte: {publicação}, {data}

IMPACTO PARA O PÚBLICO-ALVO (compradores/investidores Maceió):
{1-2 frases de impacto prático}

ÂNGULO SUGERIDO: {uma frase descrevendo o melhor ângulo para o carrossel}
Confiança geral: alta/média/baixa

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TENDÊNCIA 2: {título}
Score editorial: X/10
...

(Repetir para todas as 5 tendências)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

RECOMENDAÇÃO: Tendência {N} (score X/10) — {justificativa em 1 frase}
```

## Output Example

```
RESEARCH REPORT — MERCADO IMOBILIÁRIO
Foco: Valorização e investimento em Maceió
Período: Últimos 30 dias
Preparado: 2026-04-15

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TENDÊNCIA 1: Maceió lidera valorização no Nordeste com crescimento de 122%
Score editorial: 9/10

DADO DE GANCHO:
"Maceió registrou 122% de crescimento imobiliário acumulado — a maior alta entre as capitais do Nordeste."
Fonte: apartamentoavendaemmaceio.com, março 2026
URL: https://www.apartamentoavendaemmaceio.com/2026/03/122-de-crescimento-maceio.html

CONTEXTO:
O mercado imobiliário de Maceió encerrou 2025 com crescimento de 21% nas vendas de imóveis verticais, totalizando VGV de R$3,7 bilhões. O metro quadrado subiu 10,5% em 12 meses, chegando a R$13.260. O estoque disponível caiu 24%, criando pressão positiva sobre os preços em 2026.

DADOS ADICIONAIS:
- "NE lidera intenção de compra em 2026" — Fonte: Brain Consultoria / movimentoeconomico.com.br, fev 2026
- "Imóveis bem localizados têm potencial de 8-18% de valorização ao ano" — Fonte: Sebrae-PR, mar 2026

IMPACTO PARA O PÚBLICO-ALVO:
Compradores que adquiriram imóvel em Maceió em 2023 já viram valorização de dois dígitos. Investidores que ainda não entraram no mercado de Maceió estão pagando mais por cada mês de espera.

ÂNGULO SUGERIDO: Dado contraintuitivo — "Por que Maceió cresceu mais que São Paulo no mercado imobiliário"
Confiança geral: alta

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TENDÊNCIA 2: Estoque de imóveis em Maceió despenca 24% — o que isso significa para quem compra
Score editorial: 8/10

DADO DE GANCHO:
"O estoque de imóveis disponíveis em Maceió fechou 2025 com queda de 24% — apenas 3.745 unidades."
Fonte: Brain Consultoria via movimentoeconomico.com.br, fev 2026

CONTEXTO:
Quando a demanda cresce mais rápido que a oferta, o mercado reage com redução de estoque e pressão positiva sobre os preços. Quem espera para comprar tende a pagar mais. O cenário atual é de escassez: menos opções, preços mais altos, e prazo menor para negociar.

DADOS ADICIONAIS:
- Vendas cresceram 21% enquanto lançamentos não acompanharam o ritmo — desequilíbrio estrutural
- Bairros como Jatiúca e Ponta Verde têm disponibilidade crítica (menos de 5 unidades em alguns empreendimentos)

IMPACTO PARA O PÚBLICO-ALVO:
Cada mês que passa, há menos imóveis disponíveis e os preços sobem. Quem está na fase de pesquisa precisa entender que a janela de oportunidade está se fechando.

ÂNGULO SUGERIDO: Urgência baseada em dado — "A conta simples que mostra que esperar para comprar em Maceió sai mais caro"
Confiança geral: média-alta
```

## Quality Criteria

- [ ] 5 tendências entregues com temas distintos (não variações do mesmo)
- [ ] Cada tendência tem dado de gancho com fonte nomeada e URL
- [ ] Score editorial (1-10) com justificativa para cada tendência
- [ ] Confiança (alta/média/baixa) atribuída a cada tendência
- [ ] Ao menos 3 tendências com dado local de Maceió/AL
- [ ] Formato padrão respeitado (separadores, seções, recomendação final)

## Veto Conditions

Rejeitar e refazer se QUALQUER uma for verdade:
1. Alguma tendência não tem dado específico com fonte nomeada (só "especialistas afirmam")
2. Menos de 5 tendências entregues ou mais de 3 tendências sobre o mesmo tema
