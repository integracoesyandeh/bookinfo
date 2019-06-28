---
description: Modelo de Dados - "Sellout-Items" | Vendas aos Clientes (Itens)
---

# Vendas - Itens

**Itens do Sellout**

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **id\*** | **Identificador da venda** | **string** | **tamanho máximo de 50 caracteres** | **“RCNTH345987”** |
| **sellout\_timestamp\*** | **Data e hora da venda** | **string** | **satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”** | **“2017-08-20T14:55:08”** |
| **sku\*** | **Código do produto no ERP. Pode ser o código interno ou EAN** | **string** | **tamanho máximo de 50 caracteres** | **"1877563549875"** |
| code | Código interno do produto | string | tamanho máximo de 30 caracteres | “3789” |
| isbn | ISBN | string | tamanho mínimo de 10 e máximo de 13 caracteres | “9783161484100” |
| **description\*** | **Descrição do produto ou serviço** | **string** | **tamanho máximo de 100 caracteres** | **“CASTANHA DO PARÁ INTEIRA”** |
| **cancellation\_flag\*** | **Indica se este item foi cancelado** | **string** | **limita-se apenas aos valores: “S”: item cancelado “N”: item não cancelado** | **"N"** |
| **item\_addition\*** | **Valor de acréscimo do item** | **float** | **--** | **4.9800** |
| frete | Valor de frete do item | float | -- | 25.9800 |
| cfop | Código Fiscal de Operações e Prestações | integer | -- | 1103 |
| **item\_discount\*** | **Valor de desconto do item** | **float** | **--** | **4.9800** |
| ipi | Valor do IPI sobre o item | float | -- | 1.8700 |
| icms | Valor do ICMS | float | -- | 2.5000 |
| item\_icms\_st | Valor do ICMS ST sobre o item | float | -- | 2.5000 |
| pis | Valor do PIS sobre o item | float | -- | 1.5000 |
| cofins | Valor do COFINS sobre o item | float | -- | 1.5000 |
| **measurement\_unit\*** | **Unidade de medida** | **string** | **--** | **"KG"** |
| **unit\_value\*** | **Valor unitário do produto. Este valor deve vir com 4 casas decimais** | **float** | **--** | **4.9888** |
| **quantity\*** | **Quantidade comprada do produto** | **float** | **--** | **1.0000** |
| manufacturer\_code | Código do fabricante | string | -- | 8928329 |

## Exemplo de consulta em SQL:

```text
SELECT store_id          AS "store_id", 
       id                AS "id", 
       sellout_timestamp AS "sellout_timestamp",
       sku               AS "sku", 
       code              AS "code", 
       isbn              AS "isbn", 
       description       AS "description", 
       cancellation_flag AS "cancellation_flag", 
       item_addition     AS "item_addition", 
       frete             AS "frete", 
       cfop              AS "cfop", 
       item_discount     AS "item_discount", 
       ipi               AS "ipi", 
       icms              AS "icms",
       item_icms_st      AS "icms_st",
       pis               AS "pis", 
       cofins            AS "cofins", 
       measurement_unit  AS "measurement_unit", 
       unit_value        AS "unit_value", 
       quantity          AS "quantity" 
       manufacturer_code AS "manufacturer_code"
FROM   view_sellout_items
```

