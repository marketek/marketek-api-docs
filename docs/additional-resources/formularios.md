# Formulários

# Endpoints de Formulários

Recupere dados de submissões dos seus formulários Marketek para processá-los em sistemas externos, planilhas ou bancos de dados.

### Listar Submissões de Formulários

Obtenha uma lista de todas as submissões para um formulário específico.

**Endpoint:** `GET /forms/submissions`

**Parâmetros de Query:**

*   `locationId` (obrigatório): O ID da sua subconta.
*   `formId` (obrigatório): O ID do formulário do qual você quer as submissões.
*   `limit` (opcional): Número de submissões a serem retornadas (padrão 20).

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/forms/submissions?locationId=SEU_LOCATION_ID&formId=ID_DO_FORMULARIO' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

A resposta incluirá um array `submissions` contendo os dados de cada submissão, incluindo as informações do contato e os campos preenchidos.

  

* * *

  

# Forms Endpoints

Retrieve submission data from your Marketek forms to process it in external systems, spreadsheets, or databases.

### List Form Submissions

Get a list of all submissions for a specific form.

**Endpoint:** `GET /forms/submissions`

**Query Parameters:**

*   `locationId` (required): Your sub-account's ID.
*   `formId` (required): The ID of the form from which you want the submissions.
*   `limit` (optional): The number of submissions to return (default is 20).

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/forms/submissions?locationId=YOUR_LOCATION_ID&formId=FORM_ID_HERE' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

The response will include a `submissions` array containing the data for each submission, including contact information and the filled-out fields.
