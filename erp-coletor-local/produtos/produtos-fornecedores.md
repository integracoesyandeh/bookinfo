---
description: "Modelo de Dados - SUPPLIERS\t| Fornecedores do respectivo produto do registro de entidade - [Products]"
---

# Produtos - Fornecedores

## Fornecedores

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **code\*** | **Código interno do produto** | **string** | **tamanho máximo de 50 caracteres** | **"3789"** |
| **supplier\*** | **Código do Fornecedor** | **string** | **--** | **"72086766000141"** |

\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id AS "store_id", 
       code     AS "code", 
       supplier AS "supplier" 
FROM   view_product_suppliers
```



