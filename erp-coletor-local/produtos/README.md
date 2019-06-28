---
description: Modelo de Dados - PRODUCTS | Cadastro de Produto
---

# Produtos

## Cadastro de Produto

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
      <td style="text-align:left"><b>dt_ultima_alt*</b>
      </td>
      <td style="text-align:left"><b>Data e hora do cadastro/atualiza&#xE7;&#xE3;o do produto</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>satisfazer o padr&#xE3;o &#x201C;YYYY-MM-DD HH:MM:SS&#x201D;</b>
      </td>
      <td style="text-align:left"><b>&#x201C;2017-08-20 14:55:08&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>code*</b>
      </td>
      <td style="text-align:left"><b>C&#xF3;digo interno do produto</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>tamanho m&#xE1;ximo de 50 caracteres</b>
      </td>
      <td style="text-align:left"><b>&#x201C;3789&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>sku*</b>
      </td>
      <td style="text-align:left"><b>C&#xF3;digo de barras (EAN 13 ou DUN14) quando o mesmo possuir</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>tamanho m&#xE1;ximo de 20 caracteres</b>
      </td>
      <td style="text-align:left"><b>&quot;11402329312324&quot;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>product_type*</b>
      </td>
      <td style="text-align:left"><b>Define o tipo do produto</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left">
        <p><b>Valores aceitos : </b>
        </p>
        <p><b>&#x25CF; &#x201C;simple&#x201D; -&gt; Valor padr&#xE3;o </b>
        </p>
        <p><b>&#x25CF; &#x201C;configurable&#x201D; </b>
        </p>
        <p><b>&#x25CF; &#x201C;grouped&#x201D; </b>
        </p>
        <p><b>&#x25CF; &#x201C;virtual&#x201D; </b>
        </p>
        <p><b>&#x25CF; &#x201C;bundle&#x201D; </b>
        </p>
        <p><b>&#x25CF;&#x201C;downloadable&#x201D;</b>
        </p>
      </td>
      <td style="text-align:left"><b>&#x201C;simple&#x201D;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>name*</b>
      </td>
      <td style="text-align:left"><b>Nome do produto</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>tamanho m&#xE1;ximo de 64 caracteres</b>
      </td>
      <td style="text-align:left"><b>&quot;Coca-cola 300ml&quot;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">brand</td>
      <td style="text-align:left">Marca do produto</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&quot;Cola-Cola Company&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">visibility</td>
      <td style="text-align:left">Visibilidade do produto</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Valores aceitos :</p>
        <p>&#x25CF; &#x201C;C&#x201D; &#x2014; cat&#xE1;logo</p>
        <p>&#x25CF; &#x201C;B&#x201D; &#x2014; busca</p>
        <p>&#x25CF; &#x201C;T&#x201D; &#x2014; cat&#xE1;logo e busca</p>
        <p>&#x25CF; &#x201C;N&#x201D; &#x2014; n&#xE3;o exibir o produto individualmente</p>
      </td>
      <td style="text-align:left">&quot;T&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">sale_start_timestamp</td>
      <td style="text-align:left">Este campo cont&#xE9;m a data/hora <em><b>DO IN&#xCD;CIO</b></em> de oferta
        deste produto; Pode ser usado para indicar produtos sazonais</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">satisfazer o padr&#xE3;o &#x201C;YYYY-MM-DD HH:MM:SS&#x201D;</td>
      <td style="text-align:left">&#x201C;2017-08-20 14:55:08&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">sale_finish_timestamp</td>
      <td style="text-align:left">Este campo cont&#xE9;m a data/hora <em><b>DO FIM</b></em> de oferta deste
        produto; Pode ser usado para indicar produtos sazonais</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">satisfazer o padr&#xE3;o &#x201C;YYYY-MM-DD HH:MM:SS&#x201D;</td>
      <td style="text-align:left">&#x201C;2017-08-20 14:55:08&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">current_supplier</td>
      <td style="text-align:left">Fornecedor ativo para o produto</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&quot;72086766000141&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>status*</b>
      </td>
      <td style="text-align:left"><b>Status do produto na plataforma</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left">
        <p><b>Valores aceitos : </b>
        </p>
        <p><b>&#x25CF; &#x201C;A&#x201D; &#x2014; ativo; </b>
        </p>
        <p><b>&#x25CF; &#x201C;I&#x201D; &#x2014; inativo;</b>
        </p>
      </td>
      <td style="text-align:left"><b>&quot;A&quot;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>description*</b>
      </td>
      <td style="text-align:left"><b>Descri&#xE7;&#xE3;o COMPLETA do produto</b>
      </td>
      <td style="text-align:left"><b>string</b>
      </td>
      <td style="text-align:left"><b>tamanho m&#xE1;ximo de 255 caracteres</b>
      </td>
      <td style="text-align:left"><b>&quot;Coca-cola 300ml em garrafa de vidro - limitada&quot;</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">short_description</td>
      <td style="text-align:left">Descri&#xE7;&#xE3;o RESUMIDA do produto</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">tamanho m&#xE1;ximo 124 caracteres</td>
      <td style="text-align:left">&quot;Coca-cola 300ml&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">manufacturer</td>
      <td style="text-align:left">Nome do fabricante</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">tamanho m&#xE1;ximo de 80 caracteres</td>
      <td style="text-align:left">&quot;Coca-Cola&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">dimension.height_centimeter</td>
      <td style="text-align:left">Altura em cent&#xED;metros</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.0</td>
    </tr>
    <tr>
      <td style="text-align:left">dimension.weight</td>
      <td style="text-align:left">Peso do produto</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.5</td>
    </tr>
    <tr>
      <td style="text-align:left">dimension.measurement_quantity</td>
      <td style="text-align:left">Quantidade medida</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.0</td>
    </tr>
    <tr>
      <td style="text-align:left">dimension.length_centimeter</td>
      <td style="text-align:left">Comprimento em cent&#xED;metros</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.6</td>
    </tr>
    <tr>
      <td style="text-align:left">dimension.width_centimeter</td>
      <td style="text-align:left">Largura em cent&#xED;metros</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">1.9</td>
    </tr>
    <tr>
      <td style="text-align:left">dimension.measurement_unit</td>
      <td style="text-align:left">Unidade de medida</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&quot;KG&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">inventory.is_in_stock</td>
      <td style="text-align:left">Indica se o produto est&#xE1; em estoque ou esgotado</td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">False</td>
    </tr>
    <tr>
      <td style="text-align:left">inventory.manage_stock</td>
      <td style="text-align:left">Indica se o estoque deste produto ser&#xE1; gerenci&#xE1;vel</td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">True</td>
    </tr>
    <tr>
      <td style="text-align:left">inventory.quantity</td>
      <td style="text-align:left">Quantidade em estoque</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">3.0</td>
    </tr>
    <tr>
      <td style="text-align:left">meta_information.meta_description</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">--</td>
    </tr>
    <tr>
      <td style="text-align:left">meta_information.meta_title</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">--</td>
    </tr>
    <tr>
      <td style="text-align:left">meta_information.meta_keywords</td>
      <td style="text-align:left">Rela&#xE7;&#xE3;o de palavras-chave utilizadas nos motores de busca, separadas
        por v&#xED;rgula</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&quot;coca-cola, coca, refrigerante, cola&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">price_info.price</td>
      <td style="text-align:left">Pre&#xE7;o</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">3.65</td>
    </tr>
    <tr>
      <td style="text-align:left">price_info.special_price_from</td>
      <td style="text-align:left">Data de in&#xED;cio do pre&#xE7;o promocional</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&#x201C;2018-01-01&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">price_info.special_price_to</td>
      <td style="text-align:left">Data de t&#xE9;rmino do pre&#xE7;o promocional</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&#x201C;2018-02-01&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">price_info.special_price</td>
      <td style="text-align:left">Pre&#xE7;o Promocional</td>
      <td style="text-align:left">float</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">3.25</td>
    </tr>
    <tr>
      <td style="text-align:left">manufacturer_code</td>
      <td style="text-align:left">C&#xF3;digo do fabricante</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">--</td>
      <td style="text-align:left">&quot;8928329&quot;</td>
    </tr>
  </tbody>
