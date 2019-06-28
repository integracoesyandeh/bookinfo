---
description: Modelo de Dados - "Sellin-Items" | Compras de Fornecedor (Itens)
---

# Compras - Itens

## Compras de Fornecedor - Itens     <a id="sellin---itens"></a>

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **–** | **1** |
| **sellin\_timestamp\*** | **Data e hora da compra** | **string** | **satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”** | **“2017-08-20T14:55:08”** |
| **id\*** | **Identificador \(NF\) da compra** | **string** | **tamanho máximo de 50 caracteres** | **“RCNTH345987”** |
| **code\*** | **Código interno do produto vendido** | **string** | **tamanho máximo de 30 caracteres** | **“COCA300”** |
| isbn | ISBN | string | Tamanho mínimo de 10 caracteres e máximo de 13 caracteres | – |
| **description\*** | **Descrição do produto** | **string** | **tamanho máximo de 50 caracteres** | **“Castanha portuguesa”** |
| **ean\*** | **Código de barras do produto, se houver. Este campo aceita tanto EAN-13 quanto DUN-14** | **string** | **tamanho máximo de 14 caracteres** | **“7891149201006”** |
| **addition\*** | **Valor de acréscimo total neste item** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **34.5698** |
| **discount\*** | **Valor de desconto total neste item** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **34.5698** |
| **net\_total\*** | **Valor total das unidades vendidas, sem impostos e frete** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **56.9805** |
| measurement\_unit | Unidade de medida | string | – | “UN” |
| **gross\_total\*** | **Valor total das unidades vendidas, sem desconto ou acréscimo** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **56.9800** |
| **unit\_value\*** | **Valor unitário do produto, sem desconto ou acréscimo** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **45.9800** |
| **quantity\*** | **Quantidade do produto** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **1.0000** |
| manufacturer\_code | Código do fabricante | string | – | 8928329 |
| **icms\*** | **Valor do ICMS ST do item** | **float** | **Este valor deve ser enviado com 4 casas decimais** | **2.9000** |

\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id         AS "store_id", 
       sellin_timestamp AS "sellin_timestamp", 
       id               AS "id", 
       code             AS "code", 
       isbn             AS "isbn", 
       description      AS "description", 
       ean              AS "ean", 
       addition         AS "addition", 
       discount         AS "discount", 
       net_total        AS "net_total", 
       measurement_unit AS "measurement_unit", 
       gross_total      AS "gross_total", 
       unit_value       AS "unit_value", 
       quantity         AS "quantity"
       manufacturer_code AS "manufacturer_code"   
FROM   view_sellin_items
```

