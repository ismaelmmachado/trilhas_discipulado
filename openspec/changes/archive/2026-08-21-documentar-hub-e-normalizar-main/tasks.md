# Tasks: documentar-hub-e-normalizar-main

## 1. Delta journey-hub
- [x] Escrever specs/journey-hub/spec.md (ADDED menu global de navegação + scenarios)
- [x] Validar com openspec validate --strict

## 2. Capability material-de-apoio
- [x] Escrever specs/material-de-apoio/spec.md (categorias, itens "Em breve", navegação, a11y)

## 3. Capability rci
- [x] Escrever specs/rci/spec.md (14 seções, fluxo, tabelas, hero, a11y)

## 4. Housekeeping
- [x] AGENTS.md: contexto v1.9.0, estrutura com material-de-apoio.html/rci.html/rci/vantiga
- [x] openspec/config.yaml: bloco context atualizado
- [x] README.md: Estrutura atualizada

## 5. Publicação e normalização
- [x] Validar change completa (--strict)
- [x] Push homologacao + confirmar build Pages do commit novo
- [x] openspec archive --yes + commit + push
- [x] Fast-forward main (git push origin homologacao:main)
- [x] Verificar SHAs idênticos e tags intactas
- [x] Verificação final no ar (200s, menu sem "(Novo)", /rci-novo.html 404)
