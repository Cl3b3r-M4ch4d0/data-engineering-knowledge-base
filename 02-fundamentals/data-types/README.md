# Data Types

## Overview

Data types define the nature, representation, characteristics, and permitted operations of values stored, processed, or exchanged within a data system.

They help systems determine how data should be interpreted, validated, stored, manipulated, compared, and processed.

Choosing appropriate data types is important for data integrity, storage efficiency, processing performance, compatibility between systems, and the reliability of data pipelines.

## 1. Why Data Types Matter

Data types influence:

- Data validation and integrity.
- Storage requirements.
- Precision and accuracy.
- Mathematical and logical operations.
- Sorting and comparison behavior.
- Processing performance.
- Compatibility between databases, applications, programming languages, and data formats.
- Data ingestion, transformation, and serialization.

Incorrect data type selection may result in truncation, precision loss, conversion errors, incorrect comparisons, or unexpected behavior.

## 2. Fundamental Data Types

### 2.1 Integer

Represents whole numbers without fractional components.

Examples:
- `10`
- `-25`
- `0`
- `1000000`

Common applications:
- Counters.
- Quantities.
- Identifiers when numeric operations or numeric representation are appropriate.
- Number of records.
- Number of units sold.

Integer types may have different storage sizes and ranges depending on the system.

### 2.2 Decimal / Numeric

Represents numbers with fractional components and, depending on the implementation, controlled precision and scale.

Examples:
- `10.50`
- `1500.75`
- `-25.99`

Common applications:
- Financial values.
- Prices.
- Taxes.
- Measurements requiring decimal precision.

Fixed-precision decimal types are generally preferable to binary floating-point types for financial calculations that require exact decimal representation.

### 2.3 Floating-Point

Represents numbers using floating-point arithmetic, generally supporting a wide range of values with approximate precision.

Common types:
- Float
- Double

Examples:
- `3.141592`
- `0.000001`
- `6.02e23`

Common applications:
- Scientific calculations.
- Statistical analysis.
- Engineering measurements.
- Machine learning.
- Numerical simulations.

Floating-point values may introduce rounding differences because some decimal values cannot be represented exactly in binary.

### 2.4 String / Text

Represents textual data, character sequences, or combinations of characters.

Examples:
- `John Smith`
- `Brazil`
- `customer@example.com`
- `ABC-123`

Common applications:
- Names.
- Addresses.
- Descriptions.
- Codes.
- JSON fragments.
- Textual identifiers.

Strings may have variable or fixed length depending on the implementation.

### 2.5 Boolean

Represents a logical value with two possible states, commonly:

- `TRUE`
- `FALSE`

Common applications:
- Active or inactive flags.
- Validation results.
- Feature indicators.
- Logical conditions.
- Status indicators.

Some systems also support nullable Boolean values, which introduce an additional unknown or missing state.

### 2.6 Date

Represents a calendar date without necessarily including a time component.

Example:

`2026-11-25`

Common applications:
- Birth dates.
- Invoice dates.
- Contract dates.
- Business dates.
- Due dates.

### 2.7 Time

Represents a time of day without necessarily including a calendar date.

Example:

`14:30:45`

Common applications:
- Business opening hours.
- Daily schedules.
- Time-of-day measurements.

Depending on the system, time may include fractional seconds or timezone-related information.

### 2.8 DateTime / Timestamp

Represents a date and time, generally with varying precision.

Example:

`2026-11-25 14:30:45`

Common applications:
- Event registration.
- Transaction timestamps.
- System logs.
- Process execution times.
- Data ingestion tracking.

Some implementations distinguish between timestamps with timezone information and timestamps without timezone information.

### 2.9 Binary

Represents data as sequences of bytes rather than conventional textual values.

Examples:
- `0x48656C6C6F`
- Binary file content.

Common applications:
- Images.
- Documents.
- Encoded file content.
- Byte arrays.
- Raw data payloads.

