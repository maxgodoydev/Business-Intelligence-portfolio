<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:312E81,50:2563EB,100:0E7490&height=180&section=header&text=AN%C3%81LISE%20DE%20VENDAS&fontSize=34&fontColor=FFFFFF&fontAlignY=42&desc=Power%20BI%20%7C%20Business%20Intelligence%20%7C%20An%C3%A1lise%20de%20Dados&descSize=15&descAlignY=68" width="100%" alt="Análise de Vendas com Power BI">

<br>

![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DIO](https://img.shields.io/badge/DIO-Desafio%20de%20Projeto-6C3FC5?style=for-the-badge)
![Excel](https://img.shields.io/badge/Excel-Base%20de%20Dados-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

**Desafio de Projeto — Analisando Dados com SQL Analytics e Power BI**

</div>

---

## 📌 Sobre o Projeto

Projeto desenvolvido no curso **Analisando Dados com SQL Analytics e Power BI**, da DIO, na trilha Universia *Primeiros passos em Power BI*, Módulo 2.

O desafio utiliza a base `Financial Sample.xlsx`, composta por 700 linhas, cinco países e cinco segmentos, para desenvolver análises visuais de vendas e lucros no Power BI.

O relatório possui três páginas: duas replicadas a partir do curso e uma terceira desenvolvida de forma autoral, ampliando a análise com visualizações geográficas e distribuição do lucro por segmento.

### 🎯 Objetivo

Desenvolver uma análise visual de vendas e lucros utilizando diferentes tipos de gráficos, organizando as informações para facilitar a interpretação dos resultados.

A página autoral amplia o relatório com comparações de vendas, unidades vendidas e lucro por país, além da distribuição do lucro por segmento.

### 📂 Informações do Projeto

| Item | Descrição |
|---|---|
| Curso | Analisando Dados com SQL Analytics e Power BI |
| Instituição | DIO — trilha Universia |
| Módulo | Módulo 2 |
| Base de dados | `Financial Sample.xlsx` |
| Quantidade de registros | 700 linhas |
| Países | 5 |
| Segmentos | 5 |
| Relatório | `relatorio/relatorio_criativo_desafio_modulo2.pbix` |
| Status | ✅ Concluído |

🔗 **Repositório de referência:** [julianazanelatto/power_bi_analyst](https://github.com/julianazanelatto/power_bi_analyst)

---

## 🖥️ Demonstração dos Dashboards

O relatório está organizado em três páginas, seguindo uma sequência que começa com a análise de vendas, passa pelo detalhamento do lucro e termina com a análise geográfica autoral.

### 📈 01. Sales Report

*Página replicada do curso.*

<img src="demo/pagina1.png" alt="Página 1: Sales Report" width="100%" />

**Análises contempladas:**

- ✅ Indicadores e cards de vendas.
- ✅ Comparações por meio de gráficos de áreas e barras.
- ✅ Distribuição visual por treemap, mapa e gráfico de rosca.
- ✅ Utilização de filtros para explorar os dados.

<!-- VÍDEO PÁGINA 1: cole aqui a URL https://github.com/user-attachments/assets/... sozinha numa linha, sem colchetes e sem link -->

### 💰 02. Report de Lucro Detalhado

*Página replicada do curso.*

<img src="demo/pagina2.png" alt="Página 2: Report de Lucro Detalhado" width="100%" />

**Análises contempladas:**

- ✅ Exploração do lucro por meio de árvore de decomposição.
- ✅ Análise de variações com gráfico de cascata.
- ✅ Comparação visual com gráfico radar.
- ✅ Distribuição por treemap.

<!-- VÍDEO PÁGINA 2: cole aqui a URL https://github.com/user-attachments/assets/... sozinha numa linha, sem colchetes e sem link -->

### 🌎 03. Análise Geográfica

*Página autoral, desenvolvida para este desafio.*

<img src="demo/pagina3.png" alt="Página 3: Análise Geográfica" width="100%" />

**Perguntas de negócio respondidas:**

- ✅ Como as vendas se distribuem entre os países?
- ✅ Como as unidades vendidas se distribuem geograficamente?
- ✅ Quais países apresentam maior lucro?
- ✅ Como o lucro está distribuído entre os segmentos?

<!-- VÍDEO PÁGINA 3: cole aqui a URL https://github.com/user-attachments/assets/... sozinha numa linha, sem colchetes e sem link -->

📁 Os arquivos originais em PNG e MP4 estão disponíveis na pasta [`demo/`](demo/).

---

## 🎯 Objetivo e Organização das Páginas

O projeto foi desenvolvido para explorar diferentes formas de visualização e análise de dados no Power BI.

| Página | Conteúdo | Origem |
|---|---|---|
| 📈 01 | Dashboard de vendas: cards, áreas, barras, treemap, mapa, rosca e filtros | Replicada do curso |
| 💰 02 | Relatório de lucro detalhado: árvore de decomposição, cascata, radar e treemap | Replicada do curso |
| 🌎 03 | Análise geográfica: mapas de vendas e lucro por país e gráfico de pizza por segmento | Autoral |

---

## 🗺️ Visuais da Página Análise Geográfica

A terceira página foi desenvolvida para ampliar o relatório com comparações geográficas e análise do lucro por segmento.

### 📊 Configuração dos Visuais

| Visual | Tipo | Campos utilizados | Título |
|---|---|---|---|
| 🌎 Mapa 1 | Mapa de bolhas | Localização: `Country` · Tamanho: soma de `Sales` · Dica de ferramenta: soma de `Units Sold` | Vendas (Sales) e Unidades Vendidas por País |
| 💵 Mapa 2 | Mapa de bolhas | Localização: `Country` · Tamanho: soma de `Profit` | Lucro (Profit) por País |
| 🥧 Gráfico 3 | Gráfico de pizza | Legenda: `Segment` · Valores: soma de `Profit` | Lucro (Profit) por Segmento |

### 📐 Organização Visual

- ✅ Mapa de vendas em destaque à esquerda.
- ✅ Mapa de lucro posicionado à direita.
- ✅ Gráfico de pizza empilhado abaixo do mapa de lucro.
- ✅ Cabeçalho reaproveitando o padrão visual da página 2, com fundo, logo, título e botão de voltar.

---

## 🔎 Valores de Conferência

Os valores abaixo foram calculados diretamente do Excel para conferir os resultados dos visuais da terceira página.

> ℹ️ Os percentuais exibidos na pizza foram conferidos no Power BI Service em 28/09/2026.

### 🌎 Resultados por País

| País | Sales | Units Sold | Profit |
|---|---:|---:|---:|
| United States of America | 25.029.830,16 | 232.627,5 | 2.995.540,66 |
| Canada | 24.887.654,88 | 247.428,5 | 3.529.228,88 |
| France | 24.354.172,28 | 240.931,0 | 3.781.020,78 |
| Germany | 23.505.340,82 | 201.494,0 | 3.680.388,82 |
| Mexico | 20.949.352,11 | 203.325,0 | 2.907.523,11 |

### 🥧 Resultados por Segmento

| Segmento | Profit | % do total | % exibido na pizza |
|---|---:|---:|---:|
| Government | 11.388.173,17 | 67,41% | 65,04% |
| Small Business | 4.143.168,50 | 24,52% | 23,66% |
| Channel Partners | 1.316.803,14 | 7,79% | 7,52% |
| Midmarket | 660.103,07 | 3,91% | 3,77% |
| Enterprise | -614.545,62 | -3,64% | Não exibido |

---

## ⚠️ Pontos de Atenção nos Dados

### 🔴 Lucro Negativo no Segmento Enterprise

O segmento Enterprise apresenta lucro total negativo.

Gráficos de pizza e rosca não representam adequadamente valores negativos. Por isso, a fatia do Enterprise não aparece, embora o segmento conste na legenda do Power BI Service.

Os percentuais exibidos na pizza diferem dos percentuais calculados sobre o total porque a visualização considera apenas os segmentos positivos.

**💡 Alternativa analítica:** para comparar lucros positivos e negativos, um gráfico de barras permite representar melhor os resultados. A pizza foi mantida para atender à proposta do exercício.

### 🟡 Nome da Coluna Sales

A coluna de vendas no Excel de origem chama-se `" Sales"`, com um espaço no início.

Isso não impede necessariamente a construção dos visuais, mas pode causar erros em expressões DAX e etapas do Power Query se a referência for digitada como `[Sales]`.

**✅ Boa prática:** renomear a coluna para `Sales` no Power Query.

### 🔵 Funcionamento dos Mapas

Os mapas dependem do serviço de mapas do Power BI e das configurações do ambiente.

No Power BI Service, o administrador do tenant precisa permitir o uso de visuais de mapa e mapa de preenchimento. Na conta institucional utilizada neste projeto, os mapas renderizaram normalmente.

Em outros ambientes, os mapas podem aparecer em branco caso esse recurso esteja desabilitado, mesmo quando funcionam no Power BI Desktop.

---

## 🚀 Status do Desafio

| Item do enunciado | Status |
|---|---|
| 📈 Replicar as páginas 1 e 2 | ✅ Incluídas no arquivo, a partir do relatório criativo do repositório do curso |
| 🌎 Mapa de vendas e unidades por país | ✅ Concluído |
| 💵 Mapa de lucro por país | ✅ Concluído |
| 🥧 Gráfico de pizza de lucro por segmento | ✅ Concluído |
| 📐 Organizar os visuais | ✅ Concluído |
| 🏷️ Definir títulos claros | ✅ Concluído |
| 🔎 Configurar dicas de ferramenta | ✅ Concluído — `Units Sold` no primeiro mapa |
| ☁️ Publicar no Power BI Service | ✅ Publicado no Meu workspace, com acesso privado |
| 💾 Salvar o arquivo do relatório | ✅ Arquivo `.pbix` disponível no repositório |

🔗 **Projeto de referência:** [julianazanelatto/power_bi_analyst](https://github.com/julianazanelatto/power_bi_analyst)

---

## ☁️ Publicação no Power BI Service

O relatório foi publicado no Power BI Service, no **Meu workspace**, com as três páginas e os mapas renderizando.

O acesso é privado, vinculado à conta institucional, sem compartilhamento público. Por esse motivo, não há link público para abrir o relatório.

A imagem abaixo serve como evidência da publicação, mostrando a página **Análise Geográfica** no Power BI Service.

<img src="demo/relatorio_publicado_privado.png" alt="Relatório publicado no Power BI Service, página Análise Geográfica" width="100%" />

---

## 📁 Estrutura do Projeto

```text
.
├── relatorio/
│   └── relatorio_criativo_desafio_modulo2.pbix
├── dataset/
│   └── Financial Sample.xlsx
├── demo/
│   ├── pagina1.png
│   ├── pagina2.png
│   ├── pagina3.png
│   ├── vídeos curtos em MP4
│   └── relatorio_publicado_privado.png
└── docs/
    ├── GUIA_PAGINA_3_MANUAL.md
    ├── conferencia_por_pais.csv
    └── conferencia_por_segmento.csv
```

---

## 🛠️ Como Abrir o Projeto

**Requisito:** Power BI Desktop para Windows.

Na primeira abertura, podem ser necessários alguns ajustes de ambiente.

### 1️⃣ Configurar a Fonte de Dados

O Power BI pode armazenar o caminho absoluto do arquivo Excel.

1. Acesse **Transformar dados → Configurações da fonte de dados**.
2. Altere a origem para o arquivo `dataset/Financial Sample.xlsx` da sua cópia do repositório.
3. Clique em **Fechar e aplicar**.
4. Atualize os dados.

### 2️⃣ Instalar os Visuais Personalizados

A página 2 utiliza os visuais **Chiclet Slicer** e **Radar Chart**.

Caso não estejam disponíveis, procure-os em **Visualizações → Obter mais visuais**.

### 3️⃣ Habilitar os Mapas

No Power BI Desktop, acesse:

**Arquivo → Opções e configurações → Opções → Segurança**

Habilite a opção **Usar visuais de mapa e mapa de preenchimento** e reinicie o Desktop, se necessário.

### 4️⃣ Conferir os Resultados

Abra a página **Análise Geográfica** e compare os visuais com os valores apresentados na seção de conferência.

Se preferir reconstruir a terceira página do zero, consulte o guia [`docs/GUIA_PAGINA_3_MANUAL.md`](docs/GUIA_PAGINA_3_MANUAL.md).

---

<div align="center">

**📊 Análise de Vendas com Power BI**

Transformando dados em visualizações para apoiar a análise de resultados.

📚 [Repositório do curso](https://github.com/julianazanelatto/power_bi_analyst) · 💼 [Portfólio Power BI](https://github.com/maxgodoydev/Portfolio_Power_BI)

<sub>Projeto de estudo · DIO · Power BI · Análise de Dados</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&section=footer&height=100&color=0:312E81,50:2563EB,100:0E7490" width="100%" alt="Rodapé do projeto">

</div>
