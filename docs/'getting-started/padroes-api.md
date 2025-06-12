# Padrões da API

Para garantir uma experiência de desenvolvimento consistente, nossa API segue um conjunto de padrões comuns.

### URL Base

Todas as URLs da API v2 começam com o seguinte prefixo. Nossos servidores são baseados na infraestrutura white-label da Lead-Connector.

**URL Base:**

[https://services.leadconnectorhq.com/](https://services.leadconnectorhq.com/)

### Versionamento

A API da Marketek utiliza um cabeçalho de versionamento baseado em data para garantir que futuras atualizações não quebrem sua integração. É altamente recomendado que você sempre inclua este cabeçalho em suas requisições.

**Cabeçalho de Versão:** `Version: 2021-07-28`

### Formato de Dados

Nossa API utiliza o formato `JSON` para todas as requisições e respostas. Certifique-se de que o cabeçalho `Content-Type` de suas requisições `POST` e `PUT` esteja definido como `application/json`.

### Campos de Resposta Padrão

Nossas respostas seguem uma estrutura padrão para facilitar o tratamento de sucesso e erro, conforme detalhado na documentação de referência da Lead-Connector.

*   `success`: Um booleano (`true` ou `false`) que indica se a requisição foi bem-sucedida.
*   `data`: (Em caso de sucesso) Contém os dados solicitados. Pode ser um objeto ou um array de objetos.
*   `meta`: (Em caso de sucesso e em listas) Contém informações de paginação, como `total`, `currentPage`, `nextPage`, etc.
*   `errors`: (Em caso de falha) Contém um array com detalhes sobre o erro, incluindo uma mensagem descritiva.

  

* * *

# API Standards

To ensure a consistent development experience, our API follows a set of common standards.

### Base URL

All v2 API URLs are prefixed with the following. Our servers are based on the Lead-Connector white-label infrastructure.

**Base URL:**

[https://services.leadconnectorhq.com/](https://services.leadconnectorhq.com/)

### Versioning

The Marketek API uses a date-based versioning header to ensure that future updates do not break your integration. It is highly recommended that you always include this header in your requests.

**Version Header:** `Version: 2021-07-28`

