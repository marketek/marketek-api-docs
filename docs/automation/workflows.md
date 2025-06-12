# Workflows (Automações)

# Endpoints de Workflows

Integre suas aplicações com o poderoso motor de automação da Marketek. A ação mais comum é adicionar um contato a um workflow para iniciar uma sequência de ações.

### Adicionar Contato a um Workflow

Matricule programaticamente um contato em um workflow específico.

**Endpoint:** `POST /workflows/{workflowId}/enroll`

**Parâmetros na URL:**

*   `workflowId` (obrigatório): O ID do workflow no qual o contato será matriculado.

**Corpo da Requisição (JSON):** O corpo da requisição precisa apenas do ID do contato.

JSON

  

```json
{
    "contactId": "ID_DO_CONTATO_A_SER_ADICIONADO"
}
```

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request POST 'https://services.leadconnectorhq.com/workflows/ID_DO_WORKFLOW/enroll' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28' \
--header 'Content-Type: application/json' \
--data-raw '{
    "contactId": "ID_DO_CONTATO_A_SER_ADICIONADO"
}'
```

  

* * *

# Workflows Endpoints

Integrate your applications with Marketek's powerful automation engine. The most common action is to add a contact to a workflow to start a sequence of actions.

### Add Contact to a Workflow

Programmatically enroll a contact into a specific workflow.

**Endpoint:** `POST /workflows/{workflowId}/enroll`

**Parameters in URL:**

*   `workflowId` (required): The ID of the workflow in which the contact will be enrolled.

**Request Body (JSON):** The request body only needs the contact's ID.

JSON

  

```json
{
    "contactId": "CONTACT_ID_TO_BE_ENROLLED"
}
```

**Example (cURL):**

Bash

  

```dsconfig
curl --location --request POST 'https://services.leadconnectorhq.com/workflows/WORKFLOW_ID_HERE/enroll' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28' \
--header 'Content-Type: application/json' \
--data-raw '{
    "contactId": "CONTACT_ID_TO_BE_ENROLLED"
}'
```
