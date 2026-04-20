---
task: "Create Carousel HTML"
order: 3
input: |
  - carousel_copy: Copy aprovada pelo usuário no checkpoint (carousel-copy.md)
  - research_report: Relatório com fontes e dados verificados
output: |
  - carousel_html: Arquivo HTML auto-contido com 7 slides + legenda, salvo em output/
---

# Create Carousel HTML

Gerar o arquivo HTML completo do carrossel usando a skill carrossel-infinito, aplicando a identidade visual da Jarvis Imóveis sobre a copy aprovada. O HTML deve abrir em qualquer navegador e ser capturado slide a slide.

## Process

1. **Ler carousel-copy.md** e extrair: ângulo, keyword, todos os slides (headline, texto, dado, palavra accent, fundo) e a legenda Instagram.

2. **Aplicar a identidade visual da Jarvis** em cada slide:
   - Paleta:
     - Fundo escuro primário: `#1B2A4A`
     - Fundo escuro profundo: `#0D1B2A`
     - Fundo claro: `#F5F0E8`
     - Accent/dourado: `#C9A84C`
     - Texto sobre escuro: `#FFFFFF`
     - Texto sobre claro: `#0D1B2A`
   - Fonte: Montserrat (via Google Fonts `@import`)
   - Pesos: 400 (body), 600 (subtítulo), 700 (headline), 800 (destaque)
   - Dimensões: 1080 × 1350px por slide (ratio 4:5 Instagram)

3. **Estrutura de cada slide**:
   - Header bar topo: `@jarvisimoveis.br` em dourado `#C9A84C`, 14px, Montserrat 600
   - Área de conteúdo: padding 60px laterais, 80px superior/inferior
   - Headline: Montserrat 800, uppercase, 52-64px, com palavra accent em `#C9A84C`
   - Corpo de texto: Montserrat 400, 26-30px, line-height 1.6
   - Dado/fonte: bloco destacado com borda esquerda 4px `#C9A84C`, texto 22px italic
   - Footer bar: número do slide + "JARVIS INTELIGÊNCIA IMOBILIÁRIA", 13px

4. **Slide 1 (Capa)** — layout especial:
   - Background `#0D1B2A` com textura sutil (gradiente radial escuro)
   - Headline centralizado, máximo 3 linhas, fonte 60-72px
   - Badge `"✦ @jarvisimoveis.br ✓"` em dourado, 16px, abaixo do headline
   - Logo JARVIS em rodapé

5. **Slide 7 (CTA)** — layout especial:
   - Background `#0D1B2A`
   - Marca `JARVIS INTELIGÊNCIA IMOBILIÁRIA` em dourado, 18px, topo centralizado
   - Headline CTA: Montserrat 800, 52px, branco
   - Keyword box: borda 2px `#C9A84C`, padding 20px 40px, texto `"Comenta [KEYWORD]..."` em 24px
   - Nota `"(Acesso gratuito por tempo limitado)"` em 18px, `#C9A84C`

6. **Legenda Instagram** — incluir abaixo dos slides no HTML:
   - Box separado com background `#1B2A4A`, padding 40px, largura 1080px
   - Título "LEGENDA INSTAGRAM" em dourado
   - Texto da legenda em branco, pré-formatado com quebras de parágrafo
   - Hashtags em `#C9A84C`

7. **Preview no HTML**:
   - Slides renderizados a 30% do tamanho original (324 × 405px) em grid 3 colunas
   - Seção de preview topo da página com todos os 7 slides visíveis
   - Botão "Ver slide completo" ou clique para expandir (opcional)
   - Slides em tamanho real logo abaixo (1080 × 1350px cada)

8. **Salvar o arquivo** como:
   - Nome: `CARROSSEL-{AAAA-MM-DD}-{tema-resumido}.html`
   - Local: `squads/carrossel-imoveis/output/`
   - Exemplo: `CARROSSEL-2026-04-15-custo-de-esperar.html`

