# Agendamentos e Calendários

# ndpoints de Agendamentos e Calendários

Gerencie compromissos e eventos dos seus calendários da Marketek.

### Listar Agendamentos de um Calendário

Busque os eventos (compromissos) de um calendário específico dentro de um intervalo de datas.

**Endpoint:** `GET /calendars/{calendarId}/events`

**Parâmetros de Query Comuns:**

*   `startDate`: Data de início do período de busca (formato `YYYY-MM-DDTHH:mm:ssZ`).
*   `endDate`: Data de fim do período de busca (formato `YYYY-MM-DDTHH:mm:ssZ`).

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/calendars/ID_DO_CALENDARIO/events?startDate=2025-07-01T00:00:00-03:00&endDate=2025-07-31T23:59:59-03:00' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

### Criar um Novo Agendamento

Adicione um novo agendamento a um calendário para um contato existente.

**Endpoint:** `POST /calendars/{calendarId}/appointments`

**Corpo da Requisição (JSON):**

JSON

  

```json
{
    "contactId": "ID_DO_CONTATO",
    "startTime": "2025-08-15T14:00:00-03:00",
    "endTime": "2025-08-15T15:00:00-03:00",
    "title": "Reunião de Alinhamento",
    "appointmentStatus": "confirmed"
}
```

* * *

  

# Appointments & Calendars Endpoints

Manage appointments and events from your Marketek calendars.

### List Calendar Appointments

Fetch events (appointments) from a specific calendar within a date range.

**Endpoint:** `GET /calendars/{calendarId}/events`

**Common Query Parameters:**

*   `startDate`: The start date of the search period (format `YYYY-MM-DDTHH:mm:ssZ`).
*   `endDate`: The end date of the search period (format `YYYY-MM-DDTHH:mm:ssZ`).

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/calendars/CALENDAR_ID_HERE/events?startDate=2025-07-01T00:00:00-03:00&endDate=2025-07-31T23:59:59-03:00' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

### Create a New Appointment

Add a new appointment to a calendar for an existing contact.

**Endpoint:** `POST /calendars/{calendarId}/appointments`

**Request Body (JSON):**

JSON

  

```json
{
    "contactId": "CONTACT_ID_HERE",
    "startTime": "2025-08-15T14:00:00-03:00",
    "endTime": "2025-08-15T15:00:00-03:00",
    "title": "Alignment Meeting",
    "appointmentStatus": "confirmed"
}
```
