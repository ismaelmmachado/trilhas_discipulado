# AGENTS.md — Trilhas (Hub "A Jornada do Discípulo")

Guia de convenções e contexto para agentes que trabalham neste repositório.

## Regra de Ouro (git — nunca esquecer)

1. **"Salva"** → commit, push e tag em `homologacao` (branch de trabalho padrão).
2. **"Salva em main"** (explícito) → `main`.
3. **Tag:** usar sempre a tag do **contexto em que estamos trabalhando**.
4. **Tag específica informada** pelo usuário tem precedência sobre qualquer padrão.
5. `main` só é usado quando solicitado explicitamente.

### Contexto atual e tags
- Contexto: **hub journey-hub** → tag **`v1.9.0`** (anotada, páginas Material de Apoio e R.C.I. publicadas; R.C.I. unificada em `rci.html`).
- Tags anteriores (v1.0.0–v1.8.0) permanecem publicadas apontando para seus commits.
- Mudanças que não geram bump (housekeeping/docs) **mantêm a tag do contexto**, sem mover tag já publicada.

## Projeto

Hub estático das trilhas de discipulado da Comunidade Vitral (IPIB São José do Rio Preto).
Publicado via GitHub Pages em: `https://ismaelmmachado.github.io/trilhas_discipulado/`

### Stack
- **HTML5 + CSS puro** — sem build step, zero dependências.
- Fontes: Playfair Display (títulos) e Inter (corpo), via Google Fonts.
- Design tokens: `css/tokens.css` com paleta por estação via atributo `data-etapa`
  (1=verde, 2=dourado, 3=azul marinho).
- Estilo: `css/estilo.css` (mobile-first, formato vertical 9:16).

### Estrutura
- `index.html` — header (🧭), hero, 3 cards de estação conectados, ápice "DISCÍPULO"
  (SVG inline do caminhante rumo à cruz) e footer.
- `material-de-apoio.html` — materiais de apoio em 5 categorias.
- `rci.html` — guia da R.C.I. em 14 seções (versão antiga preservada na branch `rci/vantiga`).
- `css/tokens.css`, `css/estilo.css` — estilo.
- `favicon.svg`, `og-image.svg` — identidade.
- `openspec/` — documentação spec-driven (specs `journey-hub`, `material-de-apoio`, `rci`).
- `AGENTS.md`, `README.md` — documentação do projeto.

### Trilhas existentes (repos separados, já publicados)
- Estação 1: `https://ismaelmmachado.github.io/trilha_de_novos/index.html`
- Estação 2: `https://ismaelmmachado.github.io/trilha_praticando_o_caminho/index.html`
- Estação 3 (Fundamentos da Fé): ainda não publicada — card "Em breve" no hub.

## Deploy (GitHub Pages)

- GitHub Pages serve a partir da raiz (`/`) da branch **`homologacao`**.
- Sem build step: basta `git push origin homologacao` para publicar o conteúdo commitado.
- Verificação: `gh api repos/ismaelmmachado/trilhas_discipulado/pages` → `status: built`.
- Observação: habilitar Pages pela 1ª vez exige permissão `pages` de escrita no token
  ou configuração manual em *Settings → Pages → Deploy from a branch → homologacao / (root)*.

## Convenções

- Idioma dos documentos: português (pt-BR).
- Sem emojis em código/comentários além dos já usados no conteúdo (🧭🌱🌿🌳).
- Sem comentários no código, salvo se solicitado.
