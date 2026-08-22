## MODIFIED Requirements

### Requirement: Identidade visual da jornada

A página DEVE (MUST) apresentar a metáfora da caminhada de base para o topo inspirada no pôster "A Jornada do Discípulo": paleta em bandas horizontais — cabeçalho em petróleo-escuro (`--zona-petroleo-escuro`) e hero em gradiente de petróleo para petróleo-claro no topo, painel creme (estações), faixa dourada e base verde (footer) — conectores ligando as estações e o bloco do destino "DISCÍPULO" no topo do hero, logo após o badge, com a frase "Esteja com Jesus, Torne-se como Ele, Faça como Ele fez.", a fórmula "SER + FAZER + SABER" e os ícones ❤️ + 🖐️ + 🧠. O estilo do cabeçalho DEVE (MUST) ser definido exclusivamente no `css/estilo.css`, garantindo padrão, estilo e formato idênticos em todas as páginas.

#### Scenario: Caminho visual entre as estações
- **WHEN** o usuário percorre a página
- **THEN** as estações aparecem conectadas por conectores, conduzindo visualmente da Estação 1 até a Estação 3

#### Scenario: Bloco do destino no hero
- **WHEN** o usuário abre a página
- **THEN** o hero exibe, logo após o badge, o bloco "DISCÍPULO" com a frase "Esteja com Jesus, Torne-se como Ele, Faça como Ele fez.", a fórmula "SER + FAZER + SABER" e os ícones ❤️ + 🖐️ + 🧠

#### Scenario: Separação entre cabeçalho e hero
- **WHEN** a home é aberta
- **THEN** o cabeçalho apresenta fundo visivelmente mais escuro que o início do gradiente do hero, sem quebrar a continuidade da paleta

#### Scenario: Cabeçalho idêntico nas três páginas
- **WHEN** o usuário navega entre `index.html`, `material-de-apoio.html` e `rci.html`
- **THEN** o cabeçalho mantém o mesmo padrão, estilo e formato, diferindo apenas no item ativo do menu
