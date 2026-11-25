# Data Concepts

## Overview

This section introduces the fundamental concepts related to data and information, establishing a common vocabulary for Data Engineering, database development, analytics, and data management.

Understanding these concepts is essential for interpreting datasets, designing data structures, building data pipelines, and ensuring that data is correctly represented and used.

## Concepts

### 1. Data

Data represents raw facts, observations, measurements, values, or recorded events.

Examples:
- `Cleber`
- `150.75`
- `2026-11-25`
- `TRUE`

A single data value may have little meaning without context.

### 2. Information

Information is data organized, contextualized, or interpreted in a way that provides meaning and supports understanding or decision-making.

Example:

Raw data:

`150.75`

Contextualized information:

`The customer purchased products totaling R$ 150.75.`

### 3. Knowledge

Knowledge is the understanding derived from information, experience, analysis, and context, which can be used to support decisions and actions.

Example:

Analyzing sales information may reveal that a specific product is consistently purchased during a particular period, helping the business plan inventory.

### 4. Dataset

A dataset is a collection of related data organized for storage, processing, analysis, or exchange.

Datasets may be represented as tables, files, collections, documents, or other structures.

Examples:
- Customer dataset
- Sales dataset
- Product dataset
- Transaction dataset

### 5. Record

A record represents a collection of related data values describing a particular entity, event, or occurrence.

In a relational table, a record is generally represented by a row.

Example:

| Customer ID | Name | City |
|---|---|---|
| 101 | John Smith | New York |

This row represents a customer record.

### 6. Field

A field represents a specific data element within a record or data structure.

In a tabular dataset, a field is commonly represented by a column.

Examples:
- Customer ID
- Name
- City
- Birth Date

### 7. Attribute

An attribute describes a characteristic or property of an entity.

Example:

A customer entity may have the following attributes:
- Name
- Email
- Phone
- Address

Attributes are commonly represented as fields or columns in databases, although the concepts are not universally interchangeable across every data model.

### 8. Value

A value is the actual content stored in a field, attribute, variable, or data element.

Example:

| Field | Value |
|---|---|
| Name | John Smith |
| City | New York |
| Customer ID | 101 |

### 9. Entity

An entity represents something identifiable about which data is collected or maintained.

Examples:
- Customer
- Employee
- Product
- Company
- Vehicle
- Invoice

An entity is often represented by a table, object, document, or other data structure depending on the data model.

### 10. Data Source

A data source is the origin from which data is obtained.

Examples:
- Database
- API
- CSV file
- Spreadsheet
- Application
- Sensor
- External system

### 11. Data Target

A data target is the destination where data is delivered, stored, loaded, or made available.

Examples:
- Database table
- Data warehouse
- Data lake
- API
- File
- Analytics platform

### 12. Raw Data

Raw data is data collected from its source before, or with minimal, processing or transformation.

Raw data may contain inconsistencies, missing values, duplicates, formatting differences, or other characteristics that need to be evaluated during processing.

### 13. Processed Data

Processed data is data that has undergone one or more operations such as cleaning, validation, transformation, aggregation, enrichment, or normalization.

Processing is performed according to requirements and the intended use of the data.

## Conceptual Relationship

```text
Data
  |
  | Context, organization, interpretation
  v
Information
  |
  | Analysis, experience, understanding
  v
Knowledge
  |
  | Application and decision-making
  v
Action
```

## Practical Example

Consider a sales dataset:

| Sale ID | Customer | Product | Amount | Date |
|---|---|---|---:|---|
| 1001 | John | Laptop | 2500.00 | 2026-11-25 |
| 1002 | Mary | Monitor | 850.00 | 2026-11-25 |
| 1003 | John | Keyboard | 150.00 | 2026-11-25 |

In this example:

- **Dataset:** The complete sales collection.
- **Record:** Each individual sale represented by a row.
- **Field:** Sale ID, Customer, Product, Amount, and Date.
- **Attribute:** Characteristics associated with a sale.
- **Value:** The actual content of each field, such as `2500.00`.
- **Entity:** Sale, Customer, and Product.
- **Information:** Total sales amount, sales by customer, or sales by product.
- **Knowledge:** Insights derived from sales analysis that may support business decisions.

## Importance in Data Engineering

Understanding data concepts helps Data Engineers:

- Design appropriate data structures.
- Understand source and target systems.
- Build reliable data pipelines.
- Define data transformations.
- Interpret business requirements.
- Maintain consistent terminology.
- Improve data quality and documentation.
- Communicate effectively with technical and business teams.

## Related Topics

- [Data Types](../data-types/README.md)
- [Data Formats](../data-formats/README.md)
- [Data Structures](../data-structures/README.md)
- [Data Lifecycle](../data-lifecycle/README.md)
- [Metadata and Data Dictionary](../metadata-and-data-dictionary/README.md)

---

# Conceitos de Dados

## Visão Geral

Esta seção apresenta os conceitos fundamentais relacionados a dados e informações, estabelecendo um vocabulário comum para Engenharia de Dados, desenvolvimento de bancos de dados, analytics e gestão de dados.

Compreender esses conceitos é essencial para interpretar datasets, projetar estruturas de dados, construir pipelines e garantir que os dados sejam corretamente representados e utilizados.

## Conceitos

### 1. Dado (Data)

Dado representa fatos brutos, observações, medições, valores ou eventos registrados.

Exemplos:
- `Cleber`
- `150.75`
- `2026-11-25`
- `TRUE`

Um valor isolado pode ter pouco significado sem contexto.

### 2. Informação (Information)