</table>\*Campos obrigatórios

### Exemplo da consulta em SQL:

```text
SELECT store_id                          AS "store_id", 
       dt_ultima_alt                     AS "dt_ultima_alt", 
       sku                               AS "sku", 
       code                              AS "code", 
       product_type                      AS "product_type", 
       name                              AS "name", 
       sale_finish_timestamp             AS "sale_finish_timestamp", 
       brand                             AS "brand", 
       visibility                        AS "visibility", 
       sale_start_timestamp              AS "sale_start_timestamp", 
       current_supplier                  AS "current_supplier", 
       status                            AS "status", 
       short_description                 AS "short_description", 
       manufacturer                      AS "manufacturer", 
       description                       AS "description", 
       dimension.height_centimeter       AS "dimension.height_centimeter", 
       dimension.weight                  AS "dimension.weight", 
       dimension.measurement_quantity    AS "dimension.measurement_quantity", 
       dimension.length_centimeter       AS "dimension.length_centimeter", 
       dimension.width_centimeter        AS "dimension.width_centimeter", 
       dimension.measurement_unit        AS "dimension.measurement_unit", 
       dimension.weight_unit             AS "dimension.weight_unit", 
       inventory.is_in_stock             AS "inventory.is_in_stock", 
       inventory.manage_stock            AS "inventory.manage_stock", 
       inventory.quantity                AS "inventory.quantity", 
       meta_information.meta_description AS "meta_information.meta_description", 
       meta_information.meta_title       AS "meta_information.meta_title", 
       meta_information.meta_keywords    AS "meta_information.meta_keywords", 
       price_info.price                  AS "price_info.price", 
       price_info.special_price_from     AS "price_info.special_price_from", 
       price_info.special_price_to       AS "price_info.special_price_to", 
       price_info.special_price          AS "price_info.special_price" 
FROM   view_product
```

