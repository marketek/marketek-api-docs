# Melhores Práticas para Webhooks

### Melhores Práticas para Webhooks

Além da validação de segurança, siga estas práticas para criar um sistema resiliente que recebe webhooks.

  

**1\. Responda Imediatamente** Sua aplicação deve responder à notificação do webhook com um código de sucesso (`200 OK`) o mais rápido possível (idealmente em menos de 2 segundos). Se a Marketek não receber uma resposta rápida, ela pode considerar a entrega como falha e tentar reenviar, causando duplicatas.

  

**2\. Processe os Dados de Forma Assíncrona** Não execute lógicas complexas ou demoradas antes de enviar a resposta `200 OK`. Em vez disso, receba o webhook, armazene seus dados em uma fila (como Redis, RabbitMQ ou um serviço de nuvem) e envie a resposta `200 OK`. Um processo separado (worker) deve então pegar os dados da fila e processá-los. Isso garante que você sempre responderá a tempo.

  

**3\. Lide com Requisições Duplicadas (Idempotência)** Em raras ocasiões (como falhas de rede), você pode receber o mesmo webhook mais de uma vez. Sua aplicação deve ser idempotente, ou seja, processar o mesmo evento múltiplas vezes deve ter o mesmo resultado que processá-lo uma única vez. Uma forma de fazer isso é registrar o ID de cada evento recebido e ignorar eventos cujos IDs você já processou.

* * *

### Webhook Best Practices

Beyond security validation, follow these practices to build a resilient system for receiving webhooks.

  

**1\. Respond Immediately** Your application should respond to the webhook notification with a success code (`200 OK`) as quickly as possible (ideally under 2 seconds). If Marketek does not receive a timely response, it may consider the delivery a failure and retry, causing duplicates.

  

**2\. Process Data Asynchronously** Do not perform complex or time-consuming logic before sending the `200 OK` response. Instead, receive the webhook, store its data in a queue (like Redis, RabbitMQ, or a cloud service), and then send the `200 OK` response. A separate process (a worker) should then pick up the data from the queue and process it. This ensures you always respond in time.

  

**3\. Handle Duplicate Requests (Idempotency)** On rare occasions (like network failures), you might receive the same webhook more than once. Your application should be idempotent, meaning that processing the same event multiple times has the same result as processing it once. A common way to achieve this is by logging the ID of each event received and skipping any events whose IDs you have already processed.