Binary data may be stored directly in a database or externally in object storage, with a reference maintained in the database.

### 2.10 Null / Missing Value

Represents the absence of a value, an unknown value, or an unavailable value, depending on the system and context.

`NULL` is not equivalent to:
- `0`
- Empty string (`''`)
- `FALSE`
- A literal text value such as `'NULL'`

Null handling is important in SQL, data transformations, validation, aggregations, and data quality rules.

## 3. Specialized and Complex Data Types

### 3.1 Array

Represents an ordered collection of values.

Example:

```json
[10, 20, 30, 40]
```

Arrays may contain elements of the same type or, depending on the implementation, multiple types.

Common applications:
- Lists of measurements.
- Collections of identifiers.
- Repeated attributes.
- Nested data structures.

### 3.2 Object / Struct

Represents a collection of named properties or fields, potentially with different data types.

Example:

```json
{
  "id": 101,
  "name": "John",
  "active": true
}
```

Common applications:
- Nested records.
- API payloads.
- JSON data.
- Complex schemas.

### 3.3 Map / Dictionary

Represents a collection of key-value pairs.

Example:

```json
{
  "country": "Brazil",
  "currency": "BRL",
  "language": "Portuguese"
}
```

Common applications:
- Dynamic attributes.
- Lookup structures.
- Configuration data.
- Key-value collections.

### 3.4 Enumerated Type (Enum)

Represents a predefined set of permitted values.

Example:

```text
PENDING
APPROVED
REJECTED
CANCELLED
```

Common applications:
- Transaction statuses.
- Workflow states.
- Categories.
- Controlled classifications.

### 3.5 UUID / GUID

Represents a universally unique identifier, generally stored as a character representation or binary value depending on the implementation.

Example:

`550e8400-e29b-41d4-a716-446655440000`

Common applications:
- Distributed system identifiers.
- Record identifiers.
- API entities.
- Identifiers generated independently across systems.

### 3.6 JSON

Some systems support JSON as a native or specialized data type, while others store JSON content as text.

Example:

```json
{
  "customer": {
    "id": 101,
    "name": "John"
  }
}
```

JSON is a data interchange format, but JSON-specific database types and implementations may provide specialized functionality for storing, querying, and manipulating JSON content.

### 3.7 XML

XML may be stored as text or supported through specialized XML data types in certain systems.

Example:

```xml
<Customer>
    <ID>101</ID>
    <Name>John</Name>
</Customer>
```

XML is a data representation and interchange format. Specialized XML types may provide validation, querying, and processing features.

### 3.8 Spatial / Geographic Types

Represent geographic or geometric information.

Examples:
- Point.
- Line.
- Polygon.
- MultiPolygon.

Common applications:
- Geographic information systems (GIS).
- Maps.
- Location analysis.
- Spatial relationships.
- Route analysis.

### 3.9 Vector

Represents an ordered collection of numerical values, often used to encode characteristics or dimensions of an object.

Example:

```text
[0.12, 0.85, -0.32, 0.44]
```

Common applications:
- Machine learning.
- Embeddings.
- Similarity search.
- Semantic search.
- AI applications.

Vector support varies across databases, specialized search engines, and analytical platforms.

## 4. Data Type Categories

| Category | Examples | Typical Purpose |
|---|---|---|
| Numeric | Integer, Decimal, Float, Double | Arithmetic and measurements |
| Textual | Char, Varchar, String, Text | Text, codes, descriptions |
| Logical | Boolean | Conditions and flags |
| Temporal | Date, Time, Timestamp | Dates, times, events |
| Binary | Binary, Blob, Byte Array | Files and binary content |
| Identifiers | UUID, GUID | Unique record identification |
| Complex | Array, Struct, Map, Object | Nested and composite values |
| Specialized | JSON, XML, Spatial, Vector, Enum | Specialized data representation and operations |

## 5. Precision, Scale, and Range

### Precision

