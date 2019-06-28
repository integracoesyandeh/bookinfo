---
description: Títulos da Fatura
---

# Notas fiscais do Pedido - Títulos da Fatura

#### Essa entidade deve ser enviada se caso o ERP possuir empresas do segmento de _Material de Construção._

Modelo de Dados - ORDER-INVOICES

<table>
  <thead>
    <tr>
      <th style="text-align:left">Campo</th>
      <th style="text-align:center">Descri&#xE7;&#xE3;o</th>
      <th style="text-align:right">Tipo</th>
      <th style="text-align:right">Restri&#xE7;&#xF5;es</th>
      <th style="text-align:right">Exemplo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>store_id*</b>
      </td>
      <td style="text-align:center"><b>Identificador interno da loja</b>
      </td>
      <td style="text-align:right"><b>integer ou string</b>
      </td>
      <td style="text-align:right"><b>--</b>
      </td>
      <td style="text-align:right"><b>1</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>order_id*</b>
      </td>
      <td style="text-align:center"><b>Identificador &#xFA;nico do Pedido</b>
      </td>
      <td style="text-align:right"><b>string</b>
      </td>
      <td style="text-align:right"><b>tamanho m&#xE1;ximo de 50 caracteres</b>
      </td>
      <td style="text-align:right"><b>&quot;ABC1233233&quot;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>number*</b>
      </td>
      <td style="text-align:center"><b>N&#xFA;mero da nota fiscal</b>
      </td>
      <td style="text-align:right"><b>string</b>
      </td>
      <td style="text-align:right"><b>tamanho m&#xE1;ximo de 50 caracteres</b>
      </td>
      <td style="text-align:right"><b>&quot;NFE-0001&quot;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">total_amount</td>
      <td style="text-align:center">Valor total do t&#xED;tulo</td>
      <td style="text-align:right">float</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">890.9000</td>
    </tr>
    <tr>
      <td style="text-align:left">due_date</td>
      <td style="text-align:center">Data de vencimento</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">satisfazer o padr&#xE3;o &#x200B; &#x201C;YYYY-MM-DD&#x201D;</td>
      <td style="text-align:right">&quot;2017-08-20&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:center">Status do t&#xED;tulo</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">
        <p>limita-se a apenas um dos seguintes valores:</p>
        <p>&#x25CF; &#x201C;pending&#x201D;</p>
        <p>&#x25CF; &#x201C;complete&#x201D;</p>
        <p>&#x25CF; &#x201C;canceled&#x201D;</p>
        <p>&#x25CF; &#x201C;expired&#x201D;</p>
      </td>
      <td style="text-align:right">--</td>
    </tr>
    <tr>
      <td style="text-align:left">url</td>
      <td style="text-align:center">URL para download do t&#xED;tulo em PDF</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 255 caracteres</td>
      <td style="text-align:right">--</td>
    </tr>
  </tbody>
</table>### Exemplo de consulta em SQL:

```text
SELECT order_id     AS "order_id", 
       store_id     AS "store_id", 
       dt_order     AS "dt_order", 
       status       AS "status", 
       due_date     AS "due_date", 
       url          AS "url", 
       number       AS "number", 
       total_amount AS "total_amount" 
FROM   view_order_invoice_invoices 
```

