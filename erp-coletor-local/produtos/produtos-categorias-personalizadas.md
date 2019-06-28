---
description: >-
  Modelo de Dados - CATEGORIAS PERSONALIZADAS | Categorias personalizadas para
  respectivos produtos
---

# Produtos - Categorias Personalizadas

## Categorias Personalizadas

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **code\*** | **Código interno do produto** | **string** | **tamanho máximo de 50 caracteres** | **"3789"** |
| attibute\_code | Código atribuído personalizado | string | -- | "code" |
| value | Valor atribuído personalizado | string | -- | "9328757" |

\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id       AS "store_id", 
       code           AS "code", 
       attribute_code AS "attribute_code", 
       value          AS "value" 
FROM   view_product_custom_attributes
```