Precision generally refers to the number of significant digits that a numeric type can represent, although exact definitions vary by implementation and type.

### Scale

For fixed-precision decimal types, scale generally represents the number of digits to the right of the decimal point.

Example:

`DECIMAL(10,2)`

- Precision: 10 total digits.
- Scale: 2 digits after the decimal point.
- Maximum positive value: `99999999.99`.

### Range

Range defines the minimum and maximum values supported by a particular type.

For example, different integer types may support different numeric ranges depending on their storage size and implementation.

## 6. Type Conversion and Casting

Type conversion changes a value from one data type to another.

### Implicit Conversion

A system automatically converts a value or expression to another type according to its conversion rules.

Example:

An integer may be automatically converted to a decimal during an arithmetic operation.

Implicit conversions can introduce unexpected behavior, performance issues, or errors.

### Explicit Conversion

The developer or processing logic specifies the conversion.

Examples:
- String to Integer.
- String to Date.
- Integer to Decimal.
- Timestamp to Date.

Explicit conversion is commonly performed using functions such as `CAST` or `CONVERT` in SQL, or equivalent functions in programming languages and processing frameworks.

### Conversion Risks

- Data truncation.
- Precision loss.
- Invalid values.
- Locale-related differences.
- Date format ambiguity.
- Overflow.
- Unexpected nulls.
- Incompatible schemas.

## 7. Data Type Compatibility

Data types may differ across databases, programming languages, APIs, file formats, and processing engines.

For example, a source system may represent a value as `VARCHAR`, while the destination expects `INTEGER`.

Data pipelines must account for:

- Source and destination type differences.
- Precision and scale compatibility.
- Nullable versus non-nullable fields.
- Timestamp and timezone behavior.
- Schema evolution.
- Conversion rules.
- Validation and error handling.

Type compatibility should be evaluated during data integration and pipeline design.

## 8. Data Types in Data Engineering

Data types play a fundamental role throughout the Data Engineering lifecycle.

| Stage | Data Type Considerations |
|---|---|
| Data Ingestion | Source type identification and initial validation |
| Data Storage | Storage representation, precision, and type support |
| Data Transformation | Casting, conversion, normalization, and calculations |
| Data Quality | Type validation, invalid values, and constraints |
| Data Integration | Source-to-target compatibility |
| Data Modeling | Appropriate types for business attributes |
| Data Consumption | Correct interpretation in analytics and applications |

## 9. Practical Example

Consider a customer dataset:

| Field | Example Value | Suggested Data Type |
|---|---|---|
| Customer ID | 1001 | Integer or UUID |
| Name | John Smith | String |
| Email | john@example.com | String |
| Birth Date | 1985-06-15 | Date |
| Credit Limit | 15000.75 | Decimal |
| Active | TRUE | Boolean |
| Registration Timestamp | 2026-11-25 10:30:00 | Timestamp |

The appropriate data type depends on the business meaning, source system, destination system, expected operations, and data quality requirements.

Identifiers containing leading zeros, such as postal codes, telephone numbers, or certain business codes, are often better represented as strings rather than numeric types because arithmetic operations are not required and formatting may be significant.

## 10. Best Practices

- Select data types based on business meaning and intended use.
- Avoid storing numeric values as text when numeric operations are required.
- Use fixed-precision decimal types when exact decimal arithmetic is necessary.
- Evaluate floating-point precision before using it in calculations.
- Use appropriate date and timestamp types.
- Consider timezone requirements when working with timestamps.
- Avoid unnecessarily large data types.
- Preserve leading zeros when they are meaningful.
- Validate data before conversion.
- Handle nulls explicitly.
- Document source-to-target type mappings.
- Test type compatibility across systems.
- Consider schema evolution and backward compatibility.
- Avoid implicit conversions when they can create ambiguity or performance issues.

## Related Topics

