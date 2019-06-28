---
description: Nota Fiscal - Cabeçalho
---

# \*Notas fiscais - Pedido de Venda

#### \*Essa entidade deve ser enviada se caso o ERP possuir empresas do segmento de _Material de Construção._

Modelo de Dados - ORDER-INVOICE

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :---: | ---: | ---: | ---: |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **order\_id\*** | **Identificador único do Pedido** | **string** | **tamanho máximo de 50 caracteres** | **"ABC1233233"** |
| **number\*** | **Número da nota fiscal** | **string** | **tamanho máximo de 50 caracteres** | **"NFE-0001"** |
| **access\_key\*** | **Chave de acesso para consulta da nota fiscal eletrônica** | **string** | **tamanho máximo de 44 caracteres** | **"51080701212344000127550010000000981364112281"** |
| total\_amount | Valor total da nota fiscal | float | -- | 119.8700 |
| **series\*** | **Número de serie da nota fiscal** | **string** | **tamanho máximo de 30 caracteres** | **"003"** |
| created\_at | Data de emissão | string | satisfazer a expressão regular “\d{4}-\d{1,2}-\d{1,2}\s\(\d{2}:\){2}\d{2}” |  |
| url | URL do arquivo XML da invoice | string | -- | -- |
| discount\_amount | Valor total do desconto da nota fiscal | float | -- | 24.9000 |

### Exemplo de consulta em SQL:

```text
SELECT order_id        AS "order_id", 
       number          AS "number", 
       store_id        AS "store_id", 
       dt_order        AS "dt_order", 
       access_key      AS "access_key", 
       total_amount    AS "total_amount", 
       series          AS "series", 
       created_at      AS "created_at", 
       url             AS "url", 
       discount_amount AS "discount_amount" 
FROM   view_order_invoice 
```

