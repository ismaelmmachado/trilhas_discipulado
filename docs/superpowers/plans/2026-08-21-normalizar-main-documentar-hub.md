# Normalizar main + Documentar hub com OpenSpec — Plano de Implementação

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Sincronizar `main` com `homologacao` (fast-forward) e documentar todas as capabilities do hub em OpenSpec (menu global, Material de Apoio, RCI), corrigindo docs desatualizados.

**Architecture:** Change OpenSpec única `documentar-hub-e-normalizar-main` com 3 deltas de spec (documentam o estado atual — nenhum HTML/CSS muda), housekeeping de docs, arquivamento da change e FF da `main` como último passo.

**Tech Stack:** HTML/CSS estático, OpenSpec CLI 1.7.0, git/GitHub Pages.

## Global Constraints

- Idioma dos documentos: pt-BR
- Sem emojis além dos já usados no conteúdo (🧭🌱🌿🌳📚🎧🎵📝📱)
- Sem comentários no código
- Tag: housekeeping/docs = sem bump → mantém contexto v1.9.0, não mover tag publicada
- Regra de Ouro: commits/push em `homologacao`; `main` só recebe o FF explícito desta tarefa
- Propostas OpenSpec com menos de 500 palavras, sempre com seção "Non-goals"

---

### Task 1: Scaffold da change OpenSpec

- [x] Criar diretórios da change e `docs/superpowers/plans/`
- [x] Salvar este plano
- [x] Escrever `proposal.md`, `design.md`, `tasks.md`
- [x] Validar com `openspec validate --strict`
- [x] Commit

### Task 2: Delta da spec journey-hub — menu global

- [x] Escrever delta (ADDED Requirement: Menu global de navegação entre páginas + 3 scenarios)
- [x] Validar e commitar

### Task 3: Spec nova material-de-apoio

- [x] Escrever spec (5 categorias, itens "Em breve", navegação integrada, responsividade)
- [x] Validar e commitar

### Task 4: Spec nova rci

- [x] Escrever spec (14 seções, fluxo visual, tabelas responsivas, hero próprio, a11y)
- [x] Validar e commitar

### Task 5: Housekeeping de documentação

- [x] AGENTS.md: contexto v1.8.0 → v1.9.0; Estrutura com páginas novas e branch rci/vantiga
- [x] openspec/config.yaml: mesmo ajuste no bloco context
- [x] README.md: seção Estrutura atualizada
- [x] Conferir coerência (`grep v1.8.0`) e commitar

### Task 6: Arquivar change e publicar

- [x] Validar change completa
- [x] Push homologacao + aguardar build Pages
- [x] openspec archive + commit + push
- [x] Confirmar build final built

### Task 7: Fast-forward da main (último passo)

- [x] git push origin homologacao:main
- [x] SHAs de main/homologacao idênticos
- [x] Tags intactas (v1.9.0 em c79324f)

### Task 8: Verificação final no ar

- [x] 3 páginas 200, menu com 3 itens, sem "(Novo)"
- [x] /rci-novo.html → 404
- [x] 3 specs em openspec/specs/ + change arquivada
