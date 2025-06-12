# Conversas

# Endpoints de Conversas

A API de Conversas permite que você interaja com os canais de comunicação da Marketek, como SMS e E-mail, diretamente de suas aplicações.

### Enviar uma Mensagem

Envie uma mensagem de texto (SMS) ou um e-mail para um contato específico.

**Endpoint:** `POST /conversations/messages`

**Corpo da Requisição (JSON) para um SMS:**

JSON

  

```json
{
    "locationId": "SEU_LOCATION_ID",
    "contactId": "ID_DO_CONTATO",
    "type": "SMS",
    "message": "Olá! Este é um lembrete sobre o seu agendamento de amanhã."
}
```

**Corpo da Requisição (JSON) para um E-mail:**

JSON

  

```json
{
    "locationId": "SEU_LOCATION_ID",
    "contactId": "ID_DO_CONTATO",
    "type": "Email",
    "subject": "Confirmação do seu Pedido",
    "html": "<h1>Pedido Confirmado</h1><p>Obrigado por sua compra! Seu pedido nº 12345 está sendo processado.</p>"
}
```

### Listar Mensagens de uma Conversa

Recupere o histórico de mensagens trocadas com um contato.

**Endpoint:** `GET /conversations/messages`

**Parâmetros de Query:**

*   `locationId` (obrigatório): O ID da sua subconta.
*   `contactId` (obrigatório): O ID do contato cujo histórico você deseja ver.

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/conversations/messages?locationId=SEU_LOCATION_ID&contactId=ID_DO_CONTATO' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

  

* * *

# Conversations Endpoints

The Conversations API allows you to interact with Marketek's communication channels, such as SMS and Email, directly from your applications.

### Send a Message

Send a text message (SMS) or an email to a specific contact.

**Endpoint:** `POST /conversations/messages`

**Request Body (JSON) for an SMS:**

JSON

  

```smalltalk
{
    "locationId": "YOUR_LOCATION_ID",
    "contactId": "CONTACT_ID_HERE",
    "type": "SMS",
    "message": "Hello! This is a reminder about your appointment tomorrow."
}
```

**Request Body (JSON) for an Email:**

JSON

  

```smalltalk
{
    "locationId": "YOUR_LOCATION_ID",
    "contactId": "CONTACT_ID_HERE",
    "type": "Email",
    "subject": "Your Order Confirmation",
    "html": "<h1>Order Confirmed</h1><p>Thank you for your purchase! Your order #12345 is being processed.</p>"
}
```

### List Messages in a Conversation

Retrieve the history of messages exchanged with a contact.

**Endpoint:** `GET /conversations/messages`

**Query Parameters:**

*   `locationId` (required): Your sub-account's ID.
*   `contactId` (required): The ID of the contact whose history you want to view.

**Example (cURL):**

Bash

  

```dsconfig
curl --location --request GET 'https://services.leadconnectorhq.com/conversations/messages?locationId=YOUR_LOCATION_ID&contactId=CONTACT_ID_HERE' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

