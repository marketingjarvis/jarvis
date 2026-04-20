---
task: "Generate Carousel Angles"
order: 1
input: |
  - research_report: Relatório com tendências classificadas (de Tiago Tendências)
  - selected_trend: Tendência escolhida pelo usuário no checkpoint de seleção
output: |
  - angles: 5 ângulos distintos com hook de exemplo, driver emocional e justificativa
---

# Generate Carousel Angles

Gerar 5 ângulos emocionalmente distintos para a tendência de mercado imobiliário selecionada. Cada ângulo é uma lente diferente para contar a mesma história — o usuário escolhe o ângulo antes de qualquer copy ser escrita.

## Process

1. **Ler o research-report.md** e identificar a tendência selecionada pelo usuário, incluindo o dado de gancho e os dados adicionais.

2. **Identificar os gatilhos emocionais disponíveis** para esta tendência específica. Considerar os 6 gatilhos do mercado imobiliário:
   - Medo de ficar para trás ("Seus concorrentes já fizeram isso")
   - Urgência baseada em dado ("Cada mês que passa, o preço sobe X%")
   - Curiosidade intelectual ("O dado que ninguém no mercado imobiliário está mostrando")
   - Orgulho profissional ("Maceió fez o que São Paulo não conseguiu")
   - Revolta produtiva ("Por que o comprador entrega 30% a mais e ninguém fala nisso")
   - Esperança informada ("3 sinais de que 2026 pode ser o melhor ano para comprar")

3. **Gerar 5 ângulos distintos**, cada um com:
   - Nome do ângulo
   - Driver emocional (qual gatilho usa)
   - Hook de capa de exemplo (a headline que iria no slide 1)
   - Arco narrativo em 1 frase (como o carrossel se desenvolve)
   - Por que esse ângulo funciona para o público da Jarvis (compradores/investidores Maceió)

4. **Garantir diversidade real entre os ângulos**:
   - Ângulo 1: Tendência interpretada (dado + análise de impacto)
   - Ângulo 2: Tese contraintuitiva (desafiar o senso comum com dado)
   - Ângulo 3: Urgência / custo de esperar (dado de escassez ou valorização)
   - Ângulo 4: Educativo / desmistificação (explicar o que poucos entendem)
   - Ângulo 5: Futuro / previsão (onde o mercado vai e o que fazer agora)

5. **Apresentar os 5 ângulos** para o usuário escolher no checkpoint seguinte.

## Output Format

```
ÂNGULOS PARA O CARROSSEL
Tendência: {tendência selecionada}
Dado de gancho: {dado principal}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ÂNGULO 1: {Nome do ângulo}
Driver emocional: {gatilho}
Hook de capa: "{headline da capa}"
Arco narrativo: {1 frase descrevendo como o carrossel evolui}
Por que funciona: {1-2 frases de justificativa}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ÂNGULO 2: {Nome}
...

(Repetir para todos os 5 ângulos)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Output Example

```
ÂNGULOS PARA O CARROSSEL
Tendência: Maceió cresce 122% — maior alta do Nordeste
Dado de gancho: "122% de crescimento acumulado — a maior alta entre as capitais do NE"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ÂNGULO 1: Tendência Interpretada — "Por Que Maceió Virou o Novo Centro do Mercado Imobiliário"
Driver emocional: Curiosidade intelectual + orgulho local
Hook de capa: "Maceió cresceu 122%. E a maioria dos investidores ainda não entendeu por quê."
Arco narrativo: Contexto → 3 fatores estruturais → Comparativo com outras capitais → O que muda para quem investe agora → Ação
Por que funciona: Investidores de fora de Maceió compartilham (orgulho local / oportunidade); compradores locais se sentem validados em sua escolha. Alta probabilidade de share.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ÂNGULO 2: Tese Contraintuitiva — "O Que São Paulo Perdeu e Maceió Ganhou"
Driver emocional: Contradição de senso comum
Hook de capa: "Você investiria em São Paulo ou Maceió? O mercado já respondeu."
Arco narrativo: Percepção comum (SP é melhor) → Dado que inverte (Maceió cresceu mais) → 3 razões estruturais → Comparativo de rentabilidade → Conclusão
Por que funciona: Desafia o que o leitor acredita — força o swipe para entender a contradição. Alto potencial de salvamento.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ÂNGULO 3: Urgência — "O Custo de Esperar Para Comprar em Maceió"
Driver emocional: Medo de perda / urgência baseada em dado
Hook de capa: "Cada mês que você espera para comprar em Maceió, o preço do metro quadrado sobe R$X."
Arco narrativo: Dado de valorização → Simulação de quanto custou esperar 12 meses → Estoque caindo 24% → Projeção dos próximos 12 meses → O que fazer agora
Por que funciona: Comprador que está "pesquisando ainda" se reconhece e sente a urgência baseada em dado real, não em pressão de vendedor.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ÂNGULO 4: Educativo — "5 Dados Sobre o Mercado de Maceió Que Todo Comprador Deveria Saber"
Driver emocional: Curiosidade intelectual / empoderamento
Hook de capa: "5 dados sobre o mercado imobiliário de Maceió que mudam a forma de comprar."
Arco narrativo: 5 slides com um dado surpreendente cada → Interpretação prática de cada dado → CTA para quem quer aprofundar
Por que funciona: Formato de lista é altamente salvável. O seguidor vira referência ao repostar/compartilhar.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ÂNGULO 5: Previsão — "O Mercado Imobiliário de Maceió em 2027: O Que os Dados Já Mostram"
Driver emocional: Esperança informada / visão de futuro
Hook de capa: "3 sinais do mercado imobiliário que mostram onde Maceió estará em 2027."
Arco narrativo: Sinal 1 (dado atual) → Sinal 2 (dado atual) → Sinal 3 (dado atual) → O que o padrão histórico sugere → Posicionamento estratégico
Por que funciona: Conteúdo de visão de longo prazo gera autoridade e é compartilhado com decisores.
```

## Quality Criteria

- [ ] 5 ângulos distintos com drivers emocionais diferentes
- [ ] Hook de capa de exemplo para cada ângulo (específico, não genérico)
- [ ] Cada ângulo usa o dado de gancho da tendência selecionada
- [ ] Arco narrativo claro em 1 frase por ângulo
- [ ] Nenhum ângulo repete o driver emocional de outro

## Veto Conditions

Rejeitar e refazer se QUALQUER uma for verdade:
1. Dois ou mais ângulos têm o mesmo driver emocional
2. Algum hook de capa é genérico (poderia ser de qualquer cidade/imobiliária)
