# Compras

### description: Modelo de Dados - Sellin \| Compras de Fornecedor

## Compras

### SellIn - Cabeçalho      <a id="sellin---cabe&#xE7;alho"></a>

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id**\* | **Identificador interno da loja** | **integer ou string** | **–** | **1** |
| **id**\* | **Identificador \(NF\) da compra** | **string** | **tamanho máximo de 50 caracteres** | **“RCNTH345987”** |
| **supplier\_taxpayer\_id\*** | **CNPJ do Fornecedor** | **string** | **tamanho máximo de 14 caracteres** | **“14463765000172”** |
| **sellin\_timestamp\*** | **Data e hora da compra** | **string** | **satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”** | **“2017-08-20T14:55:08”** |
| **nfe\_access\_key\*** | **Chave de acesso para NFe/SAT** | **string** | **tamanho máximo de 50 caracteres** | **“NFe31170901704848000164550020000018481058491134”** |
| other\_expenses | Outras despesas | float | Este valor deve ser enviado com 4 casas decimais | 1.9900 |
| seller\_id | CPF do vendedor associado a esta NF, caso exista vendedor relacionado | string | tamanho máximo de 11 caracteres | “RCNTH345987” |
| ipi | Valor do IPI sobre a compra | float | Este valor deve ser enviado com 4 casas decimais | 1.8700 |
| iss | Valor do ISS sobre a compra | float | Este valor deve ser enviado com 4 casas decimais | 1.0100 |
| **sales\_discount\*** | **Valor de desconto na compra** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **5.9900** |
| insurance\_price | Valor do seguro | float | Este valor deve ser enviado com 4 casas decimais | 2.0000 |
| **gross\_total\*** | **Valor total da NF. Este valor deve vir com 4 casas decimais** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **5.9900** |
| **cancellation\_flag\*** | **Indica se esta compra foi cancelada ou não** | **string** | **Valores aceitos: “S” — para sim e “N” — para não** | **“S”** |
| **nfe\_series\_number\*** | **Número de Série da Nota Fiscal** | **integer** | – | **1** |
| **nfe\_number\*** | **Número da Nota Fiscal** | **integer** | – | **1267232** |
| **sales\_addition\*** | **Valor de acréscimo na compra** | **float** | **Este valor deve vir com 4 casas decimais** | **4.5500** |
| **store\_taxpayer\_id\*** | **CNPJ da loja** | **string** | **tamanho máximo de 14 caracteres** | **“14463765000100”** |
| **net\_total\*** | **Valor total da NF sem impostos e frete** | **float** | **Este valor deve vir com 4 casas decimais** | **4.9999** |
| freight\_price | Valor do frete | float | Este valor deve ser enviado com 4 casas decimais | 1.0000 |
| **icms\*** | **Valor do ICMS sobre a compra** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **2.9000** |

#### Exemplo da consulta em SQL:

```text
SELECT store_id             AS "store_id", 
       nfe_access_key       AS "nfe_access_key", 
       other_expenses       AS "other_expenses", 
       seller_id            AS "seller_id", 
       ipi                  AS "ipi", 
       iss                  AS "iss", 
       sales_discount       AS "sales_discount", 
       insurance_price      AS "insurance_price", 
       gross_total          AS "gross_total", 
       cancellation_flag    AS "cancellation_flag", 
       nfe_series_number    AS "nfe_series_number", 
       nfe_number           AS "nfe_number", 
       sales_addition       AS "sales_addition", 
       store_taxpayer_id    AS "store_taxpayer_id", 
       net_total            AS "net_total", 
       freight_price        AS "freight_price", 
       supplier_taxpayer_id AS "supplier_taxpayer_id", 
       icms                 AS "icms", 
       sellin_timestamp     AS "sellin_timestamp", 
       id                   AS "id" 
FROM   view_sellin
```

