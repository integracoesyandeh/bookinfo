---
description: >-
  Modelo de Dados - CATEGORIES | Árvore de categorias do produto, ordenada da
  categoria mais geral para a mais restrita
---

# Produtos - Categorias

## Categorias do Produto

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **code\*** | **Código interno do produto** | **string** | **tamanho máximo de 50 caracteres** | **"3789"** |
| **cetegory\*** | **Categoria do produto** | **string** | **--** | **"Bebidas"** |

\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id AS "store_id", 
       code     AS "code", 
       category AS "category" 
FROM   view_product_categories
```

