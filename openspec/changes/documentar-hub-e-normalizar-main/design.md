# Design: documentar-hub-e-normalizar-main

## Decisões

### 1. Normalização da main = fast-forward simples
Decisão do usuário: `main` avança até igualar `homologacao`; a branch de
trabalho e de deploy do GitHub Pages continua sendo `homologacao`. O push é
feito com `git push origin homologacao:main` (recusa non-FF por padrão),
sem trocar de branch localmente.

### 2. Cobertura completa da documentação
- `journey-hub`: delta ADDED com o menu global de navegação (presente desde
  v1.7.0/v1.8.0 mas nunca especificado).
- `material-de-apoio`: capability nova documentando a página publicada.
- `rci`: capability nova documentando o guia em 14 seções publicado.
Requirements extraídos do estado real das páginas — nenhum HTML/CSS muda.

### 3. Uma change única
Escopo pequeno e coeso; uma change linear com todos os deltas + housekeeping,
arquivada ao final em um único ciclo propose → apply → archive.

### 4. Ordem de execução
Todo o trabalho acontece na `homologacao`. O fast-forward da `main` é o último
passo, depois do archive, para que `main` já nasça normalizada com tudo pronto.

### 5. Política de tag
Housekeeping/docs não geram bump: contexto permanece **v1.9.0**, sem mover a
tag já publicada (Regra de Ouro do projeto).

## Riscos
- Build do Pages não disparar no push → verificar `pages/builds/latest`;
  se necessário, disparar com commit vazio (padrão usado anteriormente).
- Cache da CDN (até 10 min) na verificação final → hard refresh quando aplicável.
