# 📊 Desafio de Projeto: Análise de Vendas com Power BI

Desafio do curso **Analisando Dados com SQL Analytics e Power BI**, da DIO, trilha Universia *Primeiros passos em Power BI*, Módulo 2.

📂 **Base de dados:** `Financial Sample.xlsx` — 700 linhas, 5 países e 5 segmentos.

🔗 **Repositório de referência:** [julianazanelatto/power_bi_analyst](https://github.com/julianazanelatto/power_bi_analyst)

**✅ Status: concluído.**

O relatório possui três páginas: duas replicadas do curso e uma desenvolvida por mim. O arquivo `.pbix` está disponível neste repositório, e o relatório foi publicado no Power BI Service, no Meu workspace, com acesso privado.

---

# 🖥️ 1. Demonstração dos dashboards

## 📈 1.1. Sales Report

*Página replicada do curso.*

<img src="demo/pagina1.png" alt="Página 1: Sales Report" width="100%" />

<!-- VÍDEO PÁGINA 1: cole aqui a URL https://github.com/user-attachments/assets/... sozinha numa linha, sem colchetes e sem link -->

## 💰 1.2. Report de Lucro Detalhado

*Página replicada do curso.*

<img src="demo/pagina2.png" alt="Página 2: Report de Lucro Detalhado" width="100%" />

<!-- VÍDEO PÁGINA 2: cole aqui a URL https://github.com/user-attachments/assets/... sozinha numa linha, sem colchetes e sem link -->

## 🌎 1.3. Análise Geográfica

*Página autoral, desenvolvida para este desafio.*

<img src="demo/pagina3.png" alt="Página 3: Análise Geográfica" width="100%" />

<!-- VÍDEO PÁGINA 3: cole aqui a URL https://github.com/user-attachments/assets/... sozinha numa linha, sem colchetes e sem link -->

📁 Os arquivos originais em PNG e MP4 estão disponíveis na pasta [`demo/`](demo/).

---

# 🎯 2. Objetivo do desafio

Desenvolver uma análise visual das vendas e dos lucros utilizando o Power BI, explorando diferentes tipos de gráficos e organizando as informações para facilitar a interpretação dos resultados.

A terceira página amplia o relatório com uma análise geográfica, comparando vendas, unidades vendidas e lucro por país, além da distribuição do lucro por segmento.

---

# 📄 3. Organização das páginas

| Página | Conteúdo | Origem |
|---|---|---|
| 📈 1 | Dashboard de vendas: cards, áreas, barras, treemap, mapa, rosca e filtros | Replicada do curso |
| 💰 2 | Report de lucro detalhado: árvore de decomposição, cascata, radar e treemap | Replicada do curso |
| 🌎 3 | **Análise Geográfica:** mapas de vendas e lucro por país e gráfico de pizza por segmento | Autoral |

## 🗺️ 3.1. Visuais da página Análise Geográfica

| Visual | Tipo | Campos utilizados | Título |
|---|---|---|---|
| 🌎 Mapa 1 | Mapa de bolhas | Localização: `Country` · Tamanho: soma de `Sales` · Dica de ferramenta: soma de `Units Sold` | Vendas (Sales) e Unidades Vendidas por País |
| 💵 Mapa 2 | Mapa de bolhas | Localização: `Country` · Tamanho: soma de `Profit` | Lucro (Profit) por País |
| 🥧 Gráfico 3 | Gráfico de pizza | Legenda: `Segment` · Valores: soma de `Profit` | Lucro (Profit) por Segmento |

**📐 Organização visual:** o mapa de vendas fica em destaque à esquerda, enquanto o mapa de lucro e o gráfico de pizza ficam empilhados à direita.

O cabeçalho reaproveita o padrão visual da página 2, com fundo, logo, título e botão de voltar.

---

# 🔎 4. Valores de conferência

Os valores abaixo foram calculados diretamente do Excel para conferir os resultados dos visuais da terceira página.

> ℹ️ Os percentuais exibidos na pizza foram conferidos no Power BI Service em 28/09/2026.

## 🌎 4.1. Resultados por país

| País | Sales | Units Sold | Profit |
|---|---:|---:|---:|
| United States of America | 25.029.830,16 | 232.627,5 | 2.995.540,66 |
| Canada | 24.887.654,88 | 247.428,5 | 3.529.228,88 |
| France | 24.354.172,28 | 240.931,0 | 3.781.020,78 |
| Germany | 23.505.340,82 | 201.494,0 | 3.680.388,82 |
| Mexico | 20.949.352,11 | 203.325,0 | 2.907.523,11 |

## 🥧 4.2. Resultados por segmento

| Segmento | Profit | % do total | % exibido na pizza |
|---|---:|---:|---:|
| Government | 11.388.173,17 | 67,41% | 65,04% |
| Small Business | 4.143.168,50 | 24,52% | 23,66% |
| Channel Partners | 1.316.803,14 | 7,79% | 7,52% |
| Midmarket | 660.103,07 | 3,91% | 3,77% |
| Enterprise | -614.545,62 | -3,64% | Não exibido |

---

# ⚠️ 5. Pontos de atenção nos dados

### 🔴 5.1. Lucro negativo no segmento Enterprise

O segmento Enterprise apresenta lucro total negativo.

Gráficos de pizza e rosca não representam adequadamente valores negativos. Por isso, a fatia do Enterprise não aparece, embora o segmento conste na legenda do Power BI Service.

Os percentuais exibidos na pizza diferem dos percentuais calculados sobre o total porque a visualização considera apenas os segmentos positivos.

💡 **Alternativa analítica:** para comparar lucros positivos e negativos, um gráfico de barras permite representar melhor os resultados. A pizza foi mantida para atender à proposta do exercício.

### 🟡 5.2. Nome da coluna Sales

A coluna de vendas no Excel de origem chama-se `" Sales"`, com um espaço no início.

Isso não impede necessariamente a construção dos visuais, mas pode causar erros em expressões DAX e etapas do Power Query se a referência for digitada como `[Sales]`.

✅ **Boa prática:** renomear a coluna para `Sales` no Power Query.

### 🔵 5.3. Funcionamento dos mapas

Os mapas dependem do serviço de mapas do Power BI e das configurações do ambiente.

No Power BI Service, o administrador do tenant precisa permitir o uso de visuais de mapa e mapa de preenchimento. Na conta institucional utilizada neste projeto, os mapas renderizaram normalmente.

Em outros ambientes, os mapas podem aparecer em branco caso esse recurso esteja desabilitado, mesmo quando funcionam no Power BI Desktop.

---

# 🚀 6. Status do desafio

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

# ☁️ 7. Publicação no Power BI Service

O relatório foi publicado no Power BI Service, no **Meu workspace**, com as três páginas e os mapas renderizando.

O acesso é privado, vinculado à conta institucional, sem compartilhamento público. Por esse motivo, não há link público para abrir o relatório.

A imagem abaixo serve como evidência da publicação, mostrando a página **Análise Geográfica** no Power BI Service.

<img src="demo/relatorio_publicado_privado.png" alt="Relatório publicado no Power BI Service, página Análise Geográfica" width="100%" />

---

# 📁 8. Estrutura do projeto

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

# 🛠️ 9. Como abrir o projeto

**Requisito:** Power BI Desktop para Windows.

Na primeira abertura, podem ser necessários alguns ajustes de ambiente.

### 1️⃣ Configurar a fonte de dados

O Power BI pode armazenar o caminho absoluto do arquivo Excel.

1. Acesse **Transformar dados → Configurações da fonte de dados**.
2. Altere a origem para o arquivo `dataset/Financial Sample.xlsx` da sua cópia do repositório.
3. Clique em **Fechar e aplicar**.
4. Atualize os dados.

### 2️⃣ Instalar os visuais personalizados

A página 2 utiliza os visuais **Chiclet Slicer** e **Radar Chart**.

Caso não estejam disponíveis, procure-os em **Visualizações → Obter mais visuais**.

### 3️⃣ Habilitar os mapas

No Power BI Desktop, acesse:

**Arquivo → Opções e configurações → Opções → Segurança**

Habilite a opção **Usar visuais de mapa e mapa de preenchimento** e reinicie o Desktop, se necessário.

### 4️⃣ Conferir os resultados

Abra a página **Análise Geográfica** e compare os visuais com os valores apresentados na seção 4.

Se preferir reconstruir a terceira página do zero, consulte o guia [`docs/GUIA_PAGINA_3_MANUAL.md`](docs/GUIA_PAGINA_3_MANUAL.md).

---

<p align="center">
  <strong>📊 Análise de Vendas com Power BI</strong><br/>
  Transformando dados em visualizações para apoiar a análise de resultados.
</p>

<p align="center">
  <a href="https://github.com/julianazanelatto/power_bi_analyst">📚 Repositório do curso</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/maxgodoydev/Portfolio_Power_BI">💼 Portfólio Power BI</a>
</p>

<p align="center">
  <sub>Projeto de estudo • DIO • Power BI • Análise de Dados</sub>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&section=footer&height=100&color=0:312E81,50:2563EB,100:0E7490" width="100%" alt="Rodapé do projeto" />
</p>
