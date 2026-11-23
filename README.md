# Versionamento de dados e modelos (`aula-ml`)

Projeto prático de versionamento de dataset, partição, código, parâmetros e modelos de classificação de chamados (`comum` vs. `urgente`) com **Git** e **DVC**.

## Pré-requisitos

- **Git** instalado e configurado (`user.name` e `user.email`).
- **Python 3.10+** (utiliza apenas a biblioteca padrão).
- **DVC 3** (`dvc>=3,<4`).
- Ambiente **Bash / Zsh** (no Windows, via **WSL**).

## Configuração do Armazenamento DVC

Os descritores (`.dvc`) e manifestos ficam no Git/GitHub, enquanto os arquivos de dados e artefatos de modelo ficam no armazenamento remoto DVC (nesta prática, o diretório irmão `../dvc-storage`):

```bash
dvc remote add -d storage ../dvc-storage
dvc remote list
```
URL_GITHUB=$(git remote get-url origin)
cd ..
git clone "$URL_GITHUB" aula-ml-restauracao
cd aula-ml-restauracao
git switch --detach modelo-r1
dvc pull

### Atividade feita por Kauã Cavalcante (570304) - Engenharia de Sistemas Inteligentes para ATP07
