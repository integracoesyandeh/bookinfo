---
description: Itens da Fatura
---

# Notas fiscais do Pedido - Itens da Fatura

#### Essa entidade deve ser enviada se caso o ERP possuir empresas do segmento de _Material de Construção._

Modelo de Dados - INVOICE-ITEMS



| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :---: | ---: | ---: | ---: |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **order\_id\*** | **Identificador único do Pedido** | **string** | **tamanho máximo de 50 caracteres** | **"ABC1233233"** |
| ean | EAN do produto conforme nota fiscal | string | -- | "9832984320374" |
| name | Nome do produto conforme nota fiscal | string | -- | "Repolho Kg Verde" |
| price | Valor do produto conforme nota fiscal | float | -- | 6.3400 |
| qty | Quantidade do produto conforme nota fiscal | string | -- | "8.0" |
| unit | Unidade do produto conforme nota fiscal | string | -- | "KG" |

### Exemplo de consulta em SQL:

```text
SELECT order_id AS "order_id", 
       store_id AS "store_id", 
       dt_order AS "dt_order", 
       price    AS "price", 
       qty      AS "qty", 
       name     AS "name", 
       unit     AS "unit", 
       ean      AS "ean" 
FROM   view_order_invoice_items 
```

