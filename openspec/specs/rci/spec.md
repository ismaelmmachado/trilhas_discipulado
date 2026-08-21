# rci Specification

## Purpose
Guiar o discípulo para viver a RCI (Rede de Relacionamentos Informais) — Listar, Orar com G.A.P.I.S., Escolher 3 e Convidar — como parte natural da Jornada do Discípulo.
## Requirements
### Requirement: Guia estruturado em 14 seções numeradas

A página DEVE (MUST) apresentar as 14 seções numeradas (h2 com âncora) cobrindo: definição da RCI, sua importância, o fluxo prático, como vivê-la no dia a dia, conexão com a jornada, acompanhamento, dificuldades comuns, celebração dos passos, cuidado com quem cuida (C.A.F.É.), a RCI no PG, acolhimento de quem vem, a RCI na jornada do discípulo e o convite final.

#### Scenario: Estrutura do guia
- **WHEN** o usuário acessa `rci.html`
- **THEN** as 14 seções numeradas estão presentes e navegáveis por âncora

### Requirement: Fluxo visual da RCI

O fluxo "1. Listar → 2. Orar com G.A.P.I.S. → 3. Escolher 3 → 4. Convidar" DEVE (MUST) ser exibido como passos conectados por setas (`rci-fluxo`).

#### Scenario: Visualização do fluxo
- **WHEN** o usuário percorre a seção do fluxo
- **THEN** os quatro passos aparecem ligados em sequência por setas

### Requirement: Tabelas de apoio responsivas

As tabelas (G.A.P.I.S., desafios e soluções, celebração dos passos, C.A.F.É., ações do PG, estações da jornada) DEVEM (MUST) permitir rolagem horizontal controlada (`rci-table-wrap`) sem quebrar o layout da página.

#### Scenario: Tabela em viewport estreito
- **WHEN** a página é aberta em viewport de 390px
- **THEN** nenhuma tabela causa rolagem horizontal da página

### Requirement: Hero próprio e navegação integrada

A página DEVE (MUST) ter título "RCI na Prática" com subtítulo voltado ao discípulo, breadcrumb "Início" apontando para `index.html`, skip-link, link "Voltar ao topo", meta/OG tags próprias e o menu global com o item "R.C.I." ativo (`class="active"` e `aria-current="page"`).

#### Scenario: Identidade da página
- **WHEN** o usuário acessa `rci.html`
- **THEN** o hero exibe "RCI na Prática" e o menu marca "R.C.I." como ativo

### Requirement: Responsividade e acessibilidade

A página DEVE (MUST) ser mobile-first com contraste AA (WCAG 2.1), estados de foco visíveis e respeito à preferência `prefers-reduced-motion`.

#### Scenario: Uso em celular
- **WHEN** a página é aberta em uma viewport de 390px
- **THEN** nenhum conteúdo causa rolagem horizontal

