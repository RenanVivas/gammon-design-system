# Hero

Duas versões.

**Hero em caixa** (`gm-hero`, home): container arredondado `radius-md` sobre `surface-100`, texto à esquerda e, à direita, a foto de alunos recortada sobre um arco verde (`green-forest` + `green-brand` translúcido). Ordem: prova social (avatares + 30K+), título `hero` 56px em `green-moss` com a última palavra em 600, lead, botão primário. Troque `.gm-hero__arc` pela foto PNG recortada.

**Hero com foto** (`gm-hero-photo`, Institucional): foto em largura total com degradê `teal-night` da esquerda para a direita, eyebrow em `lime` (Tradição que constrói o amanhã), título 56px branco com a palavra-chave em bold (Mais que um espaço, um **legado.**), parágrafo e botão primário com seta. Altura pelo conteúdo, mínimo 520px; nunca `100vh`.

Os dois entram com `fadeInUp` em cascata (eyebrow → título → texto → botão, 100ms de intervalo).
