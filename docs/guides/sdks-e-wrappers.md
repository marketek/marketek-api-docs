# SDKs e Wrappers de API

### SDKs e Wrappers de API

Para acelerar o desenvolvimento, muitos desenvolvedores procuram por um SDK (Software Development Kit).

**Existem SDKs oficiais da Marketek?**

Atualmente, a Marketek **não oferece SDKs oficiais**. Embora existam algumas bibliotecas criadas pela comunidade para linguagens como Node.js ou PHP, elas não são mantidas por nossa equipe.

**Recomendação: Crie seu Próprio Wrapper**

Para integrações profissionais e robustas, a melhor prática é construir um "wrapper" ou "cliente de API" simples dentro da sua própria base de código.

Um wrapper é uma classe ou um conjunto de funções que lida com os detalhes da comunicação com a API da Marketek:

*   Centraliza a URL base e a chave de API.
*   Adiciona os cabeçalhos de autenticação e versionamento a todas as requisições.
*   Lida com a serialização (conversão para JSON) dos dados enviados.
*   Trata as respostas e possíveis erros de forma padronizada.

Criar seu próprio wrapper lhe dá controle total sobre a implementação, mais segurança e a flexibilidade para adaptá-lo exatamente às necessidades da sua aplicação.

* * *

### SDKs & API Wrappers

To accelerate development, many developers look for an SDK (Software Development Kit).

**Are there official Marketek SDKs?**

Currently, Marketek **does not offer official SDKs**. While some community-created libraries exist for languages like Node.js or PHP, they are not maintained by our team.

**Recommendation: Build Your Own Wrapper**

For professional and robust integrations, the best practice is to build a simple "wrapper" or "API client" within your own codebase.

A wrapper is a class or a set of functions that handles the details of communicating with the Marketek API:

*   It centralizes the base URL and the API key.
*   It adds the authentication and versioning headers to all requests.
*   It handles data serialization (conversion to JSON).
*   It handles responses and potential errors in a standardized way.

Building your own wrapper gives you full control over the implementation, more security, and the flexibility to tailor it precisely to your application's needs.

