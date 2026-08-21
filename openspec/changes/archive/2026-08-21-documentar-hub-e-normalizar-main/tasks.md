# Tasks: documentar-hub-e-normalizar-main

## 1. Delta journey-hub
- [ ] Escrever specs/journey-hub/spec.md (ADDED menu global de navegação + scenarios)
- [ ] Validar com openspec validate --strict

## 2. Capability material-de-apoio
- [ ] Escrever specs/material-de-apoio/spec.md (categorias, itens "Em breve", navegação, a11y)

## 3. Capability rci
- [ ] Escrever specs/rci/spec.md (14 seções, fluxo, tabelas, hero, a11y)

## 4. Housekeeping
- [ ] AGENTS.md: contexto v1.9.0, estrutura com material-de-apoio.html/rci.html/rci/vantiga
- [ ] openspec/config.yaml: bloco context atualizado
- [ ] README.md: Estrutura atualizada

## 5. Publicação e normalização
- [ ] Validar change completa (--strict)
- [ ] Push homologacao + confirmar build Pages do commit novo
- [ ] openspec archive --yes + commit + push
- [ ] Fast-forward main (git push origin homologacao:main)
- [ ] Verificar SHAs idênticos e tags intactas
- [ ] Verificação final no ar (200s, menu sem "(Novo)", /rci-novo.html 404)
