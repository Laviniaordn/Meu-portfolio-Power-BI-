# Portfólio de Dashboards Power BI - Alura

Este repositório apresenta uma coleção de dashboards desenvolvidos durante a formação em Power BI da Alura, demonstrando minhas habilidades em análise de dados, modelagem, cálculos DAX e visualização.

## 📊 Dashboards Incluídos

- [Dashboard 1: Petshop Gatito](#dashboard-1-petshop-gatito)
- [Dashboard 2: E-commerce no Brasil](#dashboard-2-e-commerce-no-brasil)
- [Dashboard 3: Opuline](#dashboard-3-opuline)

---

## Dashboard 1: Gatito Petshop

### 📋 Visão Geral
Este dashboard foi desenvolvido para monitorar a saúde financeira e o comportamento de vendas do **Gatito Petshop**. Ele consolida dados de faturamento e vendas, permitindo uma análise rápida através de indicadores-chave (KPIs) e visuais interativos.

**Principais Insights e Funcionalidades:**
- **KPIs de Desempenho:** Acompanhamento em tempo real do faturamento total (R$ 2,03 Mi), média de pets por cliente (3) e volume de vendas (57 mil).
- **Análise Demográfica e Geográfica:** Distribuição do faturamento por gênero e ranking por bairro (destaque para Itaquera e Guaianases).
- **Sazonalidade:** Evolução do faturamento por ano, trimestre e mês, identificando tendências de mercado.
- **UX Interativa:** Utilização de *Image Grid* com ícones de produtos e barra de busca funcional para filtragem direta.

### 🖼️ Visualização
[📄 Clique aqui para visualizar o Dashboard](GatitoPetshop/Imagens/GatitoPetshop.png)

### 🏗️ Modelo de Dados
O projeto utiliza um **Esquema Estrela (Star Schema)**, garantindo máxima performance e organização:
- **Tabela Fato (`Vendas`):** Armazena os registros de transações, faturamento e quantidades.
- **Tabelas Dimensão (`Clientes` e `Produtos`):** Contêm os atributos necessários para os filtros e segmentações (Bairro, Gênero, Categoria, Marca).
- **Relacionamentos:** Conexões do tipo 1:N (um para muitos) com direção de filtro única das dimensões para a fato.

![Modelo de Dados Gatito](GatitoPetshop/Imagens/ModeloDadosGatitoPetshop.png)

### 📏 Medidas DAX
Para extrair inteligência dos dados, foram criadas medidas personalizadas. Abaixo, destaco o cálculo do valor médio por produto:

**Valor Médio por Produto Vendido:**
```dax
Valor_medio_por_produto_vendido = SUM('Vendas'[Faturamento]) / SUM(Vendas[Quantidade])
```

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
