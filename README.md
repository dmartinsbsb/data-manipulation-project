# Desafio de Manipulação de Dados - Data Solutions Inc.

## Contexto

A Data Solutions Inc. é uma empresa especializada na análise de dados, fornecendo soluções para diversos setores, como marketing, vendas e ciência de dados. Recentemente, um grande cliente enviou um conjunto de dados com informações sobre compras, clientes e produtos. No entanto, o arquivo está bruto e precisa ser limpo e preparado para atender a diferentes necessidades analíticas de cada time da empresa. Como Analista de Dados, o objetivo é transformar esse conjunto de dados em relatórios úteis e prontos para análise, atendendo às solicitações de diferentes áreas da empresa.

## Objetivo do Desafio

O desafio consistiu em limpar e manipular um dataset bruto com dados de compras e clientes para gerar arquivos de análise para os times de Vendas, Marketing e Ciência de Dados. Para cada time, foram feitas as seguintes solicitações:

### Solicitação 1: Time de Vendas

#### Objetivo

O time de vendas precisa entender o desempenho de vendas por região. Para isso, solicitam um arquivo contendo as seguintes informações:

- ID do Cliente
- Nome do Cliente
- Região
- Total gasto por cliente

Os dados foram agregados por cliente e ordenados pelo maior total gasto.

#### Etapas Realizadas

1. **Agrupamento de dados**: Agrupei os dados por ID do Cliente e Região, somando o total gasto por cliente.
2. **Ordenação**: Organizei o dataset pelo total gasto de forma decrescente, para facilitar a análise de quais clientes mais contribuíram para as vendas.
3. **Exclusão de duplicatas**: O objetivo era garantir que o total gasto fosse único por cliente, evitando registros duplicados de compras.

#### Resultado

O arquivo final contém informações como ID do Cliente, Nome do Cliente, Região e Total gasto por cliente, pronto para análise do time de vendas.

---

### Solicitação 2: Time de Marketing

#### Objetivo

O time de marketing quer segmentar os clientes com base em sua faixa etária e padrão de compras. As seguintes informações são solicitadas:

- ID do Cliente
- Faixa Etária (por exemplo: "<25", "25-40", ">40")
- Média de gastos por cliente
- Número total de compras realizadas
- Classificação de frequência (Alta ou Baixa Frequência)

#### Etapas Realizadas

1. **Cálculo da faixa etária**: Criei categorias de faixa etária para segmentar os clientes de acordo com sua idade, utilizando condições baseadas em intervalos de idade.
2. **Média de gastos**: Calculei a média de gastos por cliente com base no valor total de compras.
3. **Número de compras**: Obtive o número total de compras realizadas por cada cliente.
4. **Segmentação por frequência**: Classifiquei os clientes em Alta Frequência ou Baixa Frequência com base no número de compras realizadas (clientes com mais de 20 compras foram classificados como Alta Frequência).

#### Resultado

O dataset final contém ID do Cliente, Faixa Etária, Média de gastos, Número de compras e Classificação de Frequência de Compras (Alta ou Baixa Frequência), pronto para análise de marketing.

---

### Solicitação 3: Time de Ciência de Dados

#### Objetivo

O time de ciência de dados deseja um dataset limpo para explorar padrões e desenvolver modelos de previsão. As informações solicitadas são:

- ID do Cliente
- Data da Compra
- Valor da Compra
- Produto
- Região
- Idade

Além disso, as seguintes transformações precisam ser feitas:

- Tratamento de valores nulos (preenchidos ou removidos)
- Conversão de colunas categóricas para valores numéricos para facilitar o uso em modelos de machine learning.

#### Etapas Realizadas

1. **Tratamento de valores nulos**: Garantir que, caso fosse necessário, valores nulos fossem preenchidos ou removidos adequadamente.
2. **Conversão de colunas categóricas**: As colunas Região e Produto foram convertidas de variáveis categóricas para valores numéricos utilizando a técnica de Label Encoding. Isso permite que modelos de machine learning possam lidar melhor com essas variáveis.
3. **Conversão de tipos de dados**: A coluna Data da Compra foi convertida de string para o formato `datetime`, facilitando a manipulação e análise temporal.

#### Resultado

O dataset final contém as colunas relevantes para análise (como ID do Cliente, Data da Compra, Valor da Compra, Produto, Região, e Idade), com valores nulos tratados e colunas categóricas convertidas para numérico, pronto para ser usado em análises de dados avançadas e construção de modelos de previsão.

---

## Tecnologias e Ferramentas Utilizadas

- **Python**: Linguagem principal utilizada para manipulação de dados.
- **Pandas**: Biblioteca fundamental para a manipulação e análise de dados.
- **Scikit-learn**: Utilizada para a conversão de variáveis categóricas com Label Encoding.
- **NumPy**: Auxiliou nas operações matemáticas e de manipulação de dados.
- **Matplotlib/Seaborn**: Bibliotecas de visualização de dados (não incluídas explicitamente no desafio, mas sempre úteis).

---

## Conclusão

Neste desafio de manipulação de dados, o principal objetivo foi limpar e transformar um dataset bruto para fornecer insights úteis para três times de uma empresa fictícia. Ao longo do processo, foram realizadas:

- Agregação de dados
- Tratamento de valores nulos
- Transformação de variáveis categóricas em numéricas
- Segmentação de clientes com base em seus comportamentos de compra

Com esses dados limpos e estruturados, cada time pode agora analisar as informações de forma eficaz, seja para entender o desempenho de vendas, segmentar clientes para campanhas de marketing ou construir modelos preditivos no time de ciência de dados.

