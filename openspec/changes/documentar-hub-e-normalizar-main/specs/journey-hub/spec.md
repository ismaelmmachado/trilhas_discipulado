## ADDED Requirements

### Requirement: Menu global de navegação entre páginas

Todas as páginas do hub DEVEM (MUST) apresentar no header um menu de navegação principal (`<nav class="nav">`) com os links "As Trilhas", "Material de Apoio" e "R.C.I.". Na home, "As Trilhas" DEVE apontar para `#trilhas`; nas páginas internas, para `index.html#trilhas`. O item correspondente à página atual DEVE receber `class="active"` e o atributo `aria-current="page"`.

#### Scenario: Navegar da home para Material de Apoio
- **WHEN** o usuário acessa `index.html` e ativa "Material de Apoio"
- **THEN** a página `material-de-apoio.html` é aberta com esse item marcado como ativo

#### Scenario: Navegar para R.C.I.
- **WHEN** o usuário ativa "R.C.I." a partir de qualquer página
- **THEN** a página `rci.html` é aberta com esse item marcado como ativo

#### Scenario: Voltar às trilhas a partir de página interna
- **WHEN** o usuário está em `rci.html` ou `material-de-apoio.html` e ativa "As Trilhas"
- **THEN** a home é aberta posicionada na seção `#trilhas`
