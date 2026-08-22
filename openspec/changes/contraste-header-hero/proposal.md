# Proposal: contraste-header-hero

## Why
Na home, o cabeçalho (`#005F6B` sólido) e o topo do hero (início do gradiente
`#005F6B → #0A6A76`) têm exatamente a mesma cor: a separação só surge quando o
gradiente clareia, perto dos boxes creme. Como header e hero carregam conteúdos
distintos (marca vs. título da página), um degrau tonal sutil melhora a
hierarquia sem quebrar a metáfora da banda contínua do pôster.

## What Changes
- Cabeçalho passa a usar `--zona-petroleo-escuro` (#074B56); o hero mantém seu
  gradiente petróleo → petróleo-claro — degrau imediato na mesma família de cor
- Consolidação da regra `.nav a.active` no `css/estilo.css`, removendo as
  duplicatas idênticas de `css/rci.css` e `css/material-de-apoio.css` — o
  cabeçalho das três páginas passa a ter um único ponto de verdade
- Delta MODIFIED na spec `journey-hub` (Identidade visual da jornada)

## Impact
- Arquivos: `css/estilo.css`, `css/rci.css`, `css/material-de-apoio.css`
- Vale para as três páginas automaticamente (estilo centralizado)
- Contraste AA do texto branco sobre o fundo melhora

## Non-goals
- Linha divisória/borda no header (desnecessária com o novo tom)
- Alterar o gradiente do hero ou qualquer outra zona da paleta
