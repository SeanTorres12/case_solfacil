# Case 1 — Análise Exploratória de Dados (Vendas de Games)

Análise exploratória com Pandas sobre um dataset fictício de vendas de videogames,
cobrindo limpeza de dados, estatísticas descritivas e visualizações.

## Como executar

Este projeto foi feito para rodar **100% no navegador, sem instalação local**, via
Google Colab.

1. Clique no botão abaixo (ou acesse o link) para abrir o notebook diretamente no Colab:

   [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/14dRK8frA81Zc2C_7y8KQLKftiXAo5oPb?usp=sharing)

2. No menu do Colab, vá em **Ambiente de execução > Executar tudo** (ou `Ctrl+F9`).

Não é necessário instalar nada nem baixar arquivos manualmente — o notebook já
carrega os dados e as bibliotecas automaticamente na primeira célula.

## Dependências

Todas as bibliotecas usadas (`pandas`, `matplotlib`) já vêm pré-instaladas no
ambiente padrão do Google Colab. Para quem preferir rodar localmente (Jupyter,
VS Code, etc.), as versões usadas estão fixadas em `requirements.txt`:

```bash
pip install -r requirements.txt
jupyter notebook Analise_Exploratoria_de_Dados_com_Pandas.ipynb
```

## Dados

O dataset (`vgsales.csv`, 72 linhas) está versionado neste repositório em
[`data/vgsales.csv`](data/vgsales.csv) e é carregado automaticamente pela primeira
célula do notebook a partir da URL raw do GitHub — não é preciso fazer upload manual:

```python
url = "https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/main/data/vgsales.csv"
df = pd.read_csv(url)
```

## Estrutura do repositório

```
.
├── Analise_Exploratoria_de_Dados_com_Pandas.ipynb   # notebook principal
├── data/
│   └── vgsales.csv                                  # dataset usado na análise
├── requirements.txt                                 # dependências fixadas
└── README.md
```

## O que a análise cobre

- Limpeza de valores faltantes na coluna `Ano`
- Gênero mais vendido globalmente e plataforma com mais jogos lançados
- Criação da coluna `Decada` (Anos 90 / Anos 2000 / Anos 2010)
- Gráfico de barras com o top 5 de gêneros por vendas
- Gráfico de linha com jogos lançados por ano
- Conclusão com os principais insights encontrados
