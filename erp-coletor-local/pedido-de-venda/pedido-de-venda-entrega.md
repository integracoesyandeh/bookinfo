---
description: Entrega
---

# Pedido de venda - Entrega

#### Essa entidade deve ser enviada se caso o ERP possuir empresas do segmento de _Material de Construção._

Modelo de Dados - SHIPPING

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :---: | ---: | ---: | ---: |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **order\_id\*** | **Identificador único do Pedido** | **string** | **tamanho máximo de 50 caracteres** | **"ABC1233233"** |
| carrier | Nome da transportadora escolhida | string | -- | "Correios" |
| shipping\_method | Forma de entrega escolhida | string | -- | "Sedex 10" |

### Exemplo de consulta em SQL:

```text
SELECT store_id        AS "store_id", 
       order_id        AS "order_id", 
       carrier         AS "carrier", 
       shipping_method AS "shipping_method" 
FROM   view_order_shipping
```

