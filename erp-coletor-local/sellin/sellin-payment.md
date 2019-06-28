---
description: >-
  Modelo de Dados - "Sellin-Payment" | Compras de Fornecedor (Forma de
  Pagamento)
---

# Compras - Formas de Pagamentos

## Forma de Pagamento     <a id="forma-de-pagamento"></a>

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **–** | **1** |
| **sellin\_timestamp\*** | **Data e hora da compra** | **string** | **satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”** | **“2017-08-20T14:55:08”** |
| **id\*** | **Identificador \(NF\) da compra** | **string** | **tamanho máximo de 50 caracteres** | **“RCNTH345987”** |
| **payment\_method\_id\*** | **Identificador da Forma de Pagamento** | **string** | **–** | **–** |
| **method\*** | **Método de Pagamento** | **string** | **–** | **“Boleto”** |
| bin | BIN \[6 Primeiros dígitos do cartão\] | string | – | – |
| ccflag\_id | Código da bandeira do cartão | string | tamanho máximo de 50 caracteres | “19389238” |
| **condition\*** | **Condição de pagamento** | **string** | **–** | **“Parcelado”** |
| operation\_id | Código da operação financeira | string | – | “92389328” |
| nsu | NSU | string | – | – |
| authorization | Autorização da transação | string | – | – |

\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id         AS "store_id", 
       sellin_timestamp AS "sellin_timestamp", 
       id               AS "id",
       payment_method_id AS "payment_id",
       method           AS "method", 
       bin              AS "bin", 
       ccflag_id        AS "ccflag_id", 
       condition        AS "condition", 
       operation_id     AS "operation_id", 
       nsu              AS "nsu", 
       AUTHORIZATION    AS "authorization" 
FROM   view_sellin_payment
```

