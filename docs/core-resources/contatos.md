# Contatos

# Endpoint Essencial: Criar um Contato

Um dos casos de uso mais comuns é a criação de um novo contato na sua subconta da Marketek.

### Requisição

Para criar um contato, envie uma requisição do tipo `POST` para o endpoint `/contacts/`.

**Endpoint:** `POST /contacts/`

**Corpo da Requisição (Payload):** O corpo da requisição deve ser um objeto JSON contendo as informações do contato. O campo `locationId` é obrigatório, e você pode incluir outros campos como `email`, `firstName`, `tags`, etc.

**Exemplo Completo (cURL):**

Bash

  

```plain
curl --location --request POST 'https://services.leadconnectorhq.com/contacts/' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28' \
--header 'Content-Type: application/json' \
--data-raw '{
    "locationId": "SEU_LOCATION_ID",
    "email": "novo.contato.api@example.com",
    "firstName": "Novo",
    "lastName": "Contato",
    "tags": ["lead-via-api", "importado-2025"]
}'
```

Uma resposta de sucesso retornará um status `201 Created` e os dados do contato recém-criado no campo `data`.

  

* * *

  

# Core Endpoint: Create a Contact

One of the most common use cases is creating a new contact in your Marketek sub-account.

### Request

To create a contact, send a `POST` request to the `/contacts/` endpoint.

**Endpoint:** `POST /contacts/`

**Request Body (Payload):** The request body must be a JSON object containing the contact's information. The `locationId` field is required, and you can include other fields like `email`, `firstName`, `tags`, etc.

**Complete Example (cURL):**

Bash

  

```plain
curl --location --request POST 'https://services.leadconnectorhq.com/contacts/' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28' \
--header 'Content-Type: application/json' \
--data-raw '{
    "locationId": "YOUR_LOCATION_ID",
    "email": "new.contact.api@example.com",
    "firstName": "New",
    "lastName": "Contact",
    "tags": ["lead-via-api", "imported-2025"]
}'
```

A successful response will return a `201 Created` status and the newly created contact's data in the `data` field.

