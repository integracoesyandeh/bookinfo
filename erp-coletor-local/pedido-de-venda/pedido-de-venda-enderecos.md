---
description: Endereços
---

# Pedido de venda - Endereços

#### Essa entidade deve ser enviada se caso o ERP possuir empresas do segmento de _Material de Construção._

Modelo de Dados - ORDER-ADDRESSES

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
      <td style="text-align:right"><b>&#x201C;ABC1233233&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">zipcode</td>
      <td style="text-align:center">CEP</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 8 caracteres</td>
      <td style="text-align:right"><b>&#x201C;</b>38400440<b>&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">address</td>
      <td style="text-align:center">Endere&#xE7;o</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 50 caracteres</td>
      <td style="text-align:right">&quot;Rua Francisco Sales&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">address_type</td>
      <td style="text-align:center">Tipo de Endere&#xE7;o</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">
        <p>Valores aceitos&#x200B; :</p>
        <p>&#x25CF; &#x201C;shipping&#x201D;</p>
        <p>&#x25CF; &#x201C;billing&#x201D;</p>
      </td>
      <td style="text-align:right">--</td>
    </tr>
    <tr>
      <td style="text-align:left">address_number</td>
      <td style="text-align:center">N&#xFA;mero do endere&#xE7;o</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 10 caracteres</td>
      <td style="text-align:right">&quot;287&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">address_extra</td>
      <td style="text-align:center">Complemento do endere&#xE7;o</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 50 caracteres</td>
      <td style="text-align:right">&quot;8o. andar&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">neighborhood</td>
      <td style="text-align:center">Bairro</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 50 caracteres</td>
      <td style="text-align:right">&quot;Santa M&#xF4;nica&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">city</td>
      <td style="text-align:center">Cidade</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 50 caracteres</td>
      <td style="text-align:right">&quot;Uberl&#xE2;ndia&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">state</td>
      <td style="text-align:center">UF do endere&#xE7;o</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 2 caracteres</td>
      <td style="text-align:right">&quot;MG&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">country</td>
      <td style="text-align:center">C&#xF3;digo do pa&#xED;s no formato ISO 3166 (2 digitos)</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">tamanho m&#xE1;ximo de 3 caracteres</td>
      <td style="text-align:right">&quot;BR&quot;</td>
    </tr>
  </tbody>
</table>### Exemplo de consulta em SQL:

```text
SELECT store_id       AS "store_id", 
       order_id       AS "order_id", 
       city           AS "city", 
       neighborhood   AS "neighborhood", 
       address_number AS "address_number", 
       address_extra  AS "address_extra", 
       country        AS "country", 
       zipcode        AS "zipcode", 
       state          AS "state", 
       address        AS "address", 
       address_type   AS "address_type" 
FROM   view_order_addresses
```

