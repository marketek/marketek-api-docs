# Autenticação

# Autenticação

Para garantir a segurança dos seus dados, todas as requisições à API da Marketek devem ser autenticadas. A autenticação é feita através de uma Chave de API (API Key).

### Onde Encontrar sua Chave de API

Sua chave de API de **Nível de Localização (Subconta)** pode ser encontrada no painel da sua subconta, em: `Configurações > Informações da Empresa > Chave de API`

### Como Usar sua Chave

Você deve incluir sua chave de API no cabeçalho (`header`) de cada requisição, utilizando o método de autenticação `Bearer Token`.

**Formato do Cabeçalho:**`Authorization: Bearer SUA_CHAVE_API`

Substitua `SUA_CHAVE_API` pela chave que você copiou do seu painel. Requisições feitas sem um token válido ou com um token incorreto retornarão um erro `401 Unauthorized`.

  

* * *

# Authentication

To ensure the security of your data, all requests to the Marketek API must be authenticated. Authentication is done via an API Key.

### Where to Find Your API Key

Your **Location Level (Sub-account)** API Key can be found in your sub-account dashboard at: `Settings > Business Info > API Key`

### How to Use Your Key

You must include your API Key in the header of every request, using the `Bearer Token` authentication method.

**Header Format:**`Authorization: Bearer YOUR_API_KEY`

Replace `YOUR_API_KEY` with the key you copied from your dashboard. Requests made without a valid token or with an incorrect token will return a `401 Unauthorized` error.

