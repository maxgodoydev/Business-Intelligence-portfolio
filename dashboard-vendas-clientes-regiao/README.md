<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:14532D,100:16A34A&height=180&section=header&text=DASHBOARD%20DE%20VENDAS&fontSize=34&fontColor=FFFFFF&fontAlignY=45&desc=Clientes%20%7C%20Regi%C3%B5es%20%7C%20Business%20Intelligence&descSize=16&descAlignY=70" width="100%" alt="Dashboard de Vendas, Clientes e Região">

<br>

![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Medidas%20Anal%C3%ADticas-16A34A?style=for-the-badge)
![SQL Server](https://img.shields.io/badge/SQL%20Server-Banco%20de%20Dados-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)

**Projeto de Business Intelligence para análise de vendas, clientes e desempenho regional.**

</div>

---

## 📌 Sobre o Projeto

O **Dashboard de Vendas, Clientes e Região** é um projeto de Business Intelligence desenvolvido com Power BI e SQL Server, com o objetivo de transformar dados relacionais em informações relevantes para a análise do desempenho comercial.

A solução utiliza o banco de dados `db_atividade_bi` e reúne informações sobre pedidos, pagamentos, produtos, clientes e vendedores.

Os dados são apresentados em quatro dashboards, organizados para facilitar a identificação de padrões de consumo, o acompanhamento do faturamento e a comparação dos resultados comerciais.

O projeto contempla **14 perguntas de negócio**, distribuídas entre as análises executiva, de vendas, de clientes e regional.

### 🎯 Objetivo

Desenvolver uma solução analítica que permita acompanhar indicadores comerciais, comparar resultados, compreender o comportamento dos clientes e identificar oportunidades de análise por região, produto e vendedor.

---

## 📊 Dashboards e Perguntas Respondidas

### 💰 01. Dashboard de Vendas

![Dashboard de Vendas](./assets/01-vendas-melhor-vendedor.png)

**Perguntas de negócio respondidas:**

- ✅ Qual é o faturamento total por região?
- ✅ Como o faturamento varia ao longo dos períodos?
- ✅ Qual é o ranking de vendedores?
- ✅ Como o faturamento varia por vendedor e período?
- ✅ Quais são as formas de pagamento utilizadas?
- ✅ Como evoluem as vendas por vendedor?

### 👥 02. Dashboard de Clientes

![Dashboard de Clientes](./assets/02-clientes.png)

**Perguntas de negócio respondidas:**

- ✅ Qual é a quantidade total de pedidos por cliente?
- ✅ Qual é o ranking de clientes?
- ✅ Qual é a proporção de clientes ativos e inativos?
- ✅ Como os clientes estão distribuídos geograficamente?

### 🌎 03. Dashboard Regional

![Dashboard Regional](./assets/03-regiao.png)

**Perguntas de negócio respondidas:**

- ✅ Quais são os produtos mais vendidos por região?
- ✅ Qual é a quantidade total de itens vendidos?
- ✅ Como o faturamento se distribui entre as regiões?

### 📈 04. Dashboard Executivo

![Dashboard Executivo](./assets/04-executivo-final.png)

**Análises contempladas:**

- ✅ Consolidação dos principais indicadores comerciais.
- ✅ Visão geral do desempenho das vendas.
- ✅ Comparação dos resultados para apoiar a tomada de decisão.

---

## 🎯 Perguntas de Negócio do Projeto

As análises foram estruturadas a partir de 14 perguntas de negócio relacionadas ao desempenho comercial.

| Nº | Pergunta |
|:---:|---|
| 01 | Qual é o faturamento total por região? |
| 02 | Qual é a quantidade total de pedidos por cliente? |
| 03 | Qual é o ticket médio por pedido? |
| 04 | Como o faturamento varia ao longo dos períodos? |
| 05 | Qual é o ranking de vendedores? |
| 06 | Qual é o ranking de clientes? |
| 07 | Qual é a quantidade total de itens vendidos? |
| 08 | Quais são os produtos mais vendidos por região? |
| 09 | Como o faturamento varia por vendedor e período? |
| 10 | Quais são as formas de pagamento utilizadas? |
| 11 | Qual é a proporção de clientes ativos e inativos? |
| 12 | Como os clientes estão distribuídos geograficamente? |
| 13 | Como evoluem as vendas por vendedor? |
| 14 | Como consolidar os principais indicadores em um dashboard executivo? |

---

## 🗃️ Modelo de Dados

O modelo utiliza tabelas relacionais para organizar as informações de pedidos, pagamentos, itens, clientes e vendedores.

A estrutura permite relacionar os dados comerciais e utilizá-los na construção dos indicadores e das visualizações no Power BI.

### 📋 Tabelas utilizadas

| Tabela | Descrição |
|---|---|
| `TB_PEDIDO` | Tabela central de pedidos, com um registro por pedido. |
| `TB_CAIXA` | Armazena as informações de pagamento relacionadas aos pedidos. |
| `TB_PEDIDO_HAS_TB_ITEM` | Tabela associativa que conecta pedidos e itens. |
| `TB_ITEM` | Contém os dados dos produtos comercializados. |
| `TB_CLIENTE` | Contém informações dos clientes, incluindo região e atividade. |
| `TB_VENDEDOR` | Contém os dados dos vendedores. |

### 🔗 Relacionamentos

```text
TB_CAIXA (1) ──── (1) TB_PEDIDO

TB_PEDIDO (M) ──── (1) TB_CLIENTE

TB_PEDIDO (M) ──── (1) TB_VENDEDOR

TB_PEDIDO_HAS_TB_ITEM (M) ──── (1) TB_ITEM

TB_PEDIDO_HAS_TB_ITEM (1) ──── (1) TB_PEDIDO
```

A tabela associativa `TB_PEDIDO_HAS_TB_ITEM` permite representar a relação entre pedidos e itens, possibilitando analisar os produtos comercializados em cada pedido.

---

## 🧮 Medidas e Cálculos DAX

O DAX foi utilizado para criar medidas analíticas necessárias à construção dos indicadores e das classificações presentes nos dashboards.

### 💵 Ticket Médio Formatado

Calcula o valor médio por pedido, dividindo a soma dos pagamentos pela quantidade distinta de pedidos.

```dax
Ticket Medio Formatado =
FORMAT(
    DIVIDE(
        SUM(TB_CAIXA[VL_Pagamento]),
        DISTINCTCOUNT(TB_CAIXA[ID_Pedido])
    ),
    "R$ #,##0.00"
)
```

**Funções utilizadas:**

- ✅ `SUM`: soma os valores de pagamento.
- ✅ `DISTINCTCOUNT`: conta os pedidos distintos.
- ✅ `DIVIDE`: realiza a divisão com tratamento para denominadores inválidos ou iguais a zero.
- ✅ `FORMAT`: apresenta o resultado no formato monetário.

### 🏆 Ranking de Produtos por Região

Classifica os produtos conforme a quantidade vendida, considerando o contexto da região analisada.

```dax
Rank_Produto_Regiao =
RANKX(
    FILTER(
        ALL(TB_ITEM[DESC_ITEM]),
        NOT(ISBLANK([Qtd_Vendida]))
    ),
    CALCULATE(
        [Qtd_Vendida],
        ALLEXCEPT(TB_CLIENTE, TB_CLIENTE[Regiao])
    ),
    ,
    DESC,
    DENSE
)
```

**Funções utilizadas:**

- ✅ `RANKX`: calcula a posição dos produtos no ranking.
- ✅ `FILTER`: filtra os produtos considerados na classificação.
- ✅ `ALL`: remove os filtros aplicados à coluna de produtos.
- ✅ `CALCULATE`: avalia a medida em um contexto de filtro específico.
- ✅ `ALLEXCEPT`: preserva o filtro de região na tabela de clientes.
- ✅ `ISBLANK`: verifica se o resultado está em branco.

---

## 💡 Principais Insights

A análise dos dados permite observar diferenças no faturamento regional, na composição da base de clientes e no comportamento de compra.

Os resultados abaixo correspondem à base de dados utilizada no projeto.

### 🌎 Faturamento por Região

| Região | Faturamento |
|---|---:|
| Sudeste | R$ 8,7 milhões |
| Sul | R$ 4,8 milhões |

- ✅ O Sudeste apresenta o maior faturamento entre as regiões destacadas.
- ✅ A região Sul aparece em seguida, com R$ 4,8 milhões em faturamento.
- ✅ A comparação regional permite investigar diferenças no desempenho comercial.

### 👥 Situação dos Clientes

| Indicador | Resultado |
|---|---:|
| Clientes ativos | 81% |
| Clientes inativos | 19% |

- ✅ A maior parte da base analisada é composta por clientes ativos.
- ✅ Os clientes inativos representam uma oportunidade de investigação sobre o comportamento de compra.
- ✅ A segmentação permite acompanhar a composição da base de clientes.

### 🛒 Comportamento de Compra

O cliente Truman possui **22 pedidos**, mas não ocupa a primeira posição em faturamento acumulado.

- ✅ A quantidade de pedidos não determina, isoladamente, o faturamento acumulado de um cliente.
- ✅ O valor das compras também precisa ser considerado para avaliar a contribuição financeira.
- ✅ A combinação de indicadores permite uma análise mais completa do comportamento de compra.

---

## 🔎 Preparação dos Dados

Os dados foram importados diretamente do SQL Server para o Power BI.

- ✅ Conexão com o banco de dados relacional `db_atividade_bi`.
- ✅ Importação das tabelas utilizadas na análise.
- ✅ Utilização dos relacionamentos entre as tabelas.
- ✅ Desenvolvimento de medidas DAX para os indicadores.

**Observação:** não foram realizadas transformações ou tratamentos no Power Query, conforme o escopo adotado para o projeto.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Aplicação |
|---|---|
| Microsoft SQL Server | Armazenamento dos dados relacionais. |
| Microsoft Power BI | Construção dos dashboards e visualização dos indicadores. |
| DAX | Criação de medidas e cálculos analíticos. |

---

## 📁 Arquivos do Projeto

| Arquivo | Descrição |
|---|---|
| `Dashboard_Vendas_Clientes_Regiao.pbix` | Arquivo principal do projeto Power BI. |
| `assets/04-executivo-final.png` | Imagem do dashboard executivo. |
| `assets/01-vendas-melhor-vendedor.png` | Imagem do dashboard de vendas. |
| `assets/02-clientes.png` | Imagem do dashboard de clientes. |
| `assets/03-regiao.png` | Imagem do dashboard regional. |

---

<div align="center">

**📊 Dashboard de Vendas, Clientes e Região**

Desenvolvido para fins de estudo e portfólio.

**Power BI · DAX · SQL Server**

</div>
