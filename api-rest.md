# API-REST

API-REST

O objetivo da Integração API da Yandeh é permitir que o lojista continue utilizando sua solução de frente de caixa \(Automação Comercial ou PDV\) e a integre através de uma API construída no padrão REST

A API Yandeh possui as seguintes características:

• Recursos REST, de forma que seja possível acessar por meio de semântica HTTP padrão.

• Códigos de status HTTP para comunicar o sucesso/erro nas chamadas.

• Todas as requisições e respostas encontram-se no formato JSON.

> Acesse a documentação [Swagger Hub](https://app.swaggerhub.com/apis/thiago.franca/erp-yandeh-integration/1.0.0.8/).

## Linguagem de Programação  <a id="linguagem-de-programa&#xE7;&#xE3;o"></a>

A solução **API Rest** da plataforma **da Yandeh Integration** foi desenvolvida com a tecnologia REST, que é padrão de mercado e independe da tecnologia utilizada por nossos clientes. Dessa forma, é possível integrar-se utilizando as mais variadas linguagens de programação, tais como:

* Net
* Java
* Delphi
* Python

### Segurança  <a id="seguran&#xE7;a"></a>

Estas operações devem ser executadas utilizando sua chave específica que chamamos de **TOKEN**, o mesmo será responsável por autenticar o acesso ao sistema.

> **Note:** Solicitar acesso para equipe integração da Yandeh.

### Certificado SSL  <a id="certificado-ssl"></a>

O Certificado SSL para servidor web oferece autenticidade e integridade dos dados de um web site, proporcionando aos clientes das lojas virtuais a garantia de que estão realmente acessando o site que desejam, e não uma um site fraudador.

### Glossário dos Métodos  <a id="gloss&#xE1;rio-dos-m&#xE9;todos"></a>

A troca de mensagens são pelas URLs os métodos receberão as mensagens HTTP através dos métodos POST, GET ou PUT.

| Método | Descrição |
| :--- | :--- |
| **POST** | `'Envio de informações que serão processadas. Por exemplo, criação de uma transação'` |
| **PUT** | `"Utilizado para atualização de um recurso já existente. Por exemplo, captura ou cancelamento de uma transação previamente autorizada."` |
| **GET** | `Utilizado para consultas de recursos já existentes. Por exemplo, consulta de transações.` |

