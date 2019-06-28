---
description: >-
  Modelo de Dados - "Sellout- Installments" |  Vendas aos Clientes (Condição de
  Pagamento)
---

# Vendas - Condições de Pagamentos

## Condição de Pagamento     <a id="forma-de-pagamento"></a>

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :---: | :--- | :--- | :--- | :--- |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **–** | **1** |
| **sellout\_timestamp\*** | **Data e hora da venda** | **string** | **satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”** | **“2017-08-20T14:55:08”** |
| **id\*** | **Identificador \(NF\) da venda** | **string** | **tamanho máximo de 50 caracteres** | **“RCNTH345987”** |
| **installment\_number** | **Número da parcela** | **string** | **--** | **1** |
| **payment\_method\_id\*** | **Identificador da Forma de Pagamento** | **string** | **–** | **–** |
| **amount\*** | **Valor da parcela** | **float** | **–** | **129.9000** |
| **payment\_term\*** | **Prazo do pagamento da parcela em dias** | **integer** | **–** | **30** |

### Exemplo da consulta em SQL:

```text
     SELECT store_id           AS "store_id", 
           sellout_timestamp  AS "sellout_timestamp", 
           id                 AS "id", 
           payment_id         AS "payment_id", 
           installment_number AS "installment_number", 
           amount             AS "amount", 
           payment_term       AS "payment_term" 
    FROM   view_sellout_payment_installments
```

