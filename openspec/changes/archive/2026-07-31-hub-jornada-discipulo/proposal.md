## Why

Não havia um ponto de entrada único para as três trilhas do discipulado. O hub apresenta visualmente a jornada completa (Estações 1–3 e o destino DISCÍPULO) e direciona o usuário a cada trilha publicada, em uma página acolhedora e responsiva.

## What Changes

- Cria um novo site estático hub "A Jornada do Discípulo" em `/root/projetos/trilhas`:
  - `index.html` — estrutura semântica da página (header, hero, 3 estações, apex e footer).
  - `css/tokens.css` — design tokens neutros e paleta por estação via `data-etapa`.
  - `css/estilo.css` — estilos dos cards, conectores, apex, responsivo e acessibilidade.
  - `favicon.svg` e `og-image.svg` — identidade para navegador e compartilhamento.
- Adiciona links de navegação para as trilhas publicadas:
  - Estação 1 → `https://ismaelmmachado.github.io/trilha_de_novos/index.html`.
  - Estação 2 → `https://ismaelmmachado.github.io/trilha_praticando_o_caminho/index.html`.
  - Estação 3 (Fundamentos da Fé) → card visível sem link, com badge "Em breve".
- O site será publicado via GitHub Pages em `https://ismaelmmachado.github.io/trilhas_discipulado/`.

## Capabilities

### New Capabilities
- `journey-hub`: página hub que apresenta as três estações da Jornada do Discípulo, conecta visualmente a caminhada até a cruz e direciona o usuário às trilhas publicadas.

### Modified Capabilities
- Nenhuma. Os sites existentes (`trilha_de_novos` e `trilha_praticando_o_caminho`) não são alterados.

## Impact

- **Código:** novos arquivos na raiz de `/root/projetos/trilhas` (HTML/CSS/SVG). Nenhum arquivo existente é modificado.
- **Deploy:** novo site estático em GitHub Pages (`ismaelmmachado/trilhas_discipulado`), sem build step.
- **Dependências:** nenhuma (HTML + CSS puro). Fontes externas via Google Fonts (Playfair Display e Inter).
- **Sistemas:** independência total dos repositórios das trilhas existentes.
