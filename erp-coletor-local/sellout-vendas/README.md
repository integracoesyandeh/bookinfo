---
description: Modelo de Dados - "SellOut" | Vendas para Clientes
---

# Vendas

| A entidade Sellout  tem como registros cada uma das vendas realizadas para os clientes. Estando preparada para descrever cada um dos seguintes tipos fiscais: ECF, CF-e, NF-e e NFC-e, SAT; E também as vendas gerenciais, esta deve ser enviada com o tipo 'ECF'. |
| :--- |


## SellOut   <a id="sellin---itens"></a>

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :--- | :--- | :--- | :--- |


| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| :--- | :--- | :--- | :--- | :--- |


| **id\*** | **Identificador da venda** | **string** | **tamanho máximo de 50 caracteres** | **“RCNTH345987”** |
| :--- | :--- | :--- | :--- | :--- |


| **sellout\_timestamp\*** | **Data e hora da venda** | **string** | **satisfazer o padrão “YYYY-MM-DDTHH:MM:SS”** | **“2017-08-20T14:55:08**” |
| :--- | :--- | :--- | :--- | :--- |


| nome\_operador | Nome do operador do PDV | string | -- | “Maria Cristina” |
| :--- | :--- | :--- | :--- | :--- |


| nome\_vendedor | Nome do vendedor | string | -- | “Ana Maria” |
| :--- | :--- | :--- | :--- | :--- |


| **store\_taxpayer\_id\*** | **CNPJ da loja que realizou a venda** | **string** | **tamanho exato de 14 caracteres** | **“05345647000122”** |
| :--- | :--- | :--- | :--- | :--- |


| buyer\_taxpayer\_id | CPF ou CNPJ do comprador final | string | tamanho exato de 11 ou 14 caracteres | “83230677323” |
| :--- | :--- | :--- | :--- | :--- |


| checkout\_id | Identificador do ponto de venda | string | -- | “2938923” |
| :--- | :--- | :--- | :--- | :--- |


| **receipt\_number\*** | **Número do documento fiscal \(NF-e/NFC-e/CF-e\)** | **string** | **tamanho máximo de 50 caracteres** | **“33093”** |
| :--- | :--- | :--- | :--- | :--- |


| **receipt\_series\_number\*** | **Série do documento fiscal \(NF-e/NFC-e/CF-e\) ou CCF \(ECF\)** | **string** | **No caso de documento ECF, obrigatório informar o CCF neste campo** | **“27”** |
| :--- | :--- | :--- | :--- | :--- |


| _coo\*_ | _Número do COO \(ECF\)_ | _string_ | _Campo obrigatório para documentos tipo ECF_ | _“123742”_ |
| :--- | :--- | :--- | :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>nfe_access_key*</b>
      </th>
      <th style="text-align:left"><b>Chave do documento NFC-e/CF-e associado &#xE0; venda</b>
      </th>
      <th style="text-align:left"><b>string</b>
      </th>
      <th style="text-align:left"><b>Satisfazer o padr&#xE3;o exato de come&#xE7;ar com 3 caracteres de tipo (&#x201C;NFe&#x201D; ou &#x201C;CFe&#x201D;) seguido por 44 caracteres num&#xE9;ricos</b>
      </th>
      <th style="text-align:left">
        <p><b>NFCe:&#x201C;NFe31170901704848000164650020000018481058491134&#x201D; ou</b>
        </p>
        <p><b>CF-e: &#x201C;CFe35150310860014000139590010000162181020002180&#x201D;;</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| _device\_id\*_ | _Número do dispositivo_ | _string_ | _Deve sempre ser fornecido para documentos do tipo ECF e em forma completa \(em vez de reduzida\). Tamanho máximo de 50 caracteres_ | _“BE1000199329329922”_ |
| :--- | :--- | :--- | :--- | :--- |


| seller\_id | CPF do vendedor associado a esta, caso exista vendedor relacionado | string | tamanho exato de 11 caracteres | “83230677323” |
| :--- | :--- | :--- | :--- | :--- |