- [Data Concepts](../data-concepts/README.md)
- [Data Formats](../data-formats/README.md)
- [Data Structures](../data-structures/README.md)
- [Metadata and Data Dictionary](../metadata-and-data-dictionary/README.md)
- [Databases](../../03-databases/README.md)
- [SQL](../../04-sql/README.md)

---

# Tipos de Dados

## Visão Geral

Tipos de dados definem a natureza, representação, características e operações permitidas sobre valores armazenados, processados ou intercambiados em um sistema de dados.

Eles ajudam os sistemas a determinar como os dados devem ser interpretados, validados, armazenados, manipulados, comparados e processados.

A escolha adequada dos tipos de dados é importante para a integridade, eficiência de armazenamento, precisão, desempenho, compatibilidade entre sistemas e confiabilidade dos pipelines.

## 1. Por que os Tipos de Dados são Importantes?

Os tipos de dados influenciam:

- Validação e integridade dos dados.
- Requisitos de armazenamento.
- Precisão e exatidão.
- Operações matemáticas e lógicas.
- Comportamento de ordenação e comparação.
- Desempenho de processamento.
- Compatibilidade entre bancos de dados, aplicações, linguagens de programação e formatos de dados.
- Ingestão, transformação e serialização.

A escolha incorreta de tipos de dados pode resultar em truncamento, perda de precisão, erros de conversão, comparações incorretas ou comportamentos inesperados.

## 2. Tipos de Dados Fundamentais

### 2.1 Integer (Inteiro)

Representa números inteiros sem componentes fracionários.

Exemplos:
- `10`
- `-25`
- `0`
- `1000000`

Aplicações comuns:
- Contadores.
- Quantidades.
- Identificadores quando a representação numérica ou operações numéricas são apropriadas.
- Número de registros.
- Quantidade de unidades vendidas.

Os tipos inteiros podem possuir diferentes tamanhos de armazenamento e intervalos de valores, dependendo do sistema.

### 2.2 Decimal / Numeric

Representa números com componentes fracionários e, dependendo da implementação, precisão e escala controladas.

Exemplos:
- `10.50`
- `1500.75`
- `-25.99`

Aplicações comuns:
- Valores financeiros.
- Preços.
- Impostos.
- Medições que exigem precisão decimal.

Tipos decimais de precisão fixa geralmente são preferíveis aos tipos de ponto flutuante binário para cálculos financeiros que exigem representação decimal exata.

### 2.3 Floating-Point (Ponto Flutuante)

Representa números utilizando aritmética de ponto flutuante, geralmente suportando uma ampla faixa de valores com precisão aproximada.

Tipos comuns:
- Float
- Double

Exemplos:
- `3.141592`
- `0.000001`
- `6.02e23`

Aplicações comuns:
- Cálculos científicos.
- Análises estatísticas.
- Medições de engenharia.
- Machine Learning.
- Simulações numéricas.

Valores de ponto flutuante podem introduzir diferenças de arredondamento, pois alguns valores decimais não podem ser representados exatamente em binário.

### 2.4 String / Text (Texto)

Representa dados textuais, sequências de caracteres ou combinações de caracteres.

Exemplos:
- `John Smith`
- `Brazil`
- `customer@example.com`
- `ABC-123`

Aplicações comuns:
- Nomes.
- Endereços.
- Descrições.
- Códigos.
- Fragmentos de JSON.
- Identificadores textuais.

Strings podem possuir tamanho variável ou fixo, dependendo da implementação.

### 2.5 Boolean (Booleano)

Representa um valor lógico com dois estados possíveis, normalmente:

- `TRUE`
- `FALSE`

Aplicações comuns:
- Indicadores ativo/inativo.
- Resultados de validação.
- Indicadores de funcionalidades.
- Condições lógicas.
- Indicadores de status.

Alguns sistemas também suportam Boolean nullable, introduzindo um estado adicional desconhecido ou ausente.

### 2.6 Date (Data)

Representa uma data de calendário sem necessariamente incluir um componente de horário.

Exemplo:

