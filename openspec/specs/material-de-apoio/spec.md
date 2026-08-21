# material-de-apoio Specification

## Purpose
Centralizar os materiais de apoio à jornada (livros, podcasts, músicas, guias e ferramentas) numa página do hub, organizada por categoria, com identidade visual consistente e navegação integrada ao menu global.
## Requirements
### Requirement: Cinco categorias de materiais

A página DEVE (MUST) exibir as categorias "📚 Livros Recomendados", "🎧 Podcasts", "🎵 Músicas", "📝 Guias e Recursos" e "📱 Ferramentas para o Caminho", cada uma com sua lista de itens contendo título e descrição curta.

#### Scenario: Visualização das categorias
- **WHEN** o usuário acessa `material-de-apoio.html`
- **THEN** as cinco categorias são listadas com seus itens visíveis

### Requirement: Itens sem recurso publicado

Itens cujo material ainda não tem link publicado DEVEM (MUST) exibir o selo "Em breve" (`apoio-em-breve`) e NÃO DEVEM ser navegáveis.

#### Scenario: Item em breve
- **WHEN** o usuário vê um item sem link publicado
- **THEN** o item mostra o selo "Em breve" e nenhuma navegação ocorre

### Requirement: Navegação integrada ao hub

A página DEVE (MUST) manter o header do hub com o menu global (item "Material de Apoio" ativo com `class="active"` e `aria-current="page"`), breadcrumb "Início" apontando para `index.html`, skip-link e link "Voltar ao topo".

#### Scenario: Breadcrumb de volta à home
- **WHEN** o usuário ativa "Início" no breadcrumb
- **THEN** retorna à home do hub

### Requirement: Responsividade e acessibilidade

A página DEVE (MUST) ser mobile-first com contraste AA (WCAG 2.1), estados de foco visíveis e respeito à preferência `prefers-reduced-motion`.

#### Scenario: Uso em celular
- **WHEN** a página é aberta em uma viewport de 390px
- **THEN** nenhum conteúdo causa rolagem horizontal

### Requirement: Ações do item Canal Spotify

O item "Canal Spotify da Comunidade Vitral" (seção Ferramentas para o Caminho) DEVE (MUST) oferecer dois botões: "Ouvir", apontando para `https://open.spotify.com/show/1prjsrcxPho9otrP1VUWT4` com `target="_blank"` e `rel="noopener noreferrer"`, e "Baixar", mantendo o link `https://www.spotify.com/download/`. Os botões DEVEM (MUST) ficar agrupados em um contêiner `.apoio-acoes`, com "Ouvir" no estilo primário e "Baixar" no estilo secundário (`is-secondary`), espelhando o padrão da Trilha de Novos.

#### Scenario: Ouvir o canal no Spotify
- **WHEN** o usuário ativa o botão "Ouvir"
- **THEN** uma nova aba abre `https://open.spotify.com/show/1prjsrcxPho9otrP1VUWT4`

#### Scenario: Baixar o aplicativo Spotify
- **WHEN** o usuário ativa o botão "Baixar"
- **THEN** uma nova aba abre `https://www.spotify.com/download/`

#### Scenario: Botões em viewport estreito
- **WHEN** a página é aberta em viewport de até 480px
- **THEN** os dois botões permanecem visíveis, centralizados e sem quebrar o layout do box

