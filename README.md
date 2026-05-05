# ⚽ Análise de Dados — Futebol Europeu

> Projeto de Análise Exploratória de Dados (EDA) aplicado a um dataset de partidas de futebol europeu, com foco em identificar padrões de desempenho, vantagem do mandante, força ofensiva/defensiva dos times e perfil dos jogadores.

---

## 📌 Objetivo

Explorar os dados históricos de partidas de futebol europeu para responder perguntas como:

- Times mandantes têm vantagem real?
- Quais times marcam mais gols e sofrem menos?
- Como é o perfil físico e técnico dos jogadores?
- Quais habilidades mais influenciam a nota geral de um jogador?
- Como o desempenho dos times evoluiu ao longo das temporadas?

---

## 📁 Dataset

- **Fonte:** [Kaggle — European Soccer Database](https://www.kaggle.com/datasets/hugomathien/soccer)
- **Formato:** SQLite (`.sqlite`)
- **Tabelas analisadas:** `Match`, `Team`, `League`, `Country`, `Player`, `Player_Attributes`
- **Período coberto:** Temporadas de futebol europeu de 2008 a 2016
- **Volume:** +25.000 partidas de diversas ligas europeias

---

## 🔍 O que foi analisado

### Tabela Match
- Estrutura geral da tabela e seleção das colunas relevantes
- Distribuição de gols totais por partida
- Distribuição dos resultados — vitória do mandante, visitante e empate
- Comparação da média de gols entre mandante e visitante (boxplot)
- Análise temporal — média de gols por temporada de 2008 a 2016

### Tabela Team
- Gols marcados e sofridos como mandante
- Saldo de gols como mandante (gols feitos − gols sofridos)
- Criação de variáveis de vitória como mandante e como visitante
- Força ofensiva — média de gols marcados em casa e fora
- Força defensiva — média de gols sofridos em casa e fora
- Métrica completa de desempenho (ataque + defesa combinados)
- Top 10 melhores e piores times por saldo médio
- Times com mais jogos como mandante e como visitante

### Tabela League e Country
- Relação entre ligas e países
- Quantidade de jogos por liga e por país
- Média de gols por liga
- Comparação de gols mandante vs visitante por liga
- Média de gols por país

### Tabela Player
- Distribuição de idade, altura e peso dos jogadores
- Estatísticas gerais do perfil físico
- Identificação de outliers — jogadores muito altos, muito baixos e muito pesados
- Correlação entre atributos físicos

### Tabela Player_Attributes
- Distribuição da nota geral (`overall_rating`)
- Evolução da nota média dos jogadores ao longo do tempo
- Correlação entre habilidades (finalização, passe curto, drible) e nota geral
- Top 10 melhores jogadores por nota média
- Redução da tabela para uma linha por jogador (média dos atributos)
- Criação de função de qualidade do time baseada no rating dos jogadores
- Rating médio calculado por time

---

## 📊 Principais Insights

- **Times mandantes marcam em média mais gols** que os visitantes, confirmando a vantagem de jogar em casa
- **Vitórias do mandante são o resultado mais comum**, seguidas de vitórias do visitante e empates
- **A média de gols por partida se manteve estável** ao longo das temporadas analisadas, sem tendência clara de crescimento ou queda
- **Algumas ligas são consistentemente mais ofensivas** que outras — há diferença relevante na média de gols entre competições
- **Times de maior nível combinam bom ataque com boa defesa** — o saldo de gols reflete isso claramente
- **As habilidades técnicas mais correlacionadas com a nota geral** dos jogadores são finalização, passe curto e drible
- **O perfil físico dos jogadores** se concentra em uma faixa bem definida de altura e peso, com poucos outliers

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
├── eda.ipynb                  # Notebook com toda a análise exploratória
│
└── README.md                  # Documentação do projeto
```

---

## 🚀 Roadmap do projeto

- [x] EDA da tabela `Match` — distribuição de gols, resultados e vantagem do mandante
- [x] Análise temporal — média de gols por temporada (2008–2016)
- [x] EDA das tabelas `League` e `Country` — volume de jogos e média de gols por liga e país
- [x] EDA da tabela `Team` — força ofensiva, defensiva e saldo de gols como mandante
- [x] EDA da tabela `Player` — perfil físico dos jogadores (idade, altura, peso)
- [x] EDA da tabela `Player_Attributes` — nota geral, evolução e correlação de habilidades
- [x] Criação de rating médio por time baseado nos jogadores
- [ ] Feature Engineering — criação de variáveis para machine learning
- [ ] Análise de forma recente dos times (últimos N jogos)
- [ ] Desenvolvimento de modelo preditivo de resultados

---

## 👤 Autor

Projeto desenvolvido como parte de formação prática em Ciência de Dados.

**Welington Fonseca**
[![GitHub](https://img.shields.io/badge/GitHub-black?style=flat&logo=github)](https://github.com/kkwelington7-cpu)
