# Tratamento de Erros e Limites

### Tratamento de Erros e Limites de Taxa

Para construir uma integração robusta, é crucial entender como lidar com os limites da API e os possíveis erros.

**Limites de Taxa (Rate Limits)**

Para garantir a estabilidade para todos os usuários, a API da Marketek limita o número de requisições que você pode fazer em um determinado período.

*   **Limite:** 100 requisições a cada 10 segundos por localização.
*   **Código de Resposta:** Se você exceder este limite, a API responderá com o código de status `429 Too Many Requests`.
*   **Cabeçalhos de Monitoramento:** A resposta da API inclui cabeçalhos `X-RateLimit-*` que informam seu limite total (`X-RateLimit-Max`) e quantas requisições ainda restam (`X-RateLimit-Remaining`) no intervalo atual. Monitore esses cabeçalhos para gerenciar sua taxa de chamadas.

**Códigos de Erro Comuns**

*   `2xx - Sucesso`: Sua requisição foi bem-sucedida.
    *   `200 OK`: Requisição bem-sucedida.
    *   `201 Created`: Recurso criado com sucesso.
*   `4xx - Erro do Cliente`: Houve um problema com a sua requisição.
    *   `400 Bad Request`: A requisição está malformada (ex: JSON inválido, campo obrigatório ausente). A resposta geralmente contém detalhes sobre o erro.
    *   `401 Unauthorized`: Sua Chave de API está ausente, inválida ou expirada.
    *   `403 Forbidden`: Você não tem permissão para acessar este recurso.
    *   `404 Not Found`: O recurso ou endpoint solicitado não existe.
*   `5xx - Erro do Servidor`: Ocorreu um problema em nossos servidores. Se este erro persistir, entre em contato com o suporte.

**Melhor Prática:** Sua aplicação deve sempre verificar o código de status da resposta e, para erros `429` e `5xx`, implementar uma estratégia de retentativa com um tempo de espera crescente (backoff exponencial).

* * *

### Error Handling & Rate Limits

To build a robust integration, it is crucial to understand how to handle API limits and potential errors.

**Rate Limits**

To ensure stability for all users, the Marketek API limits the number of requests you can make in a given period.

*   **Limit:** 100 requests per 10 seconds per location.
*   **Response Code:** If you exceed this limit, the API will respond with a `429 Too Many Requests` status code.
*   **Monitoring Headers:** The API response includes `X-RateLimit-*` headers that inform you of your total limit (`X-RateLimit-Max`) and how many requests remain (`X-RateLimit-Remaining`) in the current window. Monitor these headers to manage your call rate.

**Common Error Codes**

*   `2xx - Success`: Your request was successful.
    *   `200 OK`: Request successful.
    *   `201 Created`: Resource successfully created.
*   `4xx - Client Error`: There was a problem with your request.
    *   `400 Bad Request`: The request is malformed (e.g., invalid JSON, missing required field). The response body usually contains details about the error.
    *   `401 Unauthorized`: Your API Key is missing, invalid, or expired.
    *   `403 Forbidden`: You do not have permission to access this resource.
    *   `404 Not Found`: The requested resource or endpoint does not exist.
*   `5xx - Server Error`: An issue occurred on our servers. If this error persists, please contact support.

**Best Practice:** Your application should always check the response status code and, for `429` and `5xx` errors, implement a retry strategy with an increasing wait time (exponential backoff).

# Recursos Principais (Core Resources)
