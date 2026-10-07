# Button

Botões em pílula (`radius-pill`) com 48px de altura mínima e padding 12px 28px; o site não usa botões quadrados.

- **Primário** `gm-btn--primary`: fundo `green-brand`, texto branco 15px bold. Uma vez por dobra, para a ação principal (Fazer matrícula). Hover escurece para `green-pine`.
- **Escuro** `gm-btn--dark`: `ink`, texto 16px regular. Ações secundárias em fundo claro (Ver mais).
- **Claro** `gm-btn--light`: branco sobre `surface-200`, `ink` ou `teal-night` (Inscreva-se, Conheça a Capelania).
- **Contorno** `gm-btn--ghost-dark`: só sobre foto ou fundo escuro.
- **Ícone** `gm-icon-btn`: círculo 48px (`radius-full`) com seta; `--glass` sobre foto, `--sm` (34px) dentro de cards.

Texto em verbo + objeto, caixa de frase. A seta é opcional e desliza 4px no hover (`dur-move`).

HTML: `<a class="gm-btn gm-btn--primary" href="…">Fazer matrícula</a>`. Envolva a página (ou o widget) em `.gm` para herdar fonte e reset.