## HTML Template Structure

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Carrossel — {tema} | Jarvis Inteligência Imobiliária</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&display=swap');
    
    :root {
      --navy: #1B2A4A;
      --dark: #0D1B2A;
      --light: #F5F0E8;
      --gold: #C9A84C;
      --white: #FFFFFF;
      --text-dark: #0D1B2A;
    }
    
    /* Reset + Base */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Montserrat', sans-serif; background: #111; }
    
    /* Preview Grid */
    .preview-section { padding: 40px; }
    .preview-grid { display: grid; grid-template-columns: repeat(3, 324px); gap: 16px; }
    .preview-slide { width: 324px; height: 405px; transform-origin: top left; overflow: hidden; }
    
    /* Slide Base */
    .slide {
      width: 1080px; height: 1350px;
      position: relative; overflow: hidden;
      font-family: 'Montserrat', sans-serif;
    }
    .slide.dark-primary { background: #1B2A4A; }
    .slide.dark-deep { background: #0D1B2A; }
    .slide.light { background: #F5F0E8; }
    
    /* Header bar */
    .slide-header {
      position: absolute; top: 0; left: 0; right: 0;
      padding: 20px 60px;
      display: flex; justify-content: space-between; align-items: center;
    }
    .slide-handle { color: #C9A84C; font-size: 14px; font-weight: 600; letter-spacing: 1px; }
    
    /* Content area */
    .slide-content { padding: 120px 60px 80px; height: 100%; display: flex; flex-direction: column; justify-content: center; }
    
    /* Typography */
    .slide-headline { font-size: 64px; font-weight: 800; text-transform: uppercase; line-height: 1.1; margin-bottom: 40px; }
    .slide-body { font-size: 28px; font-weight: 400; line-height: 1.7; }
    .accent { color: #C9A84C; }
    .on-dark { color: #FFFFFF; }
    .on-light { color: #0D1B2A; }
    
    /* Dado block */
    .dado-block {
      border-left: 4px solid #C9A84C;
      padding: 16px 24px; margin-top: 32px;
      font-size: 22px; font-style: italic; font-weight: 600;
    }
    
    /* Footer */
    .slide-footer {
      position: absolute; bottom: 0; left: 0; right: 0;
      padding: 20px 60px;
      display: flex; justify-content: space-between; align-items: center;
      font-size: 13px; font-weight: 600; letter-spacing: 1.5px;
      text-transform: uppercase;
    }
    
    /* Legenda box */
    .legenda-box {
      width: 1080px; margin: 40px auto;
      background: #1B2A4A; padding: 60px;
      color: #FFFFFF; font-family: 'Montserrat', sans-serif;
    }
    .legenda-title { color: #C9A84C; font-size: 18px; font-weight: 700; letter-spacing: 2px; margin-bottom: 32px; }
    .legenda-text { font-size: 18px; line-height: 1.8; white-space: pre-line; }
    .legenda-hashtags { color: #C9A84C; margin-top: 24px; font-size: 16px; }
  </style>
</head>
<body>
  <!-- PREVIEW SECTION (30% scale) -->
  <div class="preview-section">
    <h2 style="color:#C9A84C; font-family:Montserrat; margin-bottom:24px;">Preview — {tema}</h2>
    <div class="preview-grid">
      <!-- 7 mini slides aqui -->
    </div>
  </div>
  
  <!-- SLIDES EM TAMANHO REAL -->
  <!-- Slide 1 a 7 aqui -->
  
  <!-- LEGENDA INSTAGRAM -->
  <div class="legenda-box">
    <div class="legenda-title">LEGENDA INSTAGRAM</div>
    <div class="legenda-text">{legenda completa}</div>
    <div class="legenda-hashtags">{hashtags}</div>
  </div>
</body>
</html>
```

## Quality Criteria

- [ ] 7 slides exatos gerados, mesma ordem da copy aprovada
- [ ] Alternância de fundo escuro/claro respeitada
- [ ] Palavra accent em `#C9A84C` destacada no texto de cada slide
- [ ] Header bar com `@jarvisimoveis.br` em todos os 7 slides
- [ ] Footer com número do slide e "JARVIS INTELIGÊNCIA IMOBILIÁRIA"
- [ ] Legenda Instagram incluída no HTML abaixo dos slides
- [ ] Preview grid de 7 slides a 30% acima dos slides completos
- [ ] HTML auto-contido (único arquivo, sem CSS ou JS externos além de Google Fonts)
- [ ] Arquivo salvo como `CARROSSEL-{AAAA-MM-DD}-{tema}.html` em `output/`
- [ ] Google Fonts `@import` funcional para Montserrat

## Veto Conditions

Rejeitar e refazer se QUALQUER uma for verdade:
1. Algum slide tem background errado (não correspondendo ao especificado na copy)
2. Palavra accent ausente em qualquer slide
3. HTML tem dependências externas além de Google Fonts
4. Arquivo não foi salvo na pasta output/
