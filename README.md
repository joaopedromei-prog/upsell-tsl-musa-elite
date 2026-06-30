# Upsell TSL — Acompanhamento Musa Elite

Página de vendas (Text Sales Letter) gerada a partir do roteiro de VSL
`Upsell 1 - Acompanhamento Musa Elite`. Estática, autossuficiente, mobile-first,
pt-BR. Mesma identidade visual do funil (`downsell-tsl-bum`): fonte Inter,
rosa `#EC4899`, CTA verde, coluna 640px.

## Arquivos
- `index.html` — a página completa (16 seções)
- `styles.css` — design system da marca + componentes novos
- `script.js` — ano dinâmico do rodapé
- `assets/` — imagens

## ⚠️ O QUE TROCAR ANTES DE PUBLICAR

### 1. Links de checkout (3 botões de compra)
Procure por `<!-- TROCAR pelo link de checkout` no `index.html`.
Os 3 botões `.cta-btn` estão com `href="#"`. Troque pelo link de **aceite do upsell**.

### 2. Link de recusa (2 links "Não, obrigada")
Procure por `<!-- TROCAR pela URL do downsell`.
Hoje apontam pra `../downsell-tsl-bum/index.html`. Ajuste pra URL real do downsell no funil.

### 3. Imagens dos depoimentos (placeholders)
Coloque os arquivos reais em `assets/` com estes nomes (a página troca sozinha):
- `roberta.jpg` — foto da Roberta (hoje mostra um círculo rosa com "R")
- `daniela.jpg` — foto da Daniela (círculo "D"). O áudio é um mock visual — trocar pelo player/print real.
- `patricia-antes.jpg` / `patricia-depois.jpg` — antes/depois (hoje mostram caixas placeholder)
- `murilo.jpg` — foto do Murilo na assinatura (círculo "M")

### 4. Páginas legais
O rodapé linka `privacidade.html`, `termos.html`, `contato.html` — criar ou ajustar.

## Preço configurado
De R$ 437 → cashback R$ 147 do BumbumFlix → **R$ 290 à vista / 12x de R$ 30**.
(Âncoras: consultoria R$1.500–2.000 e preço cheio R$897.) Para mudar, edite o bloco `.price-callout`.

## Deploy
É só HTML/CSS/JS estático. Suba a pasta inteira em qualquer host estático
(Vercel, Netlify, etc.) ou no builder do funil.

## Pré-visualizar PDF
A página foi feita pra web, mas renderiza bem em PDF via Chrome headless:
`/Applications/Google Chrome.app/Contents/MacOS/Google Chrome --headless --print-to-pdf=out.pdf --no-pdf-header-footer index.html`
