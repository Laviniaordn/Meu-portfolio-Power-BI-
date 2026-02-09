# Portfólio de Dashboards Power BI - Alura

Este repositório apresenta uma coleção de dashboards desenvolvidos durante a formação em Power BI da Alura, demonstrando minhas habilidades em análise de dados, modelagem, cálculos DAX e visualização.

## 📊 Dashboards Incluídos

- [Dashboard 1: Petshop Gatito](#dashboard-1-petshop-gatito)
- [Dashboard 2: E-commerce no Brasil](#dashboard-2-e-commerce-no-brasil)
- [Dashboard 3: Opuline](#dashboard-3-opuline)

---

## Dashboard 1: Petshop Gatito

### 📋 Visão Geral
Este dashboard analisa o desempenho do faturamento de um pet shop, considerando diferentes categorias como gênero dos clientes, bairro e período (ano, trimestre e mês). O painel apresenta indicadores como faturamento total, ticket médio por cliente, quantidade de vendas e média de pets por cliente. Também conta com segmentações de dados por data de compra e por marcas, além de um visual do tipo Image Grid, que permite a interação ao clicar na imagem do produto ou realizar buscas diretamente no painel.

### 🖼️ Visualização
[📄 Clique aqui para visualizar o Dashboard](GatitoPetshop/Imagens/GatitoPetshop.png)

### 🏗️ Modelo de Dados
O modelo de dados utiliza um **Esquema Estrela** focado na eficiência das análises:
- **Tabelas**: `Clientes`, `Produtos` e `Vendas`.
- **Relacionamentos**: Tabelas de dimensão conectadas à tabela fato para permitir filtros dinâmicos por categoria e tempo.

![Modelo de Dados Gatito](GatitoPetshop/Imagens/ModeloDadosGatitoPetshop.png)

### 📏 Medidas DAX
Nesta seção, apresento as principais métricas criadas para este projeto:

- **Faturamento Total**:
```dax
Faturamento Total = SUM(Vendas[Valor Total])
```
![Print Medida Faturamento](dashboard1/imagens/foto_medida_faturamento.png)

### 🛠️ Tecnologias Utilizadas
- Power BI Desktop
- Power Query (M) para ETL
- DAX para cálculos de negócio
- Fonte de dados: Excel

---

## Dashboard 2: E-commerce no Brasil

### 📋 Visão Geral
Este dashboard monitora o desempenho de campanhas de marketing, acompanhando métricas como custo por clique (CPC), taxa de conversão e retorno sobre investimento (ROI). O objetivo é otimizar o orçamento de marketing e melhorar a eficácia das campanhas no cenário de e-commerce brasileiro.

### 🖼️ Visualização
[📄 Clique aqui para visualizar o Dashboard](EcommerceNoBrasil/Imagens/EcommerceNoBrasil.png)

### 🏗️ Modelo de Dados
Utiliza um **Esquema Estrela** para performance otimizada:
- **Tabela Fato**: `FatoMarketing` (Cliques, Impressões, Custo, Conversões).
- **Tabelas Dimensão**: `DimCampanha`, `DimCanal`, `DimData`.

![Modelo de Dados E-commerce](EcommerceNoBrasil/Imagens/ModeloDadosEcommerceNoBrasil.png)

### 📏 Medidas DAX
Principais métricas de desempenho de marketing:

- **Custo por Clique (CPC)**:
```dax
CPC = DIVIDE(SUM(FatoMarketing[Custo]), SUM(FatoMarketing[Cliques]), 0)
```
![Print Medida CPC](dashboard2/imagens/foto_medida_cpc.png)

### 🛠️ Tecnologias Utilizadas
- Power BI Desktop
- DAX
- Conector Google Analytics

---

## Dashboard 3: Opuline

### 📋 Visão Geral
Este dashboard oferece uma visão abrangente das finanças da empresa, incluindo receitas, despesas, lucro e fluxo de caixa. Ele permite a análise da saúde financeira e o planejamento orçamentário detalhado.

### 🖼️ Visualização
[📄 Clique aqui para visualizar o Dashboard- Página 1](Opuline/Imagens/Opuline1.png)
[📄 Clique aqui para visualizar o Dashboard- Página 2](Opuline/Imagens/Opuline2.png)

### 🏗️ Modelo de Dados
Estrutura robusta para análise financeira:
- **Tabela Fato**: `FatoFinanceiro` (Receita, Despesa, Lucro).
- **Tabelas Dimensão**: `DimContaContabil`, `DimCentroCusto`, `DimData`.

![Modelo de Dados Opuline](Opuline/Imagens/ModeloDadosOpuline.png)

### 📏 Medidas DAX
Cálculos financeiros fundamentais:

- **Margem de Lucro**:
```dax
Margem de Lucro = DIVIDE([Lucro], [Receita], 0)
```
![Print Medida Margem](dashboard3/imagens/foto_medida_lucro.png)

### 🛠️ Tecnologias Utilizadas
- Power BI Desktop
- DAX
- Fonte de dados: Arquivos Excel (.xlsx)

---

Desenvolvido por [Lavinia Oliveira](https://www.linkedin.com/in/lav%C3%ADnia-oliveira-117993204/)
