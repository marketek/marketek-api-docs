# Usuários

# Endpoints de Usuários

A API de Usuários permite gerenciar as contas dos membros da sua equipe dentro de uma localização (subconta) específica.

### Listar Usuários

Recupere uma lista de todos os usuários associados à sua localização.

**Endpoint:** `GET /users/search`

**Parâmetros de Query:**

*   `locationId` (obrigatório): O ID da sua subconta.

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/users/search?locationId=SEU_LOCATION_ID' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

A resposta incluirá um array `users` com os detalhes de cada um, incluindo seus papéis e permissões.

### Criar um Usuário

Adicione um novo usuário à sua localização.

**Endpoint:** `POST /users/`

**Corpo da Requisição (JSON):**

JSON

  

```json
{
    "locationId": "SEU_LOCATION_ID",
    "name": "Nome do Novo Usuário",
    "email": "email.novo@exemplo.com",
    "role": "user",
    "permissions": {
        "campaigns_read_only": true,
        "contacts_read_only": true
    }
}
```

**Nota:** As permissões (`permissions`) são um objeto detalhado onde você pode especificar o nível de acesso para cada funcionalidade. Consulte a documentação de referência para a lista completa de permissões.

  

* * *

# Users Endpoints

The Users API allows you to manage your team members' accounts within a specific location (sub-account).

### List Users

Retrieve a list of all users associated with your location.

**Endpoint:** `GET /users/search`

**Query Parameters:**

*   `locationId` (required): Your sub-account's ID.

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/users/search?locationId=YOUR_LOCATION_ID' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

The response will include a `users` array with the details of each user, including their roles and permissions.

### Create a User

Add a new user to your location.

**Endpoint:** `POST /users/`

**Request Body (JSON):**

JSON

  

```json
{
    "locationId": "YOUR_LOCATION_ID",
    "name": "New User Name",
    "email": "new.user@example.com",
    "role": "user",
    "permissions": {
        "campaigns_read_only": true,
        "contacts_read_only": true
    }
}
```

**Note:** The `permissions` object is detailed, allowing you to specify the access level for each feature. Please refer to the reference documentation for a complete list of permissions.
