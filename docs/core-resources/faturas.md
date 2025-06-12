# Faturas (Invoices)

# Endpoints de Faturas

Crie e gerencie faturas para seus contatos diretamente via API, integrando seu sistema de faturamento com a Marketek.

### Listar Faturas

Obtenha uma lista de faturas, com a possibilidade de filtrar por contato ou status.

**Endpoint:** `GET /invoices/`

**Parâmetros de Query:**

*   `locationId` (obrigatório): O ID da sua subconta.
*   `contactId` (opcional): Filtra faturas de um contato específico.
*   `status` (opcional): Filtra por status (`draft`, `open`, `paid`, `void`, `uncollectible`).

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/invoices/?locationId=SEU_LOCATION_ID&status=paid' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

### Criar uma Fatura

Gere uma nova fatura em modo rascunho (`draft`) ou aberta (`open`).

**Endpoint:** `POST /invoices/`

**Corpo da Requisição (JSON):**

JSON

  

```plain
{
    "locationId": "SEU_LOCATION_ID",
    "contactId": "ID_DO_CONTATO",
    "status": "draft",
    "invoiceItems": [
        {
            "description": "Serviço de Consultoria",
            "quantity": 1,
            "unitAmount": 1500
        },
        {
            "description": "Taxa de Instalação",
            "quantity": 1,
            "unitAmount": 250
        }
    ]
}
```

  

* * *

  

# Invoices Endpoints

Create and manage invoices for your contacts directly via the API, integrating your billing system with Marketek.

### List Invoices

Get a list of invoices, with the ability to filter by contact or status.

**Endpoint:** `GET /invoices/`

**Query Parameters:**

*   `locationId` (required): Your sub-account's ID.
*   `contactId` (optional): Filters invoices for a specific contact.
*   `status` (optional): Filters by status (`draft`, `open`, `paid`, `void`, `uncollectible`).

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/invoices/?locationId=YOUR_LOCATION_ID&status=paid' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

### Create an Invoice

Generate a new invoice in either `draft` or `open` status.

**Endpoint:** `POST /invoices/`

**Request Body (JSON):**

JSON

  

```plain
{
    "locationId": "YOUR_LOCATION_ID",
    "contactId": "CONTACT_ID_HERE",
    "status": "draft",
    "invoiceItems": [
        {
            "description": "Consulting Service",
            "quantity": 1,
            "unitAmount": 1500
        },
        {
            "description": "Setup Fee",
            "quantity": 1,
            "unitAmount": 250
        }
    ]
}
```
