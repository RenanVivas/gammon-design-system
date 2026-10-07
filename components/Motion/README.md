# Motion

O movimento do site é calmo e de entrada: os blocos aparecem ao rolar, nada pisca nem quica.

- **Entradas** (Elementor “Entrance animation”): `fadeInUp` na maioria dos blocos de texto, `fadeIn` em imagens e fundos, `fadeInLeft` em colunas da esquerda. Duração `dur-enter` 1.25s (normal) ou `dur-enter-slow` 2s em imagens grandes, easing `ease`. Em cascata, 100ms entre itens (`gm-d1`…`gm-d4`).
- **Títulos de impacto**: revelação por máscara de baixo para cima (`gm-anim--mask`) ou cor que preenche a frase conforme a rolagem (Um campus. Muitas descobertas.).
- **Hover**: cor e fundo em `dur-base` 0.3s; deslocamentos (seta +4px, rotação 45° do ícone, zoom 6% da foto em 0.8s) em `dur-move` 0.4s.
- **Contínuo**: só o marquee de texto (28s linear) e elementos ambientes do mapa do campus (nuvens à deriva, pessoas em rota). Nunca em conteúdo que precisa ser lido.
- **Contador**: números sobem até o valor em 1.8s com ease-out.

Sempre respeite `prefers-reduced-motion`: as classes `gm-anim` e o marquee param. No Elementor use Avançado > Efeitos de movimento > Animação de entrada = Fade In Up, duração Normal; no widget HTML use as classes `gm-anim gm-anim--up` + um IntersectionObserver que adiciona a animação ao entrar na tela.
