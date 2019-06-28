# Coletor ERP

Esse modelo possui o seguinte fluxo:

1. Leitura da documentação sobre a Coletor ERP.
2. Criação das query’s através das views
3. Instalação Monitorada - Homologação
4. Validação das views por parte do nosso time Yandeh. 
5. Validação dos dados recebidos.
6. Cadastro da loja piloto no Portal ERP.
7. Instalação do Coletor personalizado na loja piloto selecionada pelo parceiro.
8. Validação dos dados recebidos da loja piloto.
9. Pronto, aproveite ao máximo tudo que a Integração com a Yandeh pode oferecer para você!!

A seguir, apresentamos o escopo reduzido:

| Entidade | Descrição |
| :--- | :--- |
| [Store](store.md) | Loja do cliente |
| [Compras \(Sellin\)](sellin/) | Compras realizadas pelos clientes |
| [Vendas \(Sellout\)](sellout-vendas/) | Vendas realizadas pelos clientes |
| [Products \(Produtos\)](https://wiki-yandeh.gitbook.io/yandeh/erp-coletor-local/produtos) | Cadastro de produto e suas respectivas categorias |

**IMPORTANTE:** Se o ERP possuir clientes do segmento de Materiais de Construção, é necessário enviar as entidades [Pedido de Venda\(Order\)](pedido-de-venda/) e [Notas fiscais - Pedido de Venda\(Order\_Invoice\)](notas-fiscais-do-pedido/) para o escopo reduzido.