| **sales\_addition\*** | **Valor de acréscimo na venda** | **float** | **--** | **0.5000** |
| :--- | :--- | :--- | :--- | :--- |


| **sales\_discount\*** | **Valor de desconto na venda** | **float** | **--** | **1.7500** |
| :--- | :--- | :--- | :--- | :--- |


| **subtotal\*** | **Valor do subtotal da venda** | **float** | **--** | **5.9300** |
| :--- | :--- | :--- | :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>cancellation_flag*</b>
      </th>
      <th style="text-align:left"><b>Indica se a venda foi cancelada ou n&#xE3;o</b>
      </th>
      <th style="text-align:left"><b>string</b>
      </th>
      <th style="text-align:left">
        <p><b>limita-se apenas aos valores:</b>
        </p>
        <p><b>&#x25CF; &#x201C;N&#x201D; : venda n&#xE3;o-cancelada &#x25CF; &#x201C;S&#x201D; : venda cancelada</b>
        </p>
      </th>
      <th style="text-align:left"><b>&#x201C;N</b>&#x201D;</th>
    </tr>
  </thead>
  <tbody></tbody>
</table><table>
  <thead>
    <tr>
      <th style="text-align:left">operation</th>
      <th style="text-align:left">Tipo da opera&#xE7;&#xE3;o realizada</th>
      <th style="text-align:left">string</th>
      <th style="text-align:left">
        <p>limita-se apenas aos valores:</p>
        <p>&#x25CF; &#x201C;E&#x201D; : entrada</p>
        <p>&#x25CF; &#x201C;S&#x201D; : sa&#xED;da</p>
        <p>&#x25CF; &#x201C;DE&#x201D; : devolu&#xE7;&#xE3;o de entrada</p>
        <p>&#x25CF; &#x201C;DS&#x201D; : devolu&#xE7;&#xE3;o de sa&#xED;da</p>
        <p>&#x25CF; &#x201C;N&#x201D; : neutro</p>
        <p>&#x25CF; &#x201C;NULL&#x201D; : n&#xE3;o dispon&#xED;vel</p>
      </th>
      <th style="text-align:left">&#x201C;E&#x201D;</th>
    </tr>
  </thead>
  <tbody></tbody>
</table><table>
  <thead>
    <tr>
      <th style="text-align:left">transaction_type</th>
      <th style="text-align:left">Indica qual tipo de transa&#xE7;&#xE3;o realizada</th>
      <th style="text-align:left">string</th>
      <th style="text-align:left">
        <p>limita-se apenas aos valores:</p>
        <p>&#x25CF; &#x201C;J&#x201D; : ajuste de estoque</p>
        <p>&#x25CF; &#x201C;P&#x201D; : faturamento de pedido</p>
        <p>&#x25CF; &#x201C;S&#x201D; : normal</p>
        <p>&#x25CF; &#x201C;E&#x201D; : entrada</p>
        <p>&#x25CF; &#x201C;D&#x201D; : transfer&#xEA;ncia entre dep&#xF3;sitos</p>
        <p>&#x25CF; &#x201C;T&#x201D; : transfer&#xEA;ncia</p>
      </th>
      <th style="text-align:left">&quot;P&quot;</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| ipi | Valor do IPI sobre a venda | float | -- | 1.8700 |
| :--- | :--- | :--- | :--- | :--- |


| iss | Valor do ISS sobre a venda | float | -- | 1.0100 |
| :--- | :--- | :--- | :--- | :--- |


| frete | Valor de frete da venda | float | -- | 25.9800 |
| :--- | :--- | :--- | :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>tipo*</b>
      </th>
      <th style="text-align:left"><b>Indica qual tipo de documento fiscal</b>
      </th>
      <th style="text-align:left"><b>string</b>
      </th>
      <th style="text-align:left">
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
      </th>
      <th style="text-align:left"><b>&#x201C;nfce&#x201D;</b>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>```text
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

