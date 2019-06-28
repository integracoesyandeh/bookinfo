---
description: >-
  Modelo de Dados - RELATED-PRODUCTS | Códigos dos produtos relacionados ao
  respectivo produto da entidade - [Products]
---

# Produtos - Produtos Relacionados

## Produtos Relacionados

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **code\*** | **Código interno do produto** | **string** | **tamanho máximo de 50 caracteres** | **"3789"** |
| **internal\_code** | **Código interno do produto no ERP** | **string** | **--** | **"93287"** |
| **sku** | **Código de barras \(EAN 13 ou DUN14\) dos produtos relacionados ao respectivo produto da entidade \[Products\]** | **string** | **tamanho máximo de 20 caracteres** | **"11402329312324"** |

\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id      AS "store_id", 
       code          AS "code", 
       internal_code AS "sku", 
       sku           AS "sku" 
FROM   view_product_related_products
```

