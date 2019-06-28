---
description: Forma de Pagamento
---

# Pedido de venda - Forma de Pagamento

#### Essa entidade deve ser enviada se caso o ERP possuir empresas do segmento de _Material de Construção._

Modelo de Dados - ORDER-PAYMENT

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :---: | ---: | ---: | ---: |
| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| **order\_id\*** | **Identificador único do Pedido** | **string** | **tamanho máximo de 50 caracteres** | **"ABC1233233"** |
| payment\_method | Método de pagamento escolhido pelo cliente | string | -- | "Boleto Bancário" |
| payment\_plan | Condição de pagamento escolhida pelo cliente | string | -- | "À vista" |
| payment\_amount | Valor do pagamento | float | -- | 49.9999 |

### Exemplo de consulta em SQL:

```text
SELECT store_id       AS "store_id", 
       order_id       AS "order_id", 
       payment_method AS "payment_method", 
       payment_plan   AS "payment_plan", 
       payment_amount AS "payment_amount" 
FROM   view_order_payment
```

