# Poker Trainer

Simulador de treino de poker (NLHE 6-max, 100bb) em um único arquivo HTML, sem dependências. Basta abrir `poker-trainer.html` no navegador.

## Módulos

| Aba | O que treina |
|---|---|
| Pré-flop | Abertura, defesa de BB/SB, 3-bet e 4-bet, com estratégias mistas e matriz 13×13 |
| Pós-flop (equity) | Call/fold contra aposta, com equity Monte Carlo e pot odds |
| C-bet | Check, bet 33% ou bet 75% no flop em posição |
| Push/Fold | All-in ou fold de 5 a 20bb e call de all-in no BB |
| Torneio / ICM | Decisões de bolha/mesa final pelo ICM + calculadora ICM |
| Ranges / Editor | Ver e editar ranges (formato `22+, A2s+, KTo+, A5s-A2s, 87s:0.5`) |

## Aviso

Os ranges e a estratégia de c-bet são **aproximações**, não saída de um solver. Para treinar com números exatos, cole ranges exportados de PioSOLVER/GTO Wizard na aba **Ranges / Editor**.

## Como atualizar

Veja [CONTRIBUTING.md](CONTRIBUTING.md). Em resumo: os ranges ficam no array `SCEN` dentro do `<script>` do `poker-trainer.html`.
