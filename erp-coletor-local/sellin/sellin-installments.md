---
description: >-
  Modelo de Dados - "Sellin - Installments" |  Compras de Fornecedor (Condição
  de Pagamento)
---

# Compras - Condições de Pagamentos

## Condição de Pagamento     <a id="forma-de-pagamento"></a>

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **–** | **1** |
| **sellin\_timestamp\*** | **Data e hora da compra** | **string** | **satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”** | **“2017-08-20T14:55:08”** |
| **id\*** | **Identificador \(NF\) da compra** | **string** | **tamanho máximo de 50 caracteres** | **“RCNTH345987”** |
| **payment\_method\_id\*** | **Identificador da Forma de Pagamento** | **string** | **–** | **–** |
| **installment\_number\*** | **Número da parcela** | **string** | **--** | **1** |
| **amount\*** | **Valor da parcela** | **float** | **Este valor deve ser enviado com 4 casas. decimais** | **129.9000** |
| **payment\_term\*** | **Prazo do pagamento da parcela em dias** | **integer** | **–** | **30** |

\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
 SELECT store_id          AS "store_id", 
       sellin_timestamp   AS "sellin_timestamp", 
       id                 AS "id", 
       payment_method_id  AS "payment_id", 
       installment_number AS "installment_number", 
       amount             AS "amount", 
       payment_term       AS "payment_term" 
FROM   view_sellin_payment_installments
```

