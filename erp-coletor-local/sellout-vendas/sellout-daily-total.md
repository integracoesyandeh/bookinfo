---
description: Modelo de Dados - "Daily_Sellout_Total" | Valor total de venda por dia
---

# Vendas - Total Diário

Modelo de Dados - "Daily\_Sellout\_Total" \| Valor total de venda por dia.

**Essa entidade não é obrigatória para o Escopo Reduzido \(MVP1\).**

## Vendas total por dia

| Campo | Descrição | Tipo | Restrições | Exemplo |
| :--- | :--- | :--- | :--- | :--- |


| **store\_id\*** | **Identificador interno da loja** | **integer ou string** | **--** | **1** |
| :--- | :--- | :--- | :--- | :--- |


| **date\*** | **Data do dia** | **string** | **satisfazer o padrão “YYYY-MM-DD”** | **“2018-08-13”** |
| :--- | :--- | :--- | :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>type*</b>
      </th>
      <th style="text-align:left"><b>Indica qual o tipo de documento fiscal</b>
      </th>
      <th style="text-align:left"><b>string</b>
      </th>
      <th style="text-align:left">
        <p><b>limita-se apenas aos valores:</b>
        </p>
        <p><b>&#x201C;ecf&#x201D;: SPED Fiscal</b>
        </p>
        <p><b>&#x201C;nfce&#x201D;: Nota Fiscal de Consumidor Eletr&#xF4;nica</b>
        </p>
        <p><b>&#x201C;sat&#x201D;: SAT Fiscal</b>
        </p>
        <p><b>&#x201C;nfe&#x201D;: Nota Fiscal Eletr&#xF4;nica</b>
        </p>
      </th>
      <th style="text-align:left"><b>&#x201C;nfe&#x201D;</b>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| **quantity\*** | **Quantidade de documentos fiscais** | **integer** | **inteiro não-negativo** | **3759** |
| :--- | :--- | :--- | :--- | :--- |


| **amount\*** | **Faturamento total** | **float** | **float não-negativo** | **123457.9300** |
| :--- | :--- | :--- | :--- | :--- |


```text
    SELECT store_id AS "store_id", 
           date     AS "date", 
           type     AS "type", 
           quantity AS "quantity", 
           amount   AS "amount" 
    FROM   view_daily_sellout_total 
    GROUP  BY date
```

