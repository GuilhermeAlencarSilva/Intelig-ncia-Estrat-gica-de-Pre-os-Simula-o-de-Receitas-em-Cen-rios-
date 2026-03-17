Inteligência Estratégica de Preços — Simulação de Receitas em Cenários 

Sistema de análise estratégica de pricing que permite simular cenários de decisão e entender como mudanças em preço, promoção e volume de vendas impactam receita e margem.

O projeto foi desenvolvido como uma plataforma de inteligência analítica, com foco em tomada de decisão executiva.

🎯 Objetivo do Projeto

Empresas frequentemente precisam responder perguntas estratégicas como:

O que acontece com a receita se aumentarmos o preço em 5%?

Promoções realmente aumentam lucro ou apenas volume?

Qual é o ponto ótimo entre preço e demanda?

Este projeto cria um simulador interativo de pricing (What-If) que permite explorar esses cenários.

Principais objetivos:

Simular impactos de preço na receita

Avaliar eficiência de promoções

Identificar produtos que dominam receita

Apoiar decisões estratégicas de pricing

🧠 Problema de Negócio

Empresas que vendem muitos produtos enfrentam dificuldades para entender:

Sensibilidade de preço

Impacto real de descontos

Concentração de receita

Elasticidade de demanda

Sem ferramentas analíticas adequadas, decisões de pricing são frequentemente baseadas em intuição ou análise limitada.

Este projeto resolve esse problema criando um ambiente de simulação estratégica baseado em dados.

🏗 Arquitetura do Projeto

O projeto foi estruturado em um modelo analítico semelhante ao utilizado em empresas.

Camadas
Data Generation (Python)
        ↓
Dataset estruturado
        ↓
Modelo estrela (Power BI)
        ↓
Medidas DAX
        ↓
Dashboard analítico interativo
        ↓
Simulador de cenários What-If
🗂 Estrutura do Repositório
pricing-intelligence-simulator/

data/
   dataset_vendas.csv

notebooks/
   data_generation.ipynb

powerbi/
   pricing_simulator.pbix

images/
   dashboard_preview.png
   pricing_simulator.png

docs/
   project_explanation.md

README.md
📦 Dataset

O dataset foi gerado para simular dados realistas de vendas de uma empresa de varejo.

Período

2 anos de dados históricos.

Volume

~750 mil vendas

30+ produtos

múltiplos canais de venda

múltiplos níveis de promoção

📊 Estrutura do Modelo de Dados

Modelo estrela.

Fact Table

Fact_Vendas

Campos principais:

Data

ProdutoID

CanalID

Preco

Volume

Receita

Custo

Margem

TipoPromocao

Desconto

Dimensões

Dim_Produto

ProdutoID

Produto

Categoria

Marca

Dim_Canal

CanalID

Canal

Exemplo:

E-commerce

Marketplace

Loja Física

Dim_Data

Data

Ano

Mês

Trimestre

📈 Métricas Principais
Receita Total
Receita Total = SUM(Fact_Vendas[Receita])
Volume Total
Volume Total = SUM(Fact_Vendas[Volume])
Margem Total
Margem Total = SUM(Fact_Vendas[Margem])
Margem %
Margem % = DIVIDE([Margem Total],[Receita Total])
Ticket Médio
Ticket Medio = DIVIDE([Receita Total],[Volume Total])
📊 Dashboard Analítico

O dashboard foi estruturado em 6 páginas estratégicas.

📍 Página 1 — Executive Overview

Visão geral da performance da empresa.

<img width="874" height="800" alt="pag1" src="https://github.com/user-attachments/assets/fca92049-72da-4682-8916-5a2485f65273" />

Principais métricas:

Receita Total

Margem

Volume

Ticket Médio

Visualizações:

Receita ao longo do tempo

Receita por categoria

Receita por canal

Objetivo:

Oferecer visão executiva rápida da performance.

📍 Página 2 — Product Dominance

Analisa concentração de receita.

<img width="730" height="790" alt="pag2" src="https://github.com/user-attachments/assets/96e2db94-27a8-4362-8087-6c4b48b27258" />

Visualizações:

Curva de Pareto

Ranking de produtos

Análise ABC

Insight:

Identifica produtos que dominam a geração de receita.

📍 Página 3 — Promotion Impact

Avalia impacto das promoções.

<img width="977" height="786" alt="pag3" src="https://github.com/user-attachments/assets/253b634a-2f47-4364-af34-994c8fdb2827" />

Visualizações:

Receita por tipo de promoção

Volume por promoção

Margem por promoção

Scatter de desconto vs volume

Objetivo:

Entender se promoções geram crescimento saudável ou apenas volume artificial.

📍 Página 4 — Channel Strategy

Analisa performance por canal de venda.

<img width="728" height="793" alt="pag4" src="https://github.com/user-attachments/assets/5d33077b-a27d-46a4-935e-3b5e1ddedbe2" />

Visualizações:

Receita por canal

Margem por canal

Ticket médio por canal

Insight:

Identificar canais mais lucrativos.

📍 Página 5 — Pricing Simulation Lab

Principal diferencial do projeto.

Simulador de cenários estratégicos.

<img width="699" height="787" alt="pag5" src="https://github.com/user-attachments/assets/3f2565f0-2537-4133-a92c-724cdc7eb3b3" />

Controles:

Ajuste de preço

Ajuste de promoção

Ajuste de volume

Resultados simulados:

Receita projetada

Margem simulada

Volume esperado

🔬 Simulação What-If

A simulação utiliza parâmetros de cenário.

Exemplo:

Preço +5%
Promoção -10%
Volume +8%

A partir disso o modelo calcula:

Receita Simulada
Margem Simulada
Impacto na Receita
📊 Price vs Demand Sensitivity

Mapa de sensibilidade.

Eixos:

X → ajuste de preço
Y → mudança de demanda

Valores:

Receita projetada.

Objetivo:

Encontrar zona ótima de pricing.

⚠ Risk & Scenario Analysis

Análise de incerteza.

Inclui:

distribuição de cenários

receita esperada

melhor caso

pior caso

🛠 Tecnologias Utilizadas

Ferramentas principais:

Microsoft Power BI

Python

Google Colab

Figma

Bibliotecas:

pandas

numpy

matplotlib

🚀 Principais Insights do Projeto

Exemplos de insights encontrados:

20% dos produtos geram mais de 70% da receita

Promoções aumentam volume mas reduzem margem

Alguns canais possuem alto volume porém baixa rentabilidade

Pequenas mudanças de preço geram grande impacto na receita

📷 Preview

Sugestão para colocar imagens:

/images/dashboard_preview.png
/images/pricing_simulator.png
📚 Possíveis Evoluções do Projeto

Melhorias futuras:

modelagem de elasticidade real

machine learning para previsão de demanda

otimização automática de preço

simulação avançada com Monte Carlo

💡 Aprendizados

Este projeto demonstra habilidades em:

modelagem de dados

DAX avançado

análise estratégica

visualização executiva

simulação de cenários

📬 Contato

Autor: Seu Nome

LinkedIn
GitHub
Portfólio
