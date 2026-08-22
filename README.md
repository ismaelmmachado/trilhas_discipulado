# A Jornada do Discípulo · Comunidade Vitral

Hub das trilhas de discipulado da Comunidade Vitral (IPIB São José do Rio Preto).
Uma caminhada passo a passo que aproxima de Deus e dos outros — em três estações
rumo ao destino: **DISCÍPULO** (SER + FAZER + SABER).

Publicado em: <https://ismaelmmachado.github.io/trilhas_discipulado/>

## Estações

| Estação | Trilha | Papel | Pilar | Status |
|---|---|---|---|---|
| 1 | [Trilha de Novos](https://ismaelmmachado.github.io/trilha_de_novos/index.html) | FILHO | SER | Publicada |
| 2 | [Praticando o Caminho](https://ismaelmmachado.github.io/trilha_praticando_o_caminho/index.html) | SERVO | FAZER | Publicada |
| 3 | Fundamentos da Fé | MORDOMO | SABER | Em breve |

## Stack

- **HTML5 + CSS puro** — sem build step, zero dependências.
- Fontes: Playfair Display (títulos) e Inter (corpo), via Google Fonts.
- Design tokens por estação (`data-etapa`): 1=verde, 2=dourado, 3=azul marinho.
- Mobile-first, formato vertical 9:16, acessibilidade (AA, skip-link, reduced-motion).

## Rodar localmente

Abra `index.html` diretamente no navegador (site estático, sem servidor necessário).

## Publicar

O GitHub Pages serve a raiz da branch `homologacao`:

```bash
git push origin homologacao
```

Após o push, aguarde o build e confira:

```bash
gh api repos/ismaelmmachado/trilhas_discipulado/pages  # status: built
```

Se o build não disparar (`pages/builds/latest` mostrando commit antigo — pushes
feitos com token que não dispara workflows), faça o push via git local ou um
commit vazio para acionar o workflow de deploy.

## Estrutura

- `index.html` — header, hero, cards de estação, ápice "DISCÍPULO" e footer.
- `material-de-apoio.html` — materiais de apoio em 5 categorias.
- `rci.html` — guia da R.C.I. em 14 seções.
- `css/tokens.css`, `css/estilo.css` — tokens e estilos.
- `favicon.svg`, `og-image.svg` — identidade.
- `openspec/` — especificações (`journey-hub`, `material-de-apoio`, `rci`).

## Git

Branch de trabalho padrão: `homologacao`. Veja `AGENTS.md` (Regra de Ouro).
