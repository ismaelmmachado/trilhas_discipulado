# journey-hub Specification

## Purpose
O hub apresenta a Jornada do Discípulo como uma caminhada de crescimento progressivo dividida em três estações, conecta visualmente o caminho até a cruz e direciona o usuário a cada trilha publicada — começando da base (Trilha de Novos) rumo ao destino (DISCÍPULO).
## Requirements
### Requirement: Apresentar as três estações da jornada

A página DEVE (MUST) exibir um cabeçalho com o título "A Jornada do Discípulo", um ícone de bússola (🧭) e o subtítulo "Uma caminhada passo a passo que te aproxima de Deus e dos outros — e você não caminha sozinho." Abaixo, a página DEVE (MUST) conter exatamente três cards de estação, cada um exibindo: ícone visual (🌱, 🌿, 🌳), badge de papel (FILHO, SERVO, MORDOMO) com descrição do papel, pergunta central, contagem de passos e pilar da estação (SER, FAZER, SABER). As cores de destaque de cada card DEVEM seguir a paleta de sua estação (verde, dourado e azul marinho).

#### Scenario: Visualização da Estação 1
- **WHEN** o usuário acessa o hub
- **THEN** o card da Estação 1 ("Trilha de Novos") é exibido com papel FILHO, descrição do papel "FILHO — alguém que sabe quem é em Deus", pergunta "Quem sou eu?", subtítulo "9 passos · Identidade e Pertencimento", pilar SER e destaque na cor verde

#### Scenario: Visualização da Estação 2
- **WHEN** o usuário acessa o hub
- **THEN** o card da Estação 2 ("Praticando o Caminho") é exibido com papel SERVO, descrição do papel "SERVO — alguém que pratica os caminhos de Jesus", pergunta "Como vivo?", subtítulo "17 passos · Práticas e Caráter", pilar FAZER e destaque na cor dourada

#### Scenario: Visualização da Estação 3
- **WHEN** o usuário acessa o hub
- **THEN** o card da Estação 3 ("Fundamentos da Fé") é exibido com papel MORDOMO, descrição do papel "MORDOMO — alguém que compreende e ensina a fé", pergunta "O que creio?", subtítulo "8 passos · Compreensão e Fundamentação", pilar SABER e destaque na cor azul marinho

### Requirement: Navegação para as trilhas publicadas

Os cards da Estação 1 e da Estação 2 DEVEM (MUST) funcionar como links que abrem as trilhas correspondentes em uma nova aba: Estação 1 → `https://ismaelmmachado.github.io/trilha_de_novos/index.html` e Estação 2 → `https://ismaelmmachado.github.io/trilha_praticando_o_caminho/index.html`. Os links DEVEM (MUST) incluir `rel="noopener"` e o alvo `_blank`.

#### Scenario: Abrir a Trilha de Novos
- **WHEN** o usuário ativa o card da Estação 1
- **THEN** uma nova aba é aberta em `https://ismaelmmachado.github.io/trilha_de_novos/index.html`

#### Scenario: Abrir Praticando o Caminho
- **WHEN** o usuário ativa o card da Estação 2
- **THEN** uma nova aba é aberta em `https://ismaelmmachado.github.io/trilha_praticando_o_caminho/index.html`

### Requirement: Estação 3 não clicável

Enquanto o site de Fundamentos da Fé não estiver publicado, o card da Estação 3 DEVE (MUST) permanecer visível com todo o seu conteúdo, DEVE (MUST) exibir a indicação "Em breve" e NÃO DEVE ser um link navegável nem ter aparência de link clicável.

#### Scenario: Card da Estação 3 sem navegação
- **WHEN** o usuário interage com o card da Estação 3
- **THEN** nenhuma navegação ocorre e o card mantém a indicação "Em breve"

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

### Requirement: Responsividade e acessibilidade

A página DEVE (MUST) ser mobile-first (formato vertical, 9:16) sem rolagem horizontal em viewports de celular e desktop. A página DEVE (MUST) incluir skip-link para o conteúdo principal, estados de foco visíveis nos elementos interativos e respeito à preferência `prefers-reduced-motion`. O contraste entre texto e fundo DEVE (MUST) atender ao nível AA (WCAG 2.1) em todas as seções.

#### Scenario: Navegação em dispositivos móveis
- **WHEN** o usuário abre o hub em uma viewport de 390px de largura
- **THEN** nenhum conteúdo causa rolagem horizontal e todos os cards cabem na largura da tela

#### Scenario: Contraste do bloco do destino
- **WHEN** o bloco "DISCÍPULO" é renderizado sobre a faixa de céu do hero
- **THEN** os textos do bloco mantêm contraste de pelo menos 4.5:1 em relação ao fundo

### Requirement: Menu global de navegação entre páginas

Todas as páginas do hub DEVEM (MUST) apresentar no header um menu de navegação principal (`<nav class="nav">`) com os links "As Trilhas", "Material de Apoio" e "R.C.I.". Na home, "As Trilhas" DEVE apontar para `#trilhas`; nas páginas internas, para `index.html#trilhas`. O item correspondente à página atual DEVE receber `class="active"` e o atributo `aria-current="page"`. O menu DEVE (MUST) permanecer visível e utilizável em viewports de até 520px: o header empilha em coluna (marca no topo) e os links se organizam em linha compacta com quebra quando necessário.

#### Scenario: Navegar da home para Material de Apoio
- **WHEN** o usuário acessa `index.html` e ativa "Material de Apoio"
- **THEN** a página `material-de-apoio.html` é aberta com esse item marcado como ativo

#### Scenario: Navegar para R.C.I.
- **WHEN** o usuário ativa "R.C.I." a partir de qualquer página
- **THEN** a página `rci.html` é aberta com esse item marcado como ativo

#### Scenario: Voltar às trilhas a partir de página interna
- **WHEN** o usuário está em `rci.html` ou `material-de-apoio.html` e ativa "As Trilhas"
- **THEN** a home é aberta posicionada na seção `#trilhas`

#### Scenario: Menu visível em telas pequenas
- **WHEN** o usuário abre qualquer página do hub em viewport de 390px de largura
- **THEN** os três links do menu estão visíveis abaixo da marca, sem rolagem horizontal e sem sobrepor o conteúdo

