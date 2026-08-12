# e-commerce-amazon-sales-PowerBI
Projeto pessoal prático desenvolvido para colocar em prática conhecimentos adquiridos a cerca do PowerBI e suas análises.
# 📊 Amazon Sales Performance Dashboard - Power BI

## 📌 Visão Geral do Projeto
Este projeto consiste em um dashboard interativo desenvolvido no Power BI para analisar o desempenho de vendas e métricas operacionais de e-commerce utilizando dados da Amazon.

![Visão Geral de Vendas](screenshots/visao_geral.png)

## 🎯 Objetivos de Negócio
- Monitorar o Faturamento Total e acompanhar o atingimento de metas.
- Analisar a evolução temporal das vendas diárias e mensais (MoM).
- Mapear a distribuição geográfica da receita por cidade/estado.
- Avaliar o desempenho por categoria de produto e canal de vendas.

## 🛠️ Tecnologias e Ferramentas Utilizadas
- **Power BI Desktop:** Construção do modelo, visuais e UX/UI.
- **Power Query (Linguagem M):** Limpeza, tratamento de tipos e transformação de dados.
- **DAX (Data Analysis Expressions):** Criação de inteligência temporal, tabelas calculadas (`dCalendario`) e KPIs de negócio.

## 📐 Estrutura do Modelo de Dados
- **Tabela Fato:** `Amazon Sale Report` (Vendas, Produtos, Status e Envio).
- **Tabela Dimensão:** `dCalendario` (Tabela de inteligência temporal criada em DAX).
- **Relacionamento:** 1:N entre `dCalendario[Date]` e `Amazon Sale Report[Date]`.

## 📈 Principais Medidas DAX Criadas
- **Faturamento Total:** `SUM('Amazon Sale Report'[Amount])`
- **Total de Pedidos:** `DISTINCTCOUNT('Amazon Sale Report'[Order ID])`
- **Ticket Médio:** `DIVIDE([Total Faturamento], [Total Pedidos])`

---
*Projeto desenvolvido para fins de estudos e portfólio pessoal.*
