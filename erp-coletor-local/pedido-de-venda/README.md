---
description: Dados do Pedido - Cabeçalho
---

# \*Pedido de Venda

#### \*Essa entidade deve ser enviada se caso o ERP possuir empresas do segmento de _Material de Construção._

Modelo de Dados - ORDER

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
      <td style="text-align:left">status</td>
      <td style="text-align:center">Status do pedido</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">
        <p>limita-se a apenas um dos seguintes valores:</p>
        <p>&#x25CF; &#x201C;1&#x201D;&#x200B; : pendente</p>
        <p>&#x25CF; &#x201C;2&#x201D;&#x200B; : processando</p>
        <p>&#x25CF; &#x201C;3&#x201D;&#x200B; : aguardando envio</p>
        <p>&#x25CF; &#x201C;4&#x201D;&#x200B; : enviado</p>
        <p>&#x25CF; &#x201C;5&#x201D;&#x200B; : finalizado</p>
      </td>
      <td style="text-align:right">&#x201C;3&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">grand_total</td>
      <td style="text-align:center">Valor l&#xED;quido do pedido</td>
      <td style="text-align:right">float</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">99.9999</td>
    </tr>
    <tr>
      <td style="text-align:left">subtotal</td>
      <td style="text-align:center">Valor bruto do pedido</td>
      <td style="text-align:right">float</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">199.9999</td>
    </tr>
    <tr>
      <td style="text-align:left">created_at</td>
      <td style="text-align:center">Data e hora de cria&#xE7;&#xE3;o do pedido realizado</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">satisfazer o padr&#xE3;o &#x200B; &#x201C;YYYY-MM-DD HH:MM:SS&#x201D;</td>
      <td
      style="text-align:right">&#x201C;2017-08-20 14:55:08&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">updated_at</td>
      <td style="text-align:center">Data e hora da &#xFA;ltima atualiza&#xE7;&#xE3;o do pedido</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">satisfazer o padr&#xE3;o &#x200B; &#x201C;YYYY-MM-DD HH:MM:SS&#x201D;</td>
      <td
      style="text-align:right">&#x201C;2017-08-20 14:55:08&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">freight_cost</td>
      <td style="text-align:center">Valor do frete</td>
      <td style="text-align:right">float</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">10.0000</td>
    </tr>
    <tr>
      <td style="text-align:left">discount_value</td>
      <td style="text-align:center">Valor de desconto(s) aplicados</td>
      <td style="text-align:right">float</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">9.9000</td>
    </tr>
    <tr>
      <td style="text-align:left">order_number</td>
      <td style="text-align:center">Senha do pedido para chamada em painel eletr&#xF4;nico</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">&quot;91&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">customer.phone_number&#x200B;</td>
      <td style="text-align:center">N&#xFA;mero do telefone do cliente</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">&quot;99999999&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">customer.taxvat&#x200B;</td>
      <td style="text-align:center">CPF ou CNPJ do cliente (apenas n&#xFA;meros)</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">&quot;08965639000113&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">customer.name</td>
      <td style="text-align:center">Raz&#xE3;o social ou nome do cliente</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">&#x201C;Netsuper S.A.&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">customer.phone_area_code</td>
      <td style="text-align:center">DDD do telefone</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">&quot;11&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">customer.customer_id&#x200B;</td>
      <td style="text-align:center">C&#xF3;digo do cliente na plataforma Yandeh</td>
      <td style="text-align:right">string</td>
      <td style="text-align:right">--</td>
      <td style="text-align:right">&#x201C;123233&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">customer.type&#x200B;</td>
      <td style="text-align:center">Define se o cliente &#xE9; Pessoa F&#xED;sica ou Jur&#xED;dica</td>
      <td
      style="text-align:right">string</td>
        <td style="text-align:right">
          <p>limita-se a apenas um dos seguintes valores: &#x25CF; &#x201C;company&#x201D;:
            pessoa jur&#xED;dica</p>
          <p>&#x25CF; &#x201C;person&#x201D;: pessoa f&#xED;sica</p>
        </td>
        <td style="text-align:right">&#x201C;person&#x201D;</td>
    </tr>
  </tbody>
</table>### Exemplo de consulta em SQL:

```text
 SELECT store_id                 AS "store_id", 
       dt_order                 AS "dt_order", 
       order_id                 AS "order_id", 
       status                   AS "status", 
       grand_total              AS "grand_total", 
       subtotal                 AS "subtotal", 
       created_at               AS "created_at", 
       updated_at               AS "updated_at", 
       freight_cost             AS "freight_cost", 
       discount_value           AS "discount_value", 
       order_number             AS "order_number", 
       customer.phone_number    AS "customer.phone_number", 
       customer.taxvat          AS "customer.taxvat", 
       customer.name            AS "customer.name", 
       customer.phone_area_code AS "customer.phone_area_code", 
       customer.customer_id     AS "customer.customer_id", 
       customer.type            AS "customer.type" 
FROM   view_order 
```

