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
url = "https://raw.githubusercontent.com/SeanTorres12/case_solfacil/refs/heads/main/data/vgsales.csv"
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

## Conclusão

- **Shooter** é o gênero que mais vendeu globalmente, com uma vantagem de mais de
  25 milhões de unidades sobre o segundo colocado — a maior diferença entre todos
  os itens do top 5, que entre si têm diferenças bem menores.

- O número de **lançamentos** caiu em 2019 e voltou a subir em 2020. Em um cenário
  real, esse padrão coincidiria com o período de lockdown, que provavelmente também
  teria elevado o volume de vendas.

- O **PC** é a plataforma dominante, com mais do que o dobro de jogos lançados em
  relação ao segundo colocado (PS4). Isso provavelmente reflete fatores do mundo
  real: jogos mais baratos, catálogo maior (incluindo "exclusivos" de outras
  plataformas) e o fato de o PC servir a múltiplos propósitos além de jogos —
  como trabalho e estudo.
