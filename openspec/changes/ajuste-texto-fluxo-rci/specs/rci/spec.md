## MODIFIED Requirements

### Requirement: Fluxo visual da RCI

O fluxo "1. Listar → 2. Orar → 3. Escolher 3 → 4. Convidar" DEVE (MUST) ser exibido como passos conectados por setas (`rci-fluxo`), com rótulos curtos nos pills; a explicação detalhada do G.A.P.I.S. permanece no corpo da seção correspondente.

#### Scenario: Visualização do fluxo
- **WHEN** o usuário percorre a seção do fluxo
- **THEN** os quatro passos aparecem ligados em sequência por setas, com o segundo passo rotulado apenas como "2. Orar"

#### Scenario: Rótulo da Semana 2 no roteiro de 30 dias
- **WHEN** o usuário percorre o roteiro prático de 30 dias
- **THEN** o subtítulo da segunda semana é exibido como "Semana 2: Orar"