`2026-11-25`

Aplicações comuns:
- Datas de nascimento.
- Datas de emissão de notas.
- Datas de contratos.
- Datas de negócio.
- Datas de vencimento.

### 2.7 Time (Hora)

Representa um horário do dia sem necessariamente incluir uma data de calendário.

Exemplo:

`14:30:45`

Aplicações comuns:
- Horários de funcionamento.
- Agendamentos diários.
- Medições relacionadas ao horário.

Dependendo do sistema, o tipo Time pode incluir frações de segundos ou informações relacionadas a timezone.

### 2.8 DateTime / Timestamp

Representa uma data e hora, geralmente com diferentes níveis de precisão.

Exemplo:

`2026-11-25 14:30:45`

Aplicações comuns:
- Registro de eventos.
- Timestamps de transações.
- Logs de sistemas.
- Horários de execução de processos.
- Rastreamento da ingestão de dados.

Algumas implementações diferenciam timestamps com informação de timezone e timestamps sem informação de timezone.

### 2.9 Binary (Binário)

Representa dados como sequências de bytes, em vez de valores textuais convencionais.

Exemplos:
- `0x48656C6C6F`
- Conteúdo binário de arquivos.

Aplicações comuns:
- Imagens.
- Documentos.
- Conteúdo de arquivos codificados.
- Byte arrays.
- Payloads de dados brutos.

Dados binários podem ser armazenados diretamente em bancos de dados ou externamente em object storage, mantendo-se uma referência no banco de dados.

### 2.10 Null / Missing Value (Valor Ausente)

Representa a ausência de um valor, um valor desconhecido ou indisponível, dependendo do sistema e do contexto.

`NULL` não é equivalente a:
- `0`
- String vazia (`''`)
- `FALSE`
- Um valor textual literal como `'NULL'`

O tratamento de null é importante em SQL, transformações de dados, validações, agregações e regras de qualidade.

## 3. Tipos de Dados Especializados e Complexos

### 3.1 Array

Representa uma coleção ordenada de valores.

Exemplo:

```json
[10, 20, 30, 40]
```

Arrays podem conter elementos do mesmo tipo ou, dependendo da implementação, diferentes tipos.

Aplicações comuns:
- Listas de medições.
- Coleções de identificadores.
- Atributos repetidos.
- Estruturas de dados aninhadas.

### 3.2 Object / Struct

Representa uma coleção de propriedades ou campos nomeados, potencialmente com diferentes tipos de dados.

Exemplo:

```json
{
  "id": 101,
  "name": "John",
  "active": true
}
```

Aplicações comuns:
- Registros aninhados.
- Payloads de APIs.
- Dados JSON.
- Schemas complexos.

### 3.3 Map / Dictionary (Mapa / Dicionário)

Representa uma coleção de pares chave-valor.

Exemplo:

```json
{
  "country": "Brazil",
  "currency": "BRL",
  "language": "Portuguese"
}
```

Aplicações comuns:
- Atributos dinâmicos.
- Estruturas de lookup.
- Dados de configuração.
- Coleções chave-valor.

### 3.4 Enumerated Type (Enum)

Representa um conjunto predefinido de valores permitidos.

Exemplo:

```text
PENDING
APPROVED
REJECTED
CANCELLED
```

Aplicações comuns:
- Status de transações.
- Estados de workflows.
- Categorias.
- Classificações controladas.

### 3.5 UUID / GUID

Representa um identificador universalmente único, geralmente armazenado como representação textual ou valor binário, dependendo da implementação.

Exemplo:

`550e8400-e29b-41d4-a716-446655440000`

Aplicações comuns:
- Identificadores de sistemas distribuídos.
- Identificadores de registros.
- Entidades de APIs.
- Identificadores gerados independentemente entre sistemas.

### 3.6 JSON

Alguns sistemas suportam JSON como tipo nativo ou especializado, enquanto outros armazenam o conteúdo JSON como texto.

