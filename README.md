# Portfólio de Dashboards Power BI - Alura

Este repositório apresenta uma coleção de dashboards desenvolvidos durante a formação em Power BI da Alura, demonstrando minhas habilidades em análise de dados, modelagem e visualização.

## 📊 Dashboards

Cada dashboard está em sua própria pasta, contendo:
- Imagens do dashboard.
- Uma breve descrição.
- Explicação do modelo de dados e medidas.

### Dashboards Incluídos:

- [Dashboard 1: Petshop Gatito](#dashboard-1-vendas)
- [Dashboard 2: E-commerce no Braisl](#EcommerceNoBrasil/Imagens/EcommerceNoBrasil.pdf)
- [Dashboard 3: Opuline](#dashboard-3-financeiro)

---

## Dashboard 1: Petshop Gatito

![Dashboard de Vendas](dashboard1/images/dashboard_vendas.png)

### 📋 Visão Geral
Este dashboard analisa o desempenho do faturamento de um pet shop, considerando diferentes categorias como gênero dos clientes, bairro e período (ano, trimestre e mês). O painel apresenta indicadores como faturamento total, ticket médio por cliente, quantidade de vendas e média de pets por cliente. Também conta com segmentações de dados por data de compra e por marcas, além de um visual do tipo Image Grid, que permite a interação ao clicar na imagem do produto ou realizar buscas diretamente no painel.

### 🏗️ Modelo de Dados
O modelo de dados para o Dashboard de Vendas utiliza um **Esquema Estrela** com as seguintes tabelas:
- **Tabela Fato**: `Clientes` , `Produtos` e `Vendas` (contém métrica como `Valor médio por produto vendido`).

![Modelo de Dados Vendas](data_models/modelo_dados_vendas.png)

### 🛠️ Tecnologias Utilizadas
- Power BI Desktop
- Power Query (M) para transformação de dados
- DAX para criação de medida
- Fonte de dados: Excel

---

## Dashboard 2: E-commerce no Braisl

![Dashboard de Marketing](dashboard2/images/dashboard_marketing.png)

### 📋 Visão Geral
Este dashboard monitora o desempenho de campanhas de marketing, acompanhando métricas como custo por clique (CPC), taxa de conversão e retorno sobre investimento (ROI). O objetivo é otimizar o orçamento de marketing e melhorar a eficácia das campanhas.

### 🏗️ Modelo de Dados
O modelo de dados para o Dashboard de Marketing também segue um **Esquema Estrela**:
- **Tabela Fato**: `FatoMarketing` (contém métricas como `Cliques`, `Impressões`, `Custo`, `Conversões`).
- **Tabelas Dimensão**: `DimCampanha`, `DimCanal`, `DimData`.

![Modelo de Dados Marketing](data_models/modelo_dados_marketing.png)

### 🛠️ Tecnologias Utilizadas
- Power BI Desktop
- Power Query (M)
- DAX
- Fonte de dados: Google Analytics (via conector Power BI)

---

## Dashboard 3: Opuline

![Dashboard Financeiro](dashboard3/images/dashboard_financeiro.png)

### 📋 Visão Geral
Este dashboard oferece uma visão abrangente das finanças da empresa, incluindo receitas, despesas, lucro e fluxo de caixa. Ele permite a análise da saúde financeira e o planejamento orçamentário.

### 🏗️ Modelo de Dados
O Dashboard Financeiro utiliza um **Esquema Estrela** com as seguintes tabelas:
- **Tabela Fato**: `FatoFinanceiro` (contém métricas como `Receita`, `Despesa`, `Lucro`).
- **Tabelas Dimensão**: `DimContaContabil`, `DimCentroCusto`, `DimData`.

![Modelo de Dados Financeiro](data_models/modelo_dados_financeiro.png)

### 🛠️ Tecnologias Utilizadas
- Power BI Desktop
- Power Query (M)
- DAX
- Fonte de dados: Arquivos Excel (.xlsx)

---

Desenvolvido por [Lavinia Oliveira](https://www.linkedin.com/in/lav%C3%ADnia-oliveira-117993204/)
