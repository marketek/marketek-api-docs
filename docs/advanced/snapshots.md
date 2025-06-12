### Snapshots

Um Snapshot é um "modelo" ou um "template" completo de uma subconta Marketek. Ele inclui tudo, desde pipelines e campos personalizados até workflows e campanhas.

**Caso de Uso Principal**

Snapshots são uma ferramenta poderosa para agências, permitindo padronizar e implantar rapidamente novas contas de clientes com todas as configurações, funis e automações já pré-construídas. **Esta é uma funcionalidade de nível de agência.**

**Listar Snapshots Disponíveis**

Recupere uma lista de todos os snapshots disponíveis para a sua agência.

*   **Endpoint:** `GET /snapshots/`
*   **Autenticação:** Requer uma Chave de API de nível de **Agência**.

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/snapshots/' \
--header 'Authorization: Bearer SUA_CHAVE_API_DE_AGENCIA' \
--header 'Version: 2021-07-28'
```

A resposta incluirá um array `snapshots` com os detalhes de cada um, incluindo seu `id` e `name`.

* * *

### Snapshots

A Snapshot is a complete "template" or "model" of a Marketek sub-account. It includes everything from pipelines and custom fields to workflows and campaigns.

**Primary Use Case**

Snapshots are a powerful tool for agencies, allowing them to standardize and quickly deploy new client accounts with all settings, funnels, and automations already pre-built. **This is an agency-level feature.**

**List Available Snapshots**

Retrieve a list of all snapshots available to your agency.

*   **Endpoint:** `GET /snapshots/`
*   **Authentication:** Requires an **Agency** level API Key.

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/snapshots/' \
--header 'Authorization: Bearer YOUR_AGENCY_API_KEY' \
--header 'Version: 2021-07-28'
```

The response will include a `snapshots` array with the details of each snapshot, including its `id` and `name`.
