# Lojas

## Stores \| Loja

Lojas

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :---: | ---: | ---: | ---: |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **cnpj\*** | **CNPJ da loja** | **string** | **Deve ser um CNPJ válido com 14 caracteres** | **“05345647000122”** |

\*Campos obrigatórios

### Exemplo de consulta em SQL:

```text
          SELECT id AS "id", 
          cnpj      AS "cnpj" 
          FROM   view_stores
```

