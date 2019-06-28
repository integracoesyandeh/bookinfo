# Pedidos de Venda - Itens

#### Essa entidade deve ser enviada se caso o ERP possuir empresas do segmento de _Material de Construção._

Modelo de Dados - ORDER-ITEMS

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :---: | ---: | ---: | ---: |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **order\_id\*** | **Identificador único do Pedido** | **string** | **tamanho máximo de 50 caracteres** | **“ABC1233233”** |
| **sku\*** | **Código de barras do produto \(EAN-13 ou DUN-14\) quando houver** | **string** | **tamanho máximo de 50 caracteres** | **“7898918709930”** |
| **code​\*** | **Código interno do produto** | **string** | **tamanho máximo de 50 caracteres** | **“3789”** |
| description | Nome ou descrição do produto | string | tamanho máximo de 30 caracteres | “Castanha do Pará” |
| quantity | Quantidade do produto formatado com 4 casas decimais | float | -- | 1.0000 |
| unit\_value | Valor unitário do produto | float | -- | 23.9999 |
| item\_addition | Valor de acréscimo sobre o item | float | formatado com 4 casas decimais | 3.4999 |
| item\_discount | Valor de desconto sobre o item | float | formatado com 4 casas decimais | 3.49999 |

### Exemplo de consulta em SQL:

```text
SELECT store_id      AS "store_id", 
       order_id      AS "order_id", 
       code          AS "code", 
       sku           AS "sku", 
       description   AS "description", 
       item_addition AS "item_addition", 
       item_discount AS "item_discount", 
       unit_value    AS "unit_value", 
       quantity      AS "quantity" 
FROM   view_order_items 
```

