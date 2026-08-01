## Context

O programa "A Jornada do Discípulo" já possuía dois sites estáticos publicados no GitHub Pages — `trilha_de_novos` (Estação 1) e `trilha_praticando_o_caminho` (Estação 2) — sem nenhum ponto de entrada unificado. O hub precisa apresentar a jornada completa (Estações 1–3 + destino DISCÍPULO), integrar-se visualmente ao ecossistema existente e permitir deploy simples no GitHub Pages em `ismaelmmachado/trilhas_discipulado`.

Restrições de contexto:
- Os sites existentes são HTML/CSS puros, sem build step, com design tokens e fontes Google (Playfair Display + Inter).
- A Estação 3 (Fundamentos da Fé) ainda não foi publicada.
- A especificação visual do infográfico original define gradiente verde (base) → dourado (meio) → azul marinho (topo), em proporção vertical 9:16.

## Goals / Non-Goals

**Goals:**
- Hub estático leve, sem build step e sem dependências, pronto para GitHub Pages.
- Identidade visual coerente com o ecossistema (mesmos tokens, fontes e convenções de estilo).
- Caminhada visual de base→topo: estação 1 na base, ápice (cruz) no topo, com conectores entre as estações.
- Mobile-first (formato vertical 9:16) com acessibilidade (AA, skip-link, foco visível, reduced-motion).

**Non-Goals:**
- Construir ou hospedar o site da Estação 3 (Fundamentos da Fé).
- Alterar os sites existentes (`trilha_de_novos`, `trilha_praticando_o_caminho`).
- Introduzir framework (React, Astro etc.) ou build tooling.
- Sistema de autenticação, backend ou formulários.

## Decisions

**D1 — Site estático sem build (HTML + CSS puro).**
Os sites existentes seguem esse padrão e o GitHub Pages serve arquivos estáticos diretamente. Um framework adicionaria complexidade sem benefício para três cards + uma seção de destino. Alternativas consideradas: Astro (usado em um repositório de teste do usuário) e React — descartadas por serem desnecessárias.

**D2 — Padrão de tokens CSS com paleta por `data-etapa`.**
Reutiliza a convenção dos sites existentes (`tokens.css` com variáveis e paleta por atributo `data-etapa`). O hub define três paletas (verde, dourado, azul marinho), cada uma aplicada ao card da estação correspondente.

**D3 — Gradiente de fundo alinhado às seções (base→topo).**
O gradiente cobre o documento inteiro e suas paradas foram ajustadas às posições medidas das seções (hero/Estação 1 em verde, Estação 2 em dourado, Estação 3 em azul, ápice/footer em azul marinho). Contrastes validados ≥ 6.5:1 nas áreas de texto.

**D4 — Cores da especificação, não dos sites atuais.**
A especificação do infográfico atribui verde à Estação 1 e dourado à Estação 2 — o oposto das cores atuais dos sites publicados (Estação 1 amarela, Estação 2 verde). Decisão consciente do usuário de seguir a especificação.

**D5 — Links externos absolutos com `target="_blank"` e `rel="noopener"`.**
O hub não possui rota interna; cada estação publicada abre em nova aba apontando para o URL canônico do site existente. A Estação 3 é renderizada como card desabilitado ("Em breve"), sem link.

**D6 — SVG inline para a cena do ápice.**
O caminhante rumo à cruz iluminada é desenhado em SVG inline (sem assets externos), garantindo qualidade em qualquer densidade de tela e zero requisições adicionais.

## Risks / Trade-offs

- **Divergência de cores com os sites atuais (D4):** o usuário pode estranhar que a Estação 1 aparece verde no hub e amarela no site da trilha. Mitigação: decisão consciente do usuário; pode ser revisada quando a identidade das trilhas for unificada.
- **`og-image.svg` não é suportado por todas as plataformas sociais** (ex.: algumas só aceitam PNG/JPG). Trade-off aceito para manter o padrão dos sites existentes (que também usam SVG).
- **Estação 3 sem link:** o card "Em breve" fica sem navegação até a publicação do site de Fundamentos da Fé; o estado desabilitado pode causar expectativa. Mitigação: badge explícito "Em breve".
- **Gradiente dependente das proporções do layout:** se o conteúdo crescer muito, as paradas do gradiente precisarão ser re-ajustadas. Mitigação: paradas documentadas e validação via medição em viewport móvel e desktop.
