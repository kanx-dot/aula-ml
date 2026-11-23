# Comparação de Modelos: `chamados-r1` vs. `chamados-r2`

## Alteração realizada (`dados-v1` → `dados-v2`)

Na ramificação `correcao-rotulo`, corrigiu-se o rótulo do chamado `006` (`bloqueio de acesso`) de `comum` para `urgente` em `data/chamados.csv` e atualizou-se `data/manifesto.json` para `chamados-v2`. A partição em `data/split.csv` foi mantida inalterada.

## Tabela de métricas )

| Métrica / Classe | `chamados-r1` (`chamados-v1`) | `chamados-r2` (`chamados-v2`) |
| :--- | :---: | :---: |
| **Acurácia geral** | `0.75` (3/4) | `1.0` (4/4) |
| **Recall — `comum` (suporte 2)** | `1.0` (2/2) | `1.0` (2/2) |
| **Recall — `urgente` (suporte 2)** | `0.5` (1/2) | `1.0` (2/2) |

## Verificação de integridade no clone limpo (`modelo-r1`)

- **Commit (`git rev-parse HEAD`):** `bf5df00b9003993f8c4bc90b1fe177815d3c8bc1`
- **`data/chamados.csv` (`dataset_sha256`):** `bc3fd86a3a5f598841a58839a9726d901fa7e8361ffe79c5b43873ad8a1328ac`
- **`data/split.csv` (`split_sha256`):** `2ef820171c1a4625fe216e6da67c7c8dcf9d97a08288c0239cd23f1a6961d981`
- **`models/model.json` (`artifact_sha256`):** `09d965544c9298c5586af0a1becbf07fb3f3c7b7c228a803ab91179f8b458a09`

## Decisão

**Aceitar `chamados-r2`.** O modelo `r2` elevou o recall da classe `urgente` de `0.5` para `1.0` e a acurácia de `0.75` para `1.0`, mantendo o recall da classe `comum` em `1.0` sobre a mesma partição de teste.
