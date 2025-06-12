# Webhooks

Os Webhooks permitem que a Marketek envie notificações em tempo real para sua aplicação sempre que um evento específico ocorrer, eliminando a necessidade de consultar a API repetidamente.

### Tipos de Webhooks

*   **Webhooks de Saída (Outgoing):** A Marketek notifica seu sistema sobre um evento (ex: `ContatoCriado`).
*   **Webhooks de Entrada (Incoming):** Seu sistema envia dados para uma URL de um Workflow da Marketek para iniciar uma automação.

### Segurança e Validação

É **essencial** que sua aplicação valide se as notificações de webhook recebidas são genuinamente da Marketek.

Nossa plataforma usa um método de assinatura **RSA-SHA256** para garantir a autenticidade. Cada notificação de webhook de saída inclui um cabeçalho especial:

*   **Cabeçalho:** `x-wh-signature`

Sua aplicação deve usar a chave pública da Lead-Connector para verificar se a assinatura no cabeçalho corresponde ao corpo (payload) da requisição. Se a verificação falhar, a requisição deve ser descartada.

Para um guia detalhado sobre a implementação da validação, consulte a documentação de referência sobre **Webhook Authentication**.

### Eventos Comuns

Você pode se inscrever para receber notificações de dezenas de eventos, incluindo:

*   `ContactCreate`: Um novo contato é criado.
*   `ContactDelete`: Um contato é excluído.
*   `ContactDndUpdate`: As preferências de "Não Perturbe" de um contato são atualizadas.
*   `AppointmentCreate`: Um novo agendamento é criado.
*   `OpportunityCreate`: Uma nova oportunidade é criada.
*   `OpportunityStageUpdate`: Uma oportunidade é movida para um novo estágio.
*   `InvoicePaid`: Uma fatura é paga.

  

* * *

  

# Webhooks

Webhooks allow Marketek to send real-time notifications to your application whenever a specific event occurs, eliminating the need to poll the API repeatedly.

### Types of Webhooks

*   **Outgoing Webhooks:** Marketek notifies your system about an event (e.g., `ContactCreate`).
*   **Incoming Webhooks:** Your system sends data to a Marketek Workflow URL to trigger an automation.

### Security and Validation

It is **essential** that your application validates that incoming webhook notifications are genuinely from Marketek.

Our platform uses an **RSA-SHA256** signature method to ensure authenticity. Each outgoing webhook notification includes a special header:

*   **Header:** `x-wh-signature`

Your application must use the Lead-Connector public key to verify that the signature in the header matches the request's payload. If the verification fails, the request should be discarded.

For a detailed guide on implementing this validation, please refer to the reference documentation on **Webhook Authentication**.

### Common Events

You can subscribe to receive notifications for dozens of events, including:

*   `ContactCreate`: A new contact is created.
*   `ContactDelete`: A contact is deleted.
*   `ContactDndUpdate`: A contact's "Do Not Disturb" preferences are updated.
*   `AppointmentCreate`: A new appointment is created.
*   `OpportunityCreate`: A new opportunity is created.
*   `OpportunityStageUpdate`: An opportunity is moved to a new stage.
*   `InvoicePaid`: An invoice is paid.
