# Guias e Melhores Práticas (Guides & Best Practices)



# Exemplo Prático - Onboarding de um Novo Lead

### Exemplo Prático: Onboarding de um Novo Lead

Vamos unir vários endpoints para automatizar o processo de entrada de um novo lead que preencheu um formulário no seu site.

**Cenário:** Um usuário envia um formulário com nome, e-mail e interesse em "Serviços de Consultoria".

**Passo 1: Criar o Contato** Primeiro, pegamos os dados do formulário e criamos um novo contato.

*   **Requisição:** `POST /contacts/`
*   **Corpo (JSON):**JSON

  

```perl
{
    "locationId": "SEU_LOCATION_ID",
    "email": "lead.novo@example.com",
    "firstName": "Maria",
    "lastName": "Silva"
}
```

*   **Resultado:** A resposta da API nos dará o ID do novo contato. Vamos supor que seja `ID_DA_MARIA_SILVA`.

**Passo 2: Adicionar Tags ao Novo Contato** Agora, usamos o ID obtido para adicionar tags relevantes.

*   **Requisição:** `POST /contacts/ID_DA_MARIA_SILVA/tags`
*   **Corpo (JSON):**JSON

  

```plain
{
    "tags": ["novo-lead", "site-contato"]
}
```

**Passo 3: Criar uma Oportunidade no Pipeline de Vendas** Finalmente, criamos uma oportunidade para que a equipe de vendas possa dar seguimento.

*   **Requisição:** `POST /opportunities/`
*   **Corpo (JSON):**JSON

  

```json
{
    "locationId": "SEU_LOCATION_ID",
    "pipelineId": "ID_DO_SEU_PIPELINE_DE_VENDAS",
    "contactId": "ID_DA_MARIA_SILVA",
    "name": "Oportunidade - Maria Silva",
    "status": "open",
    "monetaryValue": 5000
}
```

**Conclusão:** Com três chamadas à API, nós registramos um novo lead, o segmentamos com tags e criamos uma tarefa para a equipe de vendas. Isso demonstra como você pode orquestrar diferentes recursos da API para criar automações poderosas.

* * *

### Practical Example: Onboarding a New Lead

Let's combine several endpoints to automate the onboarding process for a new lead who filled out a form on your website.

**Scenario:** A user submits a form with their name, email, and an interest in "Consulting Services."

**Step 1: Create the Contact** First, we take the form data and create a new contact.

*   **Request:** `POST /contacts/`
*   **Body (JSON):**JSON

  

```perl
{
    "locationId": "YOUR_LOCATION_ID",
    "email": "new.lead@example.com",
    "firstName": "John",
    "lastName": "Doe"
}
```

*   **Result:** The API response will give us the new contact's ID. Let's assume it's `JOHN_DOE_CONTACT_ID`.

**Step 2: Add Tags to the New Contact** Now, we use the ID we just received to add relevant tags.

*   **Request:** `POST /contacts/JOHN_DOE_CONTACT_ID/tags`
*   **Body (JSON):**JSON

  

```plain
{
    "tags": ["new-lead", "website-contact"]
}
```

**Step 3: Create an Opportunity in the Sales Pipeline** Finally, we create an opportunity so the sales team can follow up.

*   **Request:** `POST /opportunities/`
*   **Body (JSON):**JSON

  

```json
{
    "locationId": "YOUR_LOCATION_ID",
    "pipelineId": "YOUR_SALES_PIPELINE_ID",
    "contactId": "JOHN_DOE_CONTACT_ID",
    "name": "Opportunity - John Doe",
    "status": "open",
    "monetaryValue": 5000
}
```

**Conclusion:** With three API calls, we have registered a new lead, segmented them with tags, and created a task for the sales team. This demonstrates how you can orchestrate different API resources to build powerful automations.
