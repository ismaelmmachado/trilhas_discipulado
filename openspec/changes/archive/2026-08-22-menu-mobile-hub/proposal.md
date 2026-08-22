# Proposal: menu-mobile-hub

## Why
Em telas de até 520px a regra `.nav { display: none }` esconde o único menu do
site. A regra nasceu no commit inicial (v1.0.0), quando o hub tinha apenas a
home e o link era uma âncora interna. Com as páginas Material de Apoio (v1.7.0)
e R.C.I. (v1.8.0), o celular ficou sem navegação alguma entre as páginas.

## What Changes
- No breakpoint ≤520px, o header passa a empilhar em coluna: marca no topo e a
  `.nav` reexibida em linha compacta com os três links (As Trilhas, Material de
  Apoio, R.C.I.), com quebra de linha quando necessário
- Delta MODIFIED na spec `journey-hub`: cenário "Menu visível em telas pequenas"

## Impact
- Arquivo: `css/estilo.css` (uma regra de media query)
- Corrige as três páginas de uma vez (o menu é compartilhado)

## Non-goals
- Hamburger ou menu com JavaScript (são só 3 links; projeto é zero-dependência)
- Novo elemento HTML de menu mobile (reaproveita a `.nav` existente)
