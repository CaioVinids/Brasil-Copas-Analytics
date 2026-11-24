# 📊 Dashboard Seleção Brasileira em Copas do Mundo — Power BI

## Descrição do Projeto
Dashboard interativo desenvolvido em Power BI para analisar o desempenho da Seleção Brasileira nas quatro últimas Copas do Mundo (2014, 2018, 2022 e 2026), cobrindo resultados, aproveitamento, gols, estatísticas de jogo e saldo de gols por adversário ao longo dos 22 jogos disputados no período.

O relatório é dividido em duas páginas: Visão Geral, com os resultados e a campanha de cada edição, e Raio-X Tático, com a eficiência ofensiva, a solidez defensiva, a posse de bola e a disciplina.

## 🎯 Objetivos da Análise
- Consolidar o desempenho da Seleção nas últimas quatro Copas em um único painel visual.
- Permitir a análise dos resultados sob diferentes recortes: edição, técnico, fase do torneio e adversário.
- Identificar padrões de desempenho, como aproveitamento, saldo de gols, eficiência na finalização e solidez defensiva.

## ❓ Perguntas de Negócio Respondidas
- Qual foi o aproveitamento do Brasil nas últimas quatro Copas?
- Como foi a campanha em cada edição (sede, técnico, fase alcançada e saldo de gols)?
- Em quais fases do torneio o rendimento da Seleção cai?
- O que diferencia as vitórias das derrotas: a posse de bola ou a eficiência na finalização?
- Contra quais adversários o Brasil teve o melhor e o pior saldo de gols?
- Como evoluiu a solidez defensiva de uma Copa para a outra?

## 🔍 Principais Insights
- Em 22 jogos, o Brasil somou 12 vitórias, 5 empates e 5 derrotas, com aproveitamento de 62,1%, 37 gols marcados, 24 sofridos e saldo de +13.
- A posse de bola varia pouco entre vitórias (57,6%) e derrotas (53,8%), mas a conversão de finalizações em gol vai de 16,6% nas vitórias para 4,1% nas derrotas: o que separou ganhar de perder foi a eficiência, não ter a bola.
- A defesa melhorou de forma clara: a média de gols sofridos por jogo foi de 2,0 em 2014 (ano da derrota por 7 a 1 para a Alemanha) para 0,6 em 2018 e 2022 e 0,8 em 2026.
- As edições de 2018, 2022 e 2026 tiveram o mesmo aproveitamento (66,7%), mas terminaram em fases diferentes: quartas de final (6º lugar), quartas de final (7º lugar) e oitavas de final (11º lugar).
- O melhor saldo de gols por adversário foi contra a Sérvia (+4), e o pior contra a Alemanha (-6).

## 🛠️ Ferramentas Utilizadas
- **Power BI Desktop** — modelagem de dados, DAX e construção do dashboard
- **Power Query** — combinação dos arquivos CSV, extração da edição a partir do nome do arquivo, filtro dos jogos do Brasil e criação de colunas condicionais (adversário, gols, posse, resultado, fase)
- **DAX** — criação das medidas de desempenho e estatísticas

## 🧱 Modelo de Dados:

Modelagem em esquema estrela:

- **Fato_Jogos_Brasil** — uma linha por jogo, com data, adversário, resultado, fase, gols, posse, finalizações, escanteios, faltas e cartões
- **Dim_Edicao** — uma linha por Copa, com ano, sede, técnico, campanha final e colocação (criada com DATATABLE)
- **Medidas** — tabela dedicada às medidas DAX, organizadas em pastas

## 📈 Principais Indicadores
- Jogos, Vitórias, Empates, Derrotas e Aproveitamento (%)
- Gols Marcados, Gols Sofridos e Saldo de Gols
- Finalizações, Finalizações no Alvo, % Pontaria e % Conversão
- Posse Média, Escanteios por jogo e Jogos sem sofrer gols

## 📊 Análises Desenvolvidas
Visão Geral:
- Cartões com os principais indicadores da campanha
- Resultados por edição (vitórias, empates e derrotas)
- Aproveitamento por fase do torneio
- Resumo executivo por edição: sede, técnico, campanha final, jogos, aproveitamento e saldo de gols

Raio-X Tático:
- Cartões de finalizações, pontaria, conversão, posse, escanteios e jogos sem sofrer gols
- Desempenho por resultado: posse, pontaria e conversão nas vitórias, empates e derrotas
- Saldo de gols por adversário (com formatação condicional)
- Resumo tático por edição: posse, escanteios, faltas, cartões amarelos e médias de gols

## 📁 Estrutura do Projeto
- `data/` → Bases de dados em Excel
- `powerbi/` → Arquivo do dashboard em Power BI (.pbix)
- `README.md`

## 📚 Fonte dos Dados
Os dados utilizados neste projeto foram obtidos nos datasets de Copa do Mundo disponibilizados pelo [FootyStats](https://footystats.org/international/world-cup/datasets), em formato CSV.

A partir dessas bases, os jogos da Seleção Brasileira foram selecionados, tratados e transformados no Power Query para utilização no dashboard.

## 📌 Contexto
Este projeto foi desenvolvido como parte dos meus estudos e prática em Business Intelligence, aplicando modelagem de dados (esquema estrela), Power Query e DAX sobre dados de partidas da Seleção Brasileira em Copas do Mundo, com foco na análise de desempenho em campo.

## Print do dash
<img width="1724" height="969" alt="foto1" src="https://github.com/user-attachments/assets/ee27b1a7-2b87-4e8a-802d-44450cd5b82e" />
<img width="1728" height="967" alt="foto2" src="https://github.com/user-attachments/assets/f4a9a1b9-65d5-43ab-96a4-f136237ccbae" />
