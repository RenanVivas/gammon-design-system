# Gammon Design System

Padrão visual do site do Instituto Presbiteriano Gammon (gammon.br/novosite): cores, tipografia (Inter), grade de 12 colunas, componentes HTML/CSS para o widget HTML do Elementor e padrão de animação.

## Estrutura

- `tokens.json` — fonte dos tokens (cores, tipografia, espaçamento, raios, sombras, durações)
- `tokens.css` — variáveis CSS geradas a partir do `tokens.json`
- `components/bundle.css` — classes `gm-*` de todos os componentes e animações
- `components/<Componente>/preview.html` — exemplo de HTML de cada componente (abra no navegador)
- `components/<Componente>/README.md` — regras de uso
- `docs-brandbook.md` — guia da marca: voz, cor, tipografia, grade, imagem, ícones, movimento
- `assets/logos/gammon-logo.svg` — logo oficial

## Uso no Elementor

1. Configurações do Site > CSS personalizado: cole `tokens.css` + `components/bundle.css`.
2. Carregue a Inter (400/500/600/700) pela Tipografia global ou via Google Fonts.
3. No widget HTML, envolva o conteúdo em `<div class="gm">…</div>` e use o HTML do preview do componente, trocando os blocos `.gm-photo` por `<img>`.
4. Animação de entrada em widgets nativos: Avançado > Efeitos de movimento > Fade In Up, duração Normal.

Componentes: Button, Eyebrow, SplitHeading, Header, Hero, SegmentCard, CampusCard, FeatureBlock, Accordion, StatCard, Marquee, Footer, Grid, Motion.
