# Empresas

# Endpoints de Empresas

Para cenários B2B, você pode usar a API para agrupar múltiplos contatos sob uma única entidade de Empresa.

### Listar Empresas

Recupere uma lista de todas as empresas criadas na sua localização.

**Endpoint:** `GET /businesses/search`

**Parâmetros de Query:**

*   `locationId` (obrigatório): O ID da sua subconta.

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/businesses/search?locationId=SEU_LOCATION_ID' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

### Criar uma Empresa

Crie um novo registro de empresa.

**Endpoint:** `POST /businesses/`

**Corpo da Requisição (JSON):**

JSON

  

```perl
{
    "locationId": "SEU_LOCATION_ID",
    "name": "Nome da Empresa Exemplo",
    "email": "contato@empresaexemplo.com",
    "phone": "+5511987654321",
    "address": "Endereço da Empresa, 123"
}
```

Para associar um contato a uma empresa, utilize o endpoint de atualização de contato (`PUT /contacts/{contactId}`) e adicione o campo `businessId` com o ID da empresa correspondente.

  

* * *

  

# Companies Endpoints

For B2B scenarios, you can use the API to group multiple contacts under a single Company entity.

### List Companies

Retrieve a list of all companies created in your location.

**Endpoint:** `GET /businesses/search`

**Query Parameters:**

*   `locationId` (required): Your sub-account's ID.

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/businesses/search?locationId=YOUR_LOCATION_ID' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

### Create a Company

Create a new company record.

**Endpoint:** `POST /businesses/`

**Request Body (JSON):**

JSON

  

```perl
{
    "locationId": "YOUR_LOCATION_ID",
    "name": "Sample Company Name",
    "email": "contact@samplecompany.com",
    "phone": "+14155552671",
    "address": "123 Sample St"
}
```

To associate a contact with a company, use the update contact endpoint (`PUT /contacts/{contactId}`) and add the `businessId` field with the corresponding company ID.
