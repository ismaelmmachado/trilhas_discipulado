## ADDED Requirements

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
