# ⚽ Análise de Dados — Futebol Europeu

> Projeto de Análise Exploratória de Dados (EDA) aplicado a um dataset de partidas de futebol europeu, com foco em identificar padrões de desempenho, vantagem do mandante e eficiência ofensiva/defensiva dos times.

---

## 📌 Objetivo

Explorar os dados históricos de partidas de futebol europeu para responder perguntas como:

- Times mandantes têm vantagem real?
- Quais times marcam mais gols?
- Como o desempenho dos times evoluiu ao longo das temporadas?
- Existe relação entre ataque eficiente e boa defesa?

---

## 📁 Dataset

- **Fonte:** [Kaggle — European Soccer Database](https://www.kaggle.com/datasets/hugomathien/soccer)
- **Formato:** SQLite (`.sqlite`)
- **Tabelas disponíveis:** `Match`, `Team`, `Player`, `Team_Attributes`, entre outras
- **Período coberto:** Temporadas de futebol europeu de 2008 a 2016
- **Volume:** +25.000 partidas de diversas ligas europeias

---

## 🔍 O que foi analisado (EDA Tabela Match)

### 1. Estrutura e limpeza dos dados
- Seleção das colunas relevantes para análise
- Conversão da coluna de data para formato `datetime`
- Verificação de nulos e tipos de dados

### 2. Distribuição de gols por partida
- Histograma da distribuição de gols totais
- Média, mediana e dispersão dos gols por partida

### 3. Distribuição de resultados
- Proporção de vitórias do mandante, visitante e empates
- Visualização em gráfico de barras

### 4. Mandante vs. Visitante
- Comparação da média de gols marcados por cada lado
- Boxplot evidenciando a vantagem do mandante

### 5. Análise temporal
- Média de gols por temporada ao longo dos anos
- Tendência de crescimento ou queda no volume de gols

### 6. Desempenho dos times como mandante
- Top 10 times que mais marcaram gols em casa
- Top 10 times com melhor saldo de gols como mandante
- Ranking por saldo de gols (gols feitos − gols sofridos)

---

## 📊 Principais Insights

- **Times mandantes marcam em média mais gols** que os visitantes, confirmando a vantagem de jogar em casa
- **Vitórias do mandante são o resultado mais comum**, seguidas de vitórias do visitante e empates
- **Times de maior nível combinam bom ataque com boa defesa** — o saldo de gols reflete isso claramente
- **A média de gols por partida se manteve relativamente estável** ao longo das temporadas analisadas

---

## 🛠️ Tecnologias utilizadas

| Ferramenta | Uso |
|---|---|
| Python 3 | Linguagem principal |
| Pandas | Manipulação e análise de dados |
| NumPy | Operações numéricas |
| Matplotlib | Visualizações gráficas |
| Seaborn | Gráficos estatísticos |
| SQLite3 | Conexão e consulta ao banco de dados |
| Jupyter Notebook | Ambiente de desenvolvimento |

---

## 📂 Estrutura do projeto

```
soccer-analysis/
│
├── data/
│   └── database.sqlite        # Base de dados original (Kaggle)
│
├── eda.ipynb                  # Notebook com análise exploratória (Tabela Match)
│
└── README.md                  # Documentação do projeto
```

---

## 🚀 Próximos passos

- [ ] EDA das demais tabelas (`Team_Attributes`, `Player`, `Player_Attributes`)
- [ ] Feature Engineering — criação de variáveis para machine learning
- [ ] Análise de forma recente dos times (últimos N jogos)
- [ ] Desenvolvimento de modelo preditivo de resultados

---

## 👤 Autor

Projeto desenvolvido como parte de formação prática em Ciência de Dados.

**Welington Fonseca**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/welington-fonseca/)
[![GitHub](https://img.shields.io/badge/GitHub-black?style=flat&logo=github)](https://github.com/kkwelington7-cpu)
[![GitHub](https://img.shields.io/badge/GitHub-black?style=flat&logo=github)](https://github.com/kkwelington7-cpu)
