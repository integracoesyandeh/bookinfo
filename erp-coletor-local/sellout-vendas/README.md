---
description: Modelo de Dados - "SellOut" | Vendas para Clientes
---

# Vendas

| A entidade Sellout  tem como registros cada uma das vendas realizadas para os clientes. Estando preparada para descrever cada um dos seguintes tipos fiscais: ECF, CF-e, NF-e e NFC-e, SAT; E também as vendas gerenciais, esta deve ser enviada com o tipo 'ECF'. |
| :--- |


## SellOut  <a id="sellin---itens"></a>

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
      <td style="text-align:center"><b>id*</b>
      </td>
      <td style="text-align:left"><b>Identificador da venda</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>tamanho m&#xE1;ximo de 50 caracteres</b>
      </td>
      <td style="text-align:left"><b>&#x201C;RCNTH345987&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:center"><b>sellout_timestamp*</b>
      </td>
      <td style="text-align:left"><b>Data e hora da venda</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>satisfazer o padr&#xE3;o &#x201C;YYYY-MM-DDTHH:MM:SS&#x201D;</b>
      </td>
      <td style="text-align:left"><b>&#x201C;2017-08-20T14:55:08</b>&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:center">nome_operador</td>
      <td style="text-align:left">Nome do operador do PDV</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&#x201C;Maria Cristina&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:center">nome_vendedor</td>
      <td style="text-align:left">Nome do vendedor</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&#x201C;Ana Maria&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:center"><b>store_taxpayer_id*</b>
      </td>
      <td style="text-align:left"><b>CNPJ da loja que realizou a venda</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>tamanho exato de 14 caracteres</b>
      </td>
      <td style="text-align:left"><b>&#x201C;05345647000122&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">buyer_taxpayer_id</td>
      <td style="text-align:left">CPF ou CNPJ do comprador final</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">tamanho exato de 11 ou 14 caracteres</td>
      <td style="text-align:left">&#x201C;83230677323&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:center">checkout_id</td>
      <td style="text-align:left">Identificador do ponto de venda</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&#x201C;2938923&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:center"><b>receipt_number*</b>
      </td>
      <td style="text-align:left"><b>N&#xFA;mero do documento fiscal (NF-e/NFC-e/CF-e)</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>tamanho m&#xE1;ximo de 50 caracteres</b>
      </td>
      <td style="text-align:left"><b>&#x201C;33093&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:center"><b>receipt_series_number*</b>
      </td>
      <td style="text-align:left"><b>S&#xE9;rie do documento fiscal (NF-e/NFC-e/CF-e) ou CCF (ECF)</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>No caso de documento ECF, obrigat&#xF3;rio informar o CCF neste campo</b>
      </td>
      <td style="text-align:left"><b>&#x201C;27&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:center"><em>coo*</em>
      </td>
      <td style="text-align:left"><em>N&#xFA;mero do COO (ECF)</em>
      </td>
      <td style="text-align:left"><em>string</em>
      </td>
      <td style="text-align:left"><em>Campo obrigat&#xF3;rio para documentos tipo ECF</em>
      </td>
      <td style="text-align:left"><em>&#x201C;123742&#x201D;</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:center"><b>nfe_access_key*</b>
      </td>
      <td style="text-align:left"><b>Chave do documento NFC-e/CF-e associado &#xE0; venda</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>Satisfazer o padr&#xE3;o exato de come&#xE7;ar com 3 caracteres de tipo (&#x201C;NFe&#x201D; ou &#x201C;CFe&#x201D;) seguido por 44 caracteres num&#xE9;ricos</b>
      </td>
      <td style="text-align:left">
        <p><b>NFCe:&#x201C;NFe31170901704848000164650020000018481058491134&#x201D; ou</b>
        </p>
        <p><b>CF-e: &#x201C;CFe35150310860014000139590010000162181020002180&#x201D;;</b>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:center"><em>device_id*</em>
      </td>
      <td style="text-align:left"><em>N&#xFA;mero do dispositivo</em>
      </td>
      <td style="text-align:left"><em>string</em>
      </td>
      <td style="text-align:left"><em>Deve sempre ser fornecido para documentos do tipo ECF e em forma completa (em vez de reduzida). Tamanho m&#xE1;ximo de 50 caracteres</em>
      </td>
      <td style="text-align:left"><em>&#x201C;BE1000199329329922&#x201D;</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">seller_id</td>
      <td style="text-align:left">CPF do vendedor associado a esta, caso exista vendedor relacionado</td>
      <td
      style="text-align:left">string</td>
        <td style="text-align:left">tamanho exato de 11 caracteres</td>
        <td style="text-align:left">&#x201C;83230677323&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:center"><b>sales_addition*</b>
      </td>
      <td style="text-align:left"><b>Valor de acr&#xE9;scimo na venda</b>
      </td>
      <td style="text-align:left"><b>float</b>
      </td>
      <td style="text-align:left"><b>--</b>
      </td>
      <td style="text-align:left"><b>0.5000</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:center"><b>sales_discount*</b>
      </td>
      <td style="text-align:left"><b>Valor de desconto na venda</b>
      </td>
      <td style="text-align:left"><b>float</b>
      </td>
      <td style="text-align:left"><b>--</b>
      </td>
      <td style="text-align:left"><b>1.7500</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:center"><b>subtotal*</b>
      </td>
      <td style="text-align:left"><b>Valor do subtotal da venda</b>
      </td>
      <td style="text-align:left"><b>float</b>
      </td>
      <td style="text-align:left"><b>--</b>
      </td>
      <td style="text-align:left"><b>5.9300</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:center"><b>cancellation_flag*</b>
      </td>
      <td style="text-align:left"><b>Indica se a venda foi cancelada ou n&#xE3;o</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left">
        <p><b>limita-se apenas aos valores:</b>
        </p>
        <p><b>&#x25CF; &#x201C;N&#x201D; : venda n&#xE3;o-cancelada &#x25CF; &#x201C;S&#x201D; : venda cancelada</b>
        </p>
      </td>
      <td style="text-align:left"><b>&#x201C;N</b>&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:center">operation</td>
      <td style="text-align:left">Tipo da opera&#xE7;&#xE3;o realizada</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>limita-se apenas aos valores:</p>
        <p>&#x25CF; &#x201C;E&#x201D; : entrada</p>
        <p>&#x25CF; &#x201C;S&#x201D; : sa&#xED;da</p>
        <p>&#x25CF; &#x201C;DE&#x201D; : devolu&#xE7;&#xE3;o de entrada</p>
        <p>&#x25CF; &#x201C;DS&#x201D; : devolu&#xE7;&#xE3;o de sa&#xED;da</p>
        <p>&#x25CF; &#x201C;N&#x201D; : neutro</p>
        <p>&#x25CF; &#x201C;NULL&#x201D; : n&#xE3;o dispon&#xED;vel</p>
      </td>
      <td style="text-align:left">&#x201C;E&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:center">transaction_type</td>
      <td style="text-align:left">Indica qual tipo de transa&#xE7;&#xE3;o realizada</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>limita-se apenas aos valores:</p>
        <p>&#x25CF; &#x201C;J&#x201D; : ajuste de estoque</p>
        <p>&#x25CF; &#x201C;P&#x201D; : faturamento de pedido</p>
        <p>&#x25CF; &#x201C;S&#x201D; : normal</p>
        <p>&#x25CF; &#x201C;E&#x201D; : entrada</p>
        <p>&#x25CF; &#x201C;D&#x201D; : transfer&#xEA;ncia entre dep&#xF3;sitos</p>
        <p>&#x25CF; &#x201C;T&#x201D; : transfer&#xEA;ncia</p>
      </td>
      <td style="text-align:left">&quot;P&quot;</td>
    </tr>
    <tr>
      <td style="text-align:center">ipi</td>
      <td style="text-align:left">Valor do IPI sobre a venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.8700</td>
    </tr>
    <tr>
      <td style="text-align:center">iss</td>
      <td style="text-align:left">Valor do ISS sobre a venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.0100</td>
    </tr>
    <tr>
      <td style="text-align:center">frete</td>
      <td style="text-align:left">Valor de frete da venda</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">25.9800</td>
    </tr>
    <tr>
      <td style="text-align:center"><b>tipo*</b>
      </td>
      <td style="text-align:left"><b>Indica qual tipo de documento fiscal</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left">
        <p><b>limita-se apenas aos valores:</b>
        </p>
        <p><b>&#x25CF; &#x201C;ecf&#x201D; : SPED Fiscal</b>
        </p>
        <p><b>&#x25CF; &#x201C;nfce&#x201D; : Nota Fiscal de Consumidor Eletr&#xF4;nica</b>
        </p>
        <p><b>&#x25CF; &#x201C;sat&#x201D; : SAT Fiscal</b>
        </p>
        <p><b>&#x25CF; &#x201C;nfe&#x201D; : Nota Fiscal Eletr&#xF4;nica</b>
        </p>
      </td>
      <td style="text-align:left"><b>&#x201C;nfce&#x201D;</b>
      </td>
    </tr>
  </tbody>
</table>\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id              AS "store_id", 
       sellout_timestamp     AS "sellout_timestamp", 
       id                    AS "id", 
       nome_operador         AS "nome_operador", 
       nome_vendedor         AS "nome_vendedor", 
       store_taxpayer_id     AS "store_taxpayer_id", 
       buyer_taxpayer_id     AS "buyer_taxpayer_id", 
       checkout_id           AS "checkout_id", 
       receipt_number        AS "receipt_number", 
       receipt_series_number AS "receipt_series_number", 
       coo                   AS "coo", 
       nfe_access_key        AS "nfe_access_key", 
       device_id             AS "device_id", 
       seller_id             AS "seller_id", 
       sales_addition        AS "sales_addition", 
       sales_discount        AS "sales_discount", 
       subtotal              AS "subtotal", 
       cancellaion_flag      AS "cancellaion_flag", 
       operation             AS "operation", 
       transaction_type      AS "transaction_type", 
       ipi                   AS "ipi", 
       iss                   AS "iss", 
       frete                 AS "frete", 
       tipo                  AS "tipo" 
FROM   view_sellout
```

