## MODIFIED Requirements

### Requirement: Menu global de navegação entre páginas

Todas as páginas do hub DEVEM (MUST) apresentar no header um menu de navegação principal (`<nav class="nav">`) com os links "As Trilhas", "Material de Apoio" e "R.C.I.". Na home, "As Trilhas" DEVE apontar para `#trilhas`; nas páginas internas, para `index.html#trilhas`. O item correspondente à página atual DEVE receber `class="active"` e o atributo `aria-current="page"`. O menu DEVE (MUST) permanecer visível e utilizável em viewports de até 520px: o header empilha em coluna (marca no topo) e os links se organizam em linha compacta com quebra quando necessário.

#### Scenario: Navegar da home para Material de Apoio
- **WHEN** o usuário acessa `index.html` e ativa "Material de Apoio"
- **THEN** a página `material-de-apoio.html` é aberta com esse item marcado como ativo

#### Scenario: Navegar para R.C.I.
- **WHEN** o usuário ativa "R.C.I." a partir de qualquer página
- **THEN** a página `rci.html` é aberta com esse item marcado como ativo

#### Scenario: Voltar às trilhas a partir de página interna
- **WHEN** o usuário está em `rci.html` ou `material-de-apoio.html` e ativa "As Trilhas"
- **THEN** a home é aberta posicionada na seção `#trilhas`

#### Scenario: Menu visível em telas pequenas
- **WHEN** o usuário abre qualquer página do hub em viewport de 390px de largura
- **THEN** os três links do menu estão visíveis abaixo da marca, sem rolagem horizontal e sem sobrepor o conteúdo