Exemplo:

```json
{
  "customer": {
    "id": 101,
    "name": "John"
  }
}
```

JSON é um formato de intercâmbio de dados, mas tipos e implementações específicas de JSON em bancos de dados podem oferecer funcionalidades especializadas de armazenamento, consulta e manipulação de seu conteúdo.

### 3.7 XML

XML pode ser armazenado como texto ou suportado por tipos especializados em determinados sistemas.

Exemplo:

```xml
<Customer>
    <ID>101</ID>
    <Name>John</Name>
</Customer>
```

XML é um formato de representação e intercâmbio de dados. Tipos XML especializados podem oferecer recursos de validação, consulta e processamento.

### 3.8 Spatial / Geographic (Espacial / Geográfico)

Representa informações geográficas ou geométricas.

Exemplos:
- Point.
- Line.
- Polygon.
- MultiPolygon.

Aplicações comuns:
- Sistemas de Informação Geográfica (GIS).
- Mapas.
- Análise de localização.
- Relações espaciais.
- Análise de rotas.

### 3.9 Vector (Vetor)

Representa uma coleção ordenada de valores numéricos, frequentemente utilizada para codificar características ou dimensões de um objeto.

Exemplo:

```text
[0.12, 0.85, -0.32, 0.44]
```

Aplicações comuns:
- Machine Learning.
- Embeddings.
- Busca por similaridade.
- Busca semântica.
- Aplicações de Inteligência Artificial.

O suporte a vetores varia entre bancos de dados, mecanismos de busca especializados e plataformas analíticas.

## 4. Categorias de Tipos de Dados

| Categoria | Exemplos | Finalidade Típica |
|---|---|---|
| Numéricos | Integer, Decimal, Float, Double | Cálculos e medições |
| Textuais | Char, Varchar, String, Text | Textos, códigos e descrições |
| Lógicos | Boolean | Condições e indicadores |
| Temporais | Date, Time, Timestamp | Datas, horários e eventos |
| Binários | Binary, Blob, Byte Array | Arquivos e conteúdos binários |
| Identificadores | UUID, GUID | Identificação única de registros |
| Complexos | Array, Struct, Map, Object | Valores compostos e aninhados |
| Especializados | JSON, XML, Spatial, Vector, Enum | Representações e operações especializadas |

## 5. Precisão, Escala e Intervalo

### Precision (Precisão)

Precision geralmente se refere ao número de dígitos significativos que um tipo numérico pode representar, embora definições exatas variem de acordo com a implementação e o tipo.

### Scale (Escala)

Em tipos decimais de precisão fixa, scale geralmente representa o número de dígitos à direita do separador decimal.

Exemplo:

`DECIMAL(10,2)`

- Precisão: 10 dígitos no total.
- Escala: 2 dígitos após o separador decimal.
- Valor positivo máximo: `99999999.99`.

### Range (Intervalo)

Range define os valores mínimos e máximos suportados por um determinado tipo.

Por exemplo, diferentes tipos inteiros podem suportar intervalos numéricos diferentes, dependendo de seu tamanho de armazenamento e implementação.

## 6. Conversão e Casting

A conversão de tipos altera um valor de um tipo de dado para outro.

### Implicit Conversion (Conversão Implícita)

O sistema converte automaticamente um valor ou expressão para outro tipo de acordo com suas regras de conversão.

Exemplo:

Um inteiro pode ser convertido automaticamente para decimal durante uma operação aritmética.

Conversões implícitas podem introduzir comportamentos inesperados, problemas de desempenho ou erros.

### Explicit Conversion (Conversão Explícita)

O desenvolvedor ou a lógica de processamento especifica a conversão.

Exemplos:
- String para Integer.
- String para Date.
- Integer para Decimal.
- Timestamp para Date.

Conversões explícitas são comumente realizadas por funções como `CAST` ou `CONVERT` em SQL, ou funções equivalentes em linguagens de programação e frameworks de processamento.

