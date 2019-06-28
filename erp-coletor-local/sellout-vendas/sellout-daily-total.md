---
description: Modelo de Dados - "Daily_Sellout_Total" | Valor total de venda por dia
---

# Vendas - Total Diário

Modelo de Dados - "Daily\_Sellout\_Total" \| Valor total de venda por dia.

**Essa entidade não é obrigatória para o Escopo Reduzido \(MVP1\).**

## Vendas total por dia

<table>
  <thead>
    <tr>
      <th style="text-align:center">Campo</th>
      <th style="text-align:left">Descri&#xE7;&#xE3;o</th>
      <th style="text-align:left">Tipo</th>
      <th style="text-align:left">Restri&#xE7;&#xF5;es</th>
      <th style="text-align:left">Exemplo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center"><b>store_id*</b>
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
      <td style="text-align:center"><b>date*</b>
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
      <td style="text-align:center"><b>type*</b>
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
      <td style="text-align:center"><b>quantity*</b>
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
      <td style="text-align:center"><b>amount*</b>
      </td>
      <td style="text-align:left"><b>Faturamento total</b>
      </td>
      <td style="text-align:left"><b>float</b>
      </td>
      <td style="text-align:left"><b>float n&#xE3;o-negativo</b>
      </td>
      <td style="text-align:left"><b>123457.9300</b>
      </td>
    </tr>
  </tbody>
</table>### Exemplo da consulta em SQL:

```text
    SELECT store_id AS "store_id", 
           date     AS "date", 
           type     AS "type", 
           quantity AS "quantity", 
           amount   AS "amount" 
    FROM   view_daily_sellout_total 
    GROUP  BY date
```

