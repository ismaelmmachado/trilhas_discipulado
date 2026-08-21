# Proposal: documentar-hub-e-normalizar-main

## Why
O repositório cresceu (páginas Material de Apoio e R.C.I., menu global) mas a
documentação OpenSpec cobre apenas a home (spec `journey-hub`). Além disso,
AGENTS.md e openspec/config.yaml citam o contexto v1.8.0, enquanto a realidade
é v1.9.0. A branch `main` está commits atrás de `homologacao`.

## What Changes
- ADDED requirement de menu global de navegação na spec `journey-hub`
- ADDED capabilities novas: `material-de-apoio` e `rci`
- ATUALIZAÇÃO de AGENTS.md, openspec/config.yaml e README.md para o estado atual
- Normalização da branch `main` via fast-forward até `homologacao`

## Impact
- Specs afetadas: `journey-hub` (delta), `material-de-apoio` (nova), `rci` (nova)
- Código: NENHUM (specs documentam o estado já publicado)
- Git: `main` avança para igualar `homologacao`; deploy continua na `homologacao`

## Non-goals
- Mudar a branch de deploy do GitHub Pages
- Criar bump de versão/tag nova (housekeeping mantém v1.9.0)
- Alterar conteúdo ou estilo das páginas existentes
