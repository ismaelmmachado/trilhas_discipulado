# Proposal: ajuste-texto-fluxo-rci

## Why
O pill do fluxo visual da página R.C.I. usa o rótulo longo "2. Orar com
G.A.P.I.S.", enquanto o título da própria seção já resume o fluxo como
"Listar → Orar → Escolher 3 → Convidar". O rótulo curto deixa o fluxo mais
legível e consistente, especialmente no mobile, onde os quatro pills competem
por espaço. O mesmo vale para o subtítulo da Semana 2 do roteiro de 30 dias.

## What Changes
- Pill do fluxo (`rci.html`): "2. Orar com G.A.P.I.S." → "2. Orar"
- Subtítulo da Semana 2 (`rci.html`): "Semana 2: Orar com G.A.P.I.S." → "Semana 2: Orar"
- Delta MODIFIED na spec `rci`: texto do fluxo atualizado

## Impact
- Arquivo: `rci.html` (dois rótulos)
- As explicações sobre G.A.P.I.S. no corpo da página permanecem intactas

## Non-goals
- Remover as menções explicativas ao G.A.P.I.S. no texto corrido e tabelas
- Alterar os demais passos do fluxo (1. Listar, 3. Escolher 3, 4. Convidar)
