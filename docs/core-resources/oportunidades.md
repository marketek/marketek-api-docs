# Oportunidades

# Endpoints de Oportunidades

As oportunidades representam negócios ou acordos em andamento em seus pipelines de vendas. A API permite que você gerencie essas oportunidades programaticamente.

### Listar Oportunidades

Recupere uma lista de oportunidades de um pipeline específico ou de toda a sua localização.

**Endpoint:** `GET /opportunities/search`

**Parâmetros de Query Comuns:**

*   `locationId` (obrigatório): O ID da sua subconta.
*   `pipelineId` (opcional): Filtra oportunidades de um pipeline específico.
*   `status` (opcional): Filtra por status (`open`, `won`, `lost`, `abandoned`).

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/opportunities/search?locationId=SEU_LOCATION_ID&status=open' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

### Criar uma Oportunidade

Crie uma nova oportunidade em um pipeline.

**Endpoint:** `POST /opportunities/`

**Corpo da Requisição (JSON):**

JSON

  

```json
{
    "locationId": "SEU_LOCATION_ID",
    "pipelineId": "ID_DO_PIPELINE",
    "contactId": "ID_DO_CONTATO",
    "name": "Novo Negócio via API",
    "status": "open",
    "monetaryValue": 2500.50
}
```

### Atualizar uma Oportunidade

Modifique uma oportunidade existente, como mover para um novo estágio ou alterar seu valor.

**Endpoint:** `PUT /opportunities/{opportunityId}`

**Exemplo de Corpo da Requisição (JSON) para mover um estágio:**

JSON

  

```json
{
    "pipelineStageId": "ID_DO_NOVO_ESTAGIO",
    "status": "open"
}
```

* * *

  

# Opportunities Endpoints

Opportunities represent ongoing deals or agreements in your sales pipelines. The API allows you to manage these opportunities programmatically.

### List Opportunities

Retrieve a list of opportunities from a specific pipeline or your entire location.

**Endpoint:** `GET /opportunities/search`

**Common Query Parameters:**

*   `locationId` (required): Your sub-account's ID.
*   `pipelineId` (optional): Filters opportunities from a specific pipeline.
*   `status` (optional): Filters by status (`open`, `won`, `lost`, `abandoned`).

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/opportunities/search?locationId=YOUR_LOCATION_ID&status=open' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

### Create an Opportunity

Create a new opportunity in a pipeline.

**Endpoint:** `POST /opportunities/`

**Request Body (JSON):**

JSON

  

```json
{
    "locationId": "YOUR_LOCATION_ID",
    "pipelineId": "PIPELINE_ID_HERE",
    "contactId": "CONTACT_ID_HERE",
    "name": "New Deal via API",
    "status": "open",
    "monetaryValue": 2500.50
}
```

### Update an Opportunity

Modify an existing opportunity, such as moving it to a new stage or changing its value.

**Endpoint:** `PUT /opportunities/{opportunityId}`

**Example Request Body (JSON) to move a stage:**

JSON

  

```json
{
    "pipelineStageId": "ID_OF_THE_NEW_STAGE",
    "status": "open"
}
```

* * *
