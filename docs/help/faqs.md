### Perguntas Frequentes (FAQs)

**P: Qual chave de API devo usar?R:** Para integrações dentro da sua própria conta, use a Chave de API de Localização (Subconta) encontrada em `Configurações > Informações da Empresa`. Para gerenciar múltiplas subcontas ou usar funcionalidades de agência (como Snapshots ou SaaS), você precisará de uma Chave de API de Agência.

  

**P: Recebi um erro** **`429 Too Many Requests`****. O que faço?R:** Você excedeu o limite de 100 requisições a cada 10 segundos. Sua aplicação deve pausar e tentar novamente após um curto período de espera. A melhor prática é implementar uma lógica de "backoff exponencial", aumentando o tempo de espera a cada nova tentativa. Monitore os cabeçalhos `X-RateLimit-*` para evitar o erro.

  

**P: Por que a validação do meu Webhook está falhando?R:** A validação de Webhooks da Marketek usa uma assinatura RSA-SHA256, que é mais segura que métodos comuns. Verifique os seguintes pontos: 1) Você está usando o corpo (payload) bruto da requisição para a verificação, sem modificá-lo? 2) Você está usando a chave pública correta da Lead-Connector? 3) Sua biblioteca de criptografia está configurada corretamente?

  

**P: Como posso testar a API sem afetar meus dados reais?R:** A melhor maneira de testar é criar uma subconta de "Teste" ou "Sandbox" dentro da sua agência. Use a Chave de API desta subconta de teste para todo o seu desenvolvimento, garantindo que seus dados de produção permaneçam intactos.

* * *

### Frequently Asked Questions (FAQs)

**Q: Which API key should I use?A:** For integrations within your own account, use the Location (Sub-account) API Key found under `Settings > Business Info`. To manage multiple sub-accounts or use agency features (like Snapshots or SaaS), you will need an Agency API Key.

  

**Q: I received a** **`429 Too Many Requests`** **error. What should I do?A:** You have exceeded the limit of 100 requests per 10 seconds. Your application should pause and retry after a short delay. The best practice is to implement an "exponential backoff" strategy, increasing the wait time with each failed attempt. Monitor the `X-RateLimit-*` headers to avoid this error.

  

**Q: Why is my Webhook validation failing?A:** Marketek's Webhook validation uses an RSA-SHA256 signature, which is more secure than common methods. Check the following: 1) Are you using the raw request body for the verification, without modifying it? 2) Are you using the correct Lead-Connector public key? 3) Is your cryptography library configured correctly?

  

**Q: How can I test the API without affecting my real data?A:** The best way to test is to create a dedicated "Test" or "Sandbox" sub-account within your agency. Use the API Key from this test sub-account for all your development, ensuring your production data remains untouched.
