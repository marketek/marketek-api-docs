# Agendador Social (Social Planner)

### Agendador Social (Social Planner)

A API do Agendador Social permite que você crie, agende e gerencie postagens de mídia social para as contas conectadas à sua localização Marketek.

**Criar uma Postagem Social**

Crie uma nova postagem para ser publicada em uma ou mais redes sociais.

*   **Endpoint:** `POST /social-planner/posts`
*   **Corpo da Requisição (JSON):**JSON
*   

```plain
{
    "locationId": "SEU_LOCATION_ID",
    "accountIds": [
        "ID_DA_CONTA_FACEBOOK",
        "ID_DA_CONTA_INSTAGRAM"
    ],
    "post": "Este é o texto da minha nova postagem, criada via API!",
    "postDate": "2025-09-22T15:00:00Z"
}
```

**Nota:** O `postDate` especifica quando a postagem deve ser publicada. Se omitido, a postagem é feita imediatamente.

* * *

### Social Planner

The Social Planner API allows you to create, schedule, and manage social media posts for the accounts connected to your Marketek location.

**Create a Social Post**

Create a new post to be published on one or more social networks.

*   **Endpoint:** `POST /social-planner/posts`
*   **Request Body (JSON):**JSON
*   

```plain
{
    "locationId": "YOUR_LOCATION_ID",
    "accountIds": [
        "FACEBOOK_ACCOUNT_ID",
        "INSTAGRAM_ACCOUNT_ID"
    ],
    "post": "This is the text of my new post, created via the API!",
    "postDate": "2025-09-22T15:00:00Z"
}
```

**Note:** The `postDate` specifies when the post should be published. If omitted, the post is published immediately.