Informação é o dado organizado, contextualizado ou interpretado de maneira que produza significado e contribua para o entendimento ou tomada de decisão.

Exemplo:

Dado bruto:

`150.75`

Informação contextualizada:

`O cliente comprou produtos no valor total de R$ 150,75.`

### 3. Conhecimento (Knowledge)

Conhecimento é o entendimento derivado de informações, experiências, análises e contexto, que pode ser utilizado para apoiar decisões e ações.

Exemplo:

A análise de informações de vendas pode revelar que determinado produto é comprado consistentemente em um período específico, ajudando a empresa a planejar seu estoque.

### 4. Dataset (Conjunto de Dados)

Dataset é uma coleção de dados relacionados, organizada para armazenamento, processamento, análise ou intercâmbio.

Datasets podem ser representados por tabelas, arquivos, coleções, documentos ou outras estruturas.

Exemplos:
- Dataset de clientes
- Dataset de vendas
- Dataset de produtos
- Dataset de transações

### 5. Record (Registro)

Record representa uma coleção de valores de dados relacionados que descrevem uma entidade, evento ou ocorrência específica.

Em uma tabela relacional, um record geralmente é representado por uma linha.

Exemplo:

| Customer ID | Name | City |
|---|---|---|
| 101 | John Smith | New York |

Essa linha representa um registro de cliente.

### 6. Field (Campo)

Field representa um elemento de dado específico dentro de um registro ou estrutura de dados.

Em um dataset tabular, um field é comumente representado por uma coluna.

Exemplos:
- Customer ID
- Name
- City
- Birth Date

### 7. Attribute (Atributo)

Attribute descreve uma característica ou propriedade de uma entidade.

Exemplo:

Uma entidade cliente pode possuir os seguintes atributos:
- Nome
- E-mail
- Telefone
- Endereço

Atributos são frequentemente representados como campos ou colunas em bancos de dados, embora os conceitos não sejam universalmente intercambiáveis em todos os modelos de dados.

### 8. Value (Valor)

Value é o conteúdo efetivamente armazenado em um campo, atributo, variável ou elemento de dados.

Exemplo:

| Field | Value |
|---|---|
| Name | John Smith |
| City | New York |
| Customer ID | 101 |

### 9. Entity (Entidade)

Entity representa algo identificável sobre o qual dados são coletados ou mantidos.

Exemplos:
- Cliente
- Funcionário
- Produto
- Empresa
- Veículo
- Nota fiscal

Uma entidade pode ser representada por uma tabela, objeto, documento ou outra estrutura, dependendo do modelo de dados utilizado.

### 10. Data Source (Fonte de Dados)

Data Source é a origem de onde os dados são obtidos.

Exemplos:
- Banco de dados
- API
- Arquivo CSV
- Planilha
- Aplicação
- Sensor
- Sistema externo

### 11. Data Target (Destino de Dados)

Data Target é o destino para onde os dados são entregues, armazenados, carregados ou disponibilizados.

Exemplos:
- Tabela de banco de dados
- Data Warehouse
- Data Lake
- API
- Arquivo
- Plataforma de analytics

### 12. Raw Data (Dados Brutos)

Raw Data são dados coletados de sua origem antes de, ou com processamento ou transformação mínimos.

Os dados brutos podem conter inconsistências, valores ausentes, duplicidades, diferenças de formatação ou outras características que precisam ser avaliadas durante o processamento.

### 13. Processed Data (Dados Processados)

Processed Data são dados que passaram por uma ou mais operações, como limpeza, validação, transformação, agregação, enriquecimento ou normalização.

O processamento é realizado de acordo com os requisitos e a finalidade de utilização dos dados.

## Relação Conceitual

```text
Dados
  |
  | Contextualização, organização, interpretação
  v
Informação
  |
  | Análise, experiência, compreensão
  v
Conhecimento
  |
  | Aplicação e tomada de decisão
  v
Ação
```

## Exemplo Prático

Considere um dataset de vendas:

| Sale ID | Customer | Product | Amount | Date |
|---|---|---|---:|---|
| 1001 | John | Laptop | 2500.00 | 2026-11-25 |
| 1002 | Mary | Monitor | 850.00 | 2026-11-25 |
| 1003 | John | Keyboard | 150.00 | 2026-11-25 |

Neste exemplo:

- **Dataset:** A coleção completa de vendas.
- **Record:** Cada venda individual representada por uma linha.
- **Field:** Sale ID, Customer, Product, Amount e Date.
- **Attribute:** Características associadas a uma venda.
- **Value:** O conteúdo de cada campo, como `2500.00`.
- **Entity:** Venda, Cliente e Produto.
- **Information:** Valor total vendido, vendas por cliente ou por produto.
- **Knowledge:** Insights derivados da análise de vendas que podem apoiar decisões de negócio.

## Importância na Engenharia de Dados

Compreender os conceitos de dados ajuda os Data Engineers a:

- Projetar estruturas de dados adequadas.
- Compreender sistemas de origem e destino.
- Construir pipelines de dados confiáveis.
- Definir transformações.
- Interpretar requisitos de negócio.
- Manter terminologia consistente.
- Melhorar qualidade e documentação dos dados.
- Comunicar-se efetivamente com equipes técnicas e de negócio.

## Tópicos Relacionados

- [Tipos de Dados](../data-types/README.md)
- [Formatos de Dados](../data-formats/README.md)
- [Estruturas de Dados](../data-structures/README.md)
- [Ciclo de Vida dos Dados](../data-lifecycle/README.md)
- [Metadados e Dicionário de Dados](../metadata-and-data-dictionary/README.md)
