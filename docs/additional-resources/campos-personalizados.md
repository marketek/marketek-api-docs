# Campos Personalizados

# Endpoints de Campos Personalizados

Campos personalizados permitem que você armazene informações únicas sobre seus contatos. Você pode gerenciá-los e atualizá-los via API.

### Listar Campos Personalizados

Para atualizar um campo, primeiro você precisa saber seu ID. Use este endpoint para listar todos os campos personalizados disponíveis em sua subconta.

**Endpoint:** `GET /locations/{locationId}/customFields`

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/locations/SEU_LOCATION_ID/customFields' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

A resposta conterá um array `customFields` com os detalhes de cada campo, incluindo seu `id` e `name`.

### Atualizar o Valor de um Campo Personalizado

A atualização do valor de um campo personalizado para um contato é feita através do endpoint de **Atualização de Contato**.

**Endpoint de Referência:** `PUT /contacts/{contactId}`

No corpo da requisição, inclua o array `customFields` com o `id` do campo que você quer atualizar e seu novo `field_value`.

**Exemplo de Corpo da Requisição (JSON):**

JSON

  

```plain
{
    "customFields": [
        {
            "id": "ID_DO_CAMPO_PERSONALIZADO",
            "field_value": "Novo Valor a ser Salvo"
        }
    ]
}
```

  

* * *

  

# Custom Fields Endpoints

Custom fields allow you to store unique information about your contacts. You can manage and update them via the API.

### List Custom Fields

To update a field, you first need to know its ID. Use this endpoint to list all available custom fields in your sub-account.

**Endpoint:** `GET /locations/{locationId}/customFields`

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/locations/YOUR_LOCATION_ID/customFields' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

The response will contain a `customFields` array with the details of each field, including its `id` and `name`.

### Update a Custom Field's Value

Updating a custom field's value for a contact is done via the **Update Contact** endpoint.

**Reference Endpoint:** `PUT /contacts/{contactId}`

In the request body, include the `customFields` array with the `id` of the field you want to update and its new `field_value`.

**Example Request Body (JSON):**

JSON

  

```plain
{
    "customFields": [
        {
            "id": "CUSTOM_FIELD_ID_HERE",
            "field_value": "New Value to be Saved"
        }
    ]
}
```
