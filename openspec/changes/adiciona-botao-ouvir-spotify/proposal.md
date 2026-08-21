# Proposal: adiciona-botao-ouvir-spotify

## Why
Na página Material de Apoio, o box "Canal Spotify da Comunidade Vitral"
(seção Ferramentas para o Caminho) oferece apenas o botão "Baixar". A mesma
ferramenta na Trilha de Novos (Estação 1) oferece também o botão "Ouvir" com
link direto para o canal no Spotify. O hub deve oferecer a experiência
completa, sem exigir que o visitante passe pela página da trilha.

## What Changes
- ADDED botão "Ouvir" no box do Spotify de `material-de-apoio.html`,
  apontando para `https://open.spotify.com/show/1prjsrcxPho9otrP1VUWT4`
- ADDED estilo `.apoio-acoes` e `.apoio-link.is-secondary` em
  `css/material-de-apoio.css`, espelhando o padrão visual da Trilha de Novos
  (Ouvir primário, Baixar secundário)
- ADDED requirement "Ações do item Canal Spotify" na spec `material-de-apoio`

## Impact
- Arquivos: `material-de-apoio.html`, `css/material-de-apoio.css`, spec delta
- Nenhum outro box ou página é alterado

## Non-goals
- Alterar os boxes de Bible App, Lectio 365 e demais categorias
- Mudar o link existente de "Baixar" (`https://www.spotify.com/download/`)
- Criar player embutido do Spotify
