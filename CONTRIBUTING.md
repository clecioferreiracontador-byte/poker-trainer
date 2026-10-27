# Como contribuir

1. Crie uma branch: `git checkout -b minha-alteracao`
2. Edite `poker-trainer.html` e teste abrindo no navegador (ou `python -m http.server` na pasta).
3. Faça commit e abra um Pull Request descrevendo a mudança.

## Onde mexer

- **Ranges pré-flop:** array `SCEN` (campo `r` com `raise` e `call`). Formato: `22+`, `A2s+`, `KTo+`, `A5s-A2s`, `87s:0.5` (`:0.5` = 50% de frequência). Fold é o restante.
- **Push/Fold:** tabelas `PUSH` e `CALLV` (% de mãos por stack 5/8/10/12/15/20bb) e `RANKSTR` (ordem de força das mãos).
- **ICM:** presets em `ICMP`; cálculo em `icmEq`, `icmCtx`, `icmEval`.
- **C-bet:** modelo heurístico em `cbStrat`.

## Regras

- Mantenha tudo em um único arquivo, sem dependências externas.
- Ao mudar ranges, diga a fonte (solver, livro, chart) no Pull Request.
