# Tags

### Tags

Tags são essenciais para segmentar e organizar seus contatos. A API permite que você adicione e remova tags de um contato de forma programática.

**Adicionar Tags a um Contato**

Aplique uma ou mais tags a um contato existente. Se a tag não existir na localização, ela será criada.

*   **Endpoint:** `POST /contacts/{contactId}/tags`
*   **Corpo da Requisição (JSON):** Um array com os nomes das tags. JSON
*   

```plain
{
    "tags": [
        "lead-qualificado",
        "webinar-2025"
    ]
}
```

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request POST 'https://services.leadconnectorhq.com/contacts/ID_DO_CONTATO/tags' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28' \
--header 'Content-Type: application/json' \
--data-raw '{
    "tags": ["lead-qualificado"]
}'
```

**Remover Tags de um Contato**

Remova uma ou more tags de um contato.

*   **Endpoint:** `DELETE /contacts/{contactId}/tags`
*   **Corpo da Requisição (JSON):** Um array com os nomes das tags a serem removidas.

* * *

### Tags

Tags are essential for segmenting and organizing your contacts. The API allows you to programmatically add and remove tags from a contact.

**Add Tags to a Contact**

Apply one or more tags to an existing contact. If the tag does not exist in the location, it will be created.

*   **Endpoint:** `POST /contacts/{contactId}/tags`
*   **Request Body (JSON):** An array with the names of the tags. JSON
*   

```plain
{
    "tags": [
        "qualified-lead",
        "webinar-2025"
    ]
}
```

**Example (cURL):**

Bash

  

```plain
curl --location --request POST 'https://services.leadconnectorhq.com/contacts/CONTACT_ID_HERE/tags' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28' \
--header 'Content-Type: application/json' \
--data-raw '{
    "tags": ["qualified-lead"]
}'
```

**Remove Tags from a Contact**

Remove one or more tags from a contact.

*   **Endpoint:** `DELETE /contacts/{contactId}/tags`
*   **Request Body (JSON):** An array with the names of the tags to be removed.

# Recursos Adicionais (Additional Resources)

You don't have access to this Doc