### Riscos de Conversão

- Truncamento de dados.
- Perda de precisão.
- Valores inválidos.
- Diferenças relacionadas a locale.
- Ambiguidade em formatos de data.
- Overflow.
- Nulls inesperados.
- Schemas incompatíveis.

## 7. Compatibilidade entre Tipos de Dados

Os tipos de dados podem diferir entre bancos de dados, linguagens de programação, APIs, formatos de arquivos e engines de processamento.

Por exemplo, um sistema de origem pode representar um valor como `VARCHAR`, enquanto o destino espera `INTEGER`.

Pipelines de dados precisam considerar:

- Diferenças entre tipos de origem e destino.
- Compatibilidade de precisão e escala.
- Campos nullable e non-nullable.
- Comportamento de timestamps e timezones.
- Evolução de schemas.
- Regras de conversão.
- Validação e tratamento de erros.

A compatibilidade entre tipos deve ser avaliada durante o desenho da integração de dados e dos pipelines.

## 8. Tipos de Dados na Engenharia de Dados

Os tipos de dados possuem papel fundamental ao longo do ciclo de vida da Engenharia de Dados.

| Etapa | Considerações sobre Tipos de Dados |
|---|---|
| Data Ingestion | Identificação dos tipos de origem e validação inicial |
| Data Storage | Representação de armazenamento, precisão e suporte aos tipos |
| Data Transformation | Casting, conversão, normalização e cálculos |
| Data Quality | Validação de tipos, valores inválidos e constraints |
| Data Integration | Compatibilidade entre origem e destino |
| Data Modeling | Tipos adequados para atributos de negócio |
| Data Consumption | Interpretação correta em analytics e aplicações |

## 9. Exemplo Prático

Considere um dataset de clientes:

| Field | Example Value | Suggested Data Type |
|---|---|---|
| Customer ID | 1001 | Integer or UUID |
| Name | John Smith | String |
| Email | john@example.com | String |
| Birth Date | 1985-06-15 | Date |
| Credit Limit | 15000.75 | Decimal |
| Active | TRUE | Boolean |
| Registration Timestamp | 2026-11-25 10:30:00 | Timestamp |

O tipo de dado adequado depende do significado de negócio, sistema de origem, sistema de destino, operações esperadas e requisitos de qualidade dos dados.

Identificadores que possuem zeros à esquerda, como CEPs, telefones ou determinados códigos empresariais, geralmente são mais adequadamente representados como strings do que como tipos numéricos, pois não exigem operações aritméticas e sua formatação pode ser significativa.

## 10. Boas Práticas

- Selecionar tipos de dados com base no significado de negócio e na finalidade de utilização.
- Evitar armazenar valores numéricos como texto quando operações numéricas forem necessárias.
- Utilizar tipos decimais de precisão fixa quando cálculos decimais exatos forem necessários.
- Avaliar a precisão de ponto flutuante antes de utilizá-lo em cálculos.
- Utilizar tipos adequados de Date e Timestamp.
- Considerar requisitos de timezone ao trabalhar com timestamps.
- Evitar tipos de dados desnecessariamente grandes.
- Preservar zeros à esquerda quando forem significativos.
- Validar os dados antes das conversões.
- Tratar nulls explicitamente.
- Documentar mapeamentos de tipos entre origem e destino.
- Testar compatibilidade entre sistemas.
- Considerar evolução de schemas e compatibilidade retroativa.
- Evitar conversões implícitas quando puderem gerar ambiguidades ou problemas de desempenho.

## Tópicos Relacionados

- [Conceitos de Dados](../data-concepts/README.md)
- [Formatos de Dados](../data-formats/README.md)
- [Estruturas de Dados](../data-structures/README.md)
- [Metadados e Dicionário de Dados](../metadata-and-data-dictionary/README.md)
- [Bancos de Dados](../../03-databases/README.md)
- [SQL](../../04-sql/README.md)
