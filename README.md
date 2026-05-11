# Previsão de Resultados de Partidas de Futebol

Este projeto tem como objetivo prever o resultado de partidas de futebol com base em dados históricos. O trabalho está sendo desenvolvido em etapas, partindo da exploração dos dados até a construção e avaliação de modelos de machine learning.

---

## Sobre o projeto

Os dados vêm de uma base SQLite com informações de ligas europeias de futebol, cobrindo múltiplas temporadas. A análise foca no desempenho ofensivo e defensivo dos times, na distribuição de resultados e nos padrões de gols ao longo do tempo.

A ideia central é: dado o histórico de dois times, é possível prever se o mandante vai vencer, se haverá empate ou se o visitante vai ganhar?

---

## Etapas do projeto

**Análise exploratória (concluída)**

A EDA foi feita sobre a tabela de partidas, cruzando com a tabela de times para dar nome aos IDs. As principais análises foram:

  Distribuição de gols por partida e por temporada
  Comparação entre desempenho de mandante e visitante
  Força ofensiva e defensiva por time, calculada como média de gols marcados e sofridos em casa e fora
  Saldo médio de gols como métrica de desempenho geral
  Ranking dos melhores e piores times com base nesse saldo

Um padrão já se confirma nos dados: times mandantes têm vantagem estatística clara, e os times de ponta sustentam saldo positivo tanto em casa quanto fora.

**Feature engineering (próxima etapa)**

A partir das métricas já calculadas na EDA, o plano é construir variáveis que representem o contexto de cada time antes de cada partida:

  Média móvel de gols marcados e sofridos nas últimas N partidas
  Taxa de vitória recente como mandante e visitante
  Saldo de gols acumulado por temporada
  Diferença de força entre os dois times em confronto

O objetivo é que cada linha do dataset de treino represente um contexto comparativo entre mandante e visitante, não apenas os dados brutos de uma partida.

**Modelagem (planejada)**

Com as features prontas, serão testados modelos de classificação para prever o resultado (vitória mandante, empate, vitória visitante). A avaliação vai levar em conta não só a acurácia mas também como o modelo lida com empates, que costumam ser a classe mais difícil de acertar.

---

## Tecnologias utilizadas

  Python 3
  Pandas e NumPy para manipulação de dados
  Matplotlib e Seaborn para visualizações
  SQLite como fonte de dados
  Scikit-learn (na etapa de modelagem)

---

## Estrutura do repositório


data/
 database.sqlite
 assets/
 (gráficos gerados durante a EDA)
 eda.ipynb
 README.md


---

## Status

O projeto está em andamento. A análise exploratória e analise de hipóteses foram concluídas e a próxima etapa é a construção das features para alimentar o modelo.

