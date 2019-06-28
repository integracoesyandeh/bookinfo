---
description: Modelo de Dados - "Daily_SellIn_Total" | Valor total de compra por dia
---

# Compras - Total Diário

Modelo de Dados - "Daily\_SellIn\_Total" \| Valor total de compra por dia.

_Essa entidade não é obrigatória para o Escopo Reduzido \(MVP1\)._

## Compra total por dia

<table>
  <thead>
    <tr>
      <th style="text-align:left">Campo</th>
      <th style="text-align:left">Descri&#xE7;&#xE3;o</th>
      <th style="text-align:left">Tipo</th>
      <th style="text-align:left">Restri&#xE7;&#xF5;es</th>
      <th style="text-align:left">Exemplo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>store_id*</b>
      </td>
      <td style="text-align:left"><b>Identificador interno da loja</b>
      </td>
      <td style="text-align:left"><b>integer ou string</b>
      </td>
      <td style="text-align:left"><b>--</b>
      </td>
      <td style="text-align:left"><b>1</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>date*</b>
      </td>
      <td style="text-align:left"><b>Data do dia</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>satisfazer o padr&#xE3;o &#x201C;YYYY-MM-DD&#x201D;</b>
      </td>
      <td style="text-align:left"><b>&#x201C;2018-08-13&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>type*</b>
      </td>
      <td style="text-align:left"><b>Indica qual o tipo de documento fiscal</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left">
        <p><b>limita-se apenas aos valores: </b>
        </p>
        <p><b>&#x201C;ecf&#x201D;: SPED Fiscal </b>
        </p>
        <p><b>&#x201C;nfce&#x201D;: Nota Fiscal de Consumidor Eletr&#xF4;nica </b>
        </p>
        <p><b>&#x201C;sat&#x201D;: SAT Fiscal </b>
        </p>
        <p><b>&#x201C;nfe&#x201D;: Nota Fiscal Eletr&#xF4;nica</b>
        </p>
      </td>
      <td style="text-align:left"><b>&#x201C;nfe&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>quantity*</b>
      </td>
      <td style="text-align:left"><b>Quantidade de documentos fiscais</b>
      </td>
      <td style="text-align:left"><b>integer</b>
      </td>
      <td style="text-align:left"><b>inteiro n&#xE3;o-negativo</b>
      </td>
      <td style="text-align:left"><b>3759</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>amount*</b>
      </td>
      <td style="text-align:left"><b>Faturamento total</b>
      </td>
      <td style="text-align:left"><b>float</b>
      </td>
      <td style="text-align:left"><b>Float n&#xE3;o-negativo e este valor deve ser enviado com 4 casas decimais</b>
      </td>
      <td style="text-align:left"><b>123457.9300</b>
      </td>
    </tr>
  </tbody>
</table>\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id  AS "store_id", 
       date     AS "date", 
       type     AS "type", 
       quantity AS "quantity", 
       amount   AS "amount" 
FROM   view_dialy_sellin_total 
GROUP  BY date
```

