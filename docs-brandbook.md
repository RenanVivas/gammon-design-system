O padrão visual do novo site do Instituto Presbiteriano Gammon (gammon.br/novosite): escola centenária de Lavras/MG, do berçário ao vestibular. O site é claro, verde e fotográfico; transmite tradição com acolhimento. Toda página nova parte dos tokens e componentes daqui.

## Voz e conteúdo

- Português do Brasil, frases curtas e afirmativas, na primeira pessoa do plural: "Acolhemos com cuidado e formamos com excelência".
- Títulos em duas partes, com a segunda parte em destaque de cor ou peso: "Educação que acolhe, forma e **transforma.**", "Um campus. **Muitas descobertas.**", "Mais que um espaço, um **legado.**". Termine títulos de impacto com ponto final.
- Caixa de frase em títulos e botões; CAIXA ALTA só no eyebrow.
- A identidade confessional aparece com naturalidade ("Dedicado à Glória de Deus e ao Progresso Humano", "Amar a Deus e ao próximo"), nunca em tom de pregação.
- Slogan da campanha atual: "Presença para toda a vida". Não use emoji. Use números só quando forem reais (30K+ alunos, nota 917.18 no ENEM).

## Cor

- Base clara: `surface-0` (página), `surface-100` e `surface-200` para seções e cards cinza. Texto em `text`, títulos em `ink`, apoio em `text-muted` (só a 16px+).
- O verde carrega a marca em três papéis: `green-brand` (verde claro da logo) para o botão primário e destaques de títulos grandes; `green-moss` (verde escuro da logo) para o título do hero; `green-forest` para a única seção verde cheia por página e para o degradê sobre fotos.
- `green-deep` é o verde para texto pequeno (eyebrow, links, rodapé): `green-brand` sobre branco tem só 2.45:1.
- `teal-night` é o escuro institucional (hero da página Institucional, overlays). Sobre ele e sobre `green-forest`, texto `on-dark` e acento `lime`.
- `lime` e `gold` são acentos raros do kit: nunca sobre fundo claro, nunca em área grande.
- Proporção por página: ~70% branco/cinza, ~20% fotografia, ~10% verde cheio.

## Tipografia

- Uma família: **Inter** (Google Fonts, pesos 400/500/600/700), stack `--font-sans`. Carregue com `<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">`.
- Títulos em peso 500 (nunca 800/900); a palavra de destaque sobe para 600–700 ou muda para verde. Escala: `hero` 56 · `h2` 40 · `h4` 35 · `h3` 34 · `h5` 24 · `body` 16 · `eyebrow` 13.
- Display só em seções de impacto: `display-lg` 67, `display-xl` 75 em `green-vivid`, `marquee` 96.
- No mobile reduza títulos em ~30% (56→38, 40→30).

## Grade e espaço

- `gm-container` de 1300px (`container`), 12 colunas, gap 20px (`space-3`), margem lateral `gutter`.
- Composições recorrentes: 6+6 (hero, pares), 5+7 (título fixo + lista), 4+4+4 (cards), 6+3+3 (mosaico com destaque).
- Seções com `space-7` (100px) de respiro vertical; seções de impacto com `space-8`. Padding de card `space-4` (30px).
- Breakpoints Elementor: 1024px e 767px.

## Forma, borda e sombra

- Cantos: `radius-md` (15px) em cards, seções em caixa e fotos grandes; `radius-sm` (8px) em fotos dentro de cards; `radius-pill` em todo botão e chip; `radius-full` no botão-ícone com seta.
- Bordas quase não aparecem: só filetes de 1px `line` no acordeão e no cabeçalho dividido. Separe por fundo (`surface-100` vs `surface-0`), não por contorno.
- Sombras discretas: `shadow-md` em cards brancos sobre cinza, `shadow-sm` no botão-ícone, `shadow-lg` só em modal/drawer.

## Imagem

- Fotografia real de alunos com uniforme verde e branco, luz natural, campus ao fundo. Fotos sempre com cantos arredondados, exceto o hero de largura total.
- Sobre foto, use degradê de baixo para cima em `green-forest` (cards) ou da esquerda para a direita em `teal-night` (hero) para garantir leitura do texto branco.
- O mapa ilustrado 3D do campus é a única ilustração; não misture com ícones coloridos ou clipart.

## Ícones

- Ícones de linha fina (stroke 1.8, cantos arredondados), monocromáticos, em `currentColor`: seta → para avançar, seta ↗ em cards-link, selo/pin no eyebrow soft. Sem emoji e sem ícones preenchidos coloridos.

## Movimento

- Entradas ao rolar com `fadeInUp` (padrão), `fadeIn` (imagens) e `fadeInLeft` (coluna esquerda), `dur-enter` 1.25s, easing `ease`, cascata de 100ms.
- Hover: 0.3s para cor/fundo/sombra (`dur-base`), 0.4s para deslocamento (`dur-move`): seta +4px, ícone gira 45°, foto aproxima 6%.
- Contínuo só no marquee de slogan e nos elementos ambientes do mapa. Contadores sobem em 1.8s.
- Respeite `prefers-reduced-motion`. Detalhes e demonstração no componente Motion.

## Como usar no Elementor

1. Em Configurações do Site > CSS personalizado, cole `tokens.css` (gerado por este sistema) e `components/bundle.css`.
2. Carregue a Inter (Configurações do Site > Tipografia global, ou o `<link>` acima).
3. Em cada widget HTML, envolva o conteúdo em `<div class="gm">…</div>` e use o HTML do preview do componente, trocando `.gm-photo` por `<img>` reais.
4. Para animação de entrada em widgets nativos, use Avançado > Efeitos de movimento com Fade In Up, duração Normal.
5. Logo: sempre o arquivo `assets/Logos/gammon-logo.svg`, nunca recriado em texto.
