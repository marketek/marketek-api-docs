# Visão Geral de OAuth 2.0

Enquanto a autenticação por Chave de API é ideal para integrações privadas, o **OAuth 2.0** é o padrão utilizado para construir aplicativos públicos que outros usuários da Marketek podem instalar e usar.

### Quando Usar OAuth 2.0?

Você deve usar o fluxo OAuth 2.0 se estiver construindo um aplicativo que:

*   Será listado em uma Marketplace.
*   Precisa acessar os dados de múltiplas contas de usuários da Marketek de forma segura.
*   Requer que os usuários concedam permissão explícita para que seu aplicativo acesse seus dados, sem nunca compartilhar suas Chaves de API diretamente com você.

### Como Funciona (Fluxo Simplificado)

1. **Redirecionamento para Autorização:** Sua aplicação redireciona o usuário para uma página de autorização da Marketek.
2. **Consentimento do Usuário:** O usuário faz login em sua conta Marketek e vê quais permissões (escopos) seu aplicativo está solicitando. Ele então aprova ou nega o acesso.
3. **Código de Autorização:** Após a aprovação, o usuário é redirecionado de volta para sua aplicação com um `código` temporário.
4. **Troca pelo Access Token:** O backend da sua aplicação usa esse `código` para fazer uma chamada segura à API da Marketek e trocá-lo por um `access_token` e um `refresh_token`.
5. **Acesso Autorizado:** Sua aplicação pode agora usar o `access_token` para fazer chamadas à API em nome do usuário, respeitando as permissões que ele concedeu.

Este é um tópico avançado. Para detalhes técnicos de implementação, consulte as seções "OAuth 2.0" e "Authorization" na documentação de referência da Lead-Connector.

  

* * *

# OAuth 2.0 Overview

While API Key authentication is ideal for private integrations, **OAuth 2.0** is the standard used for building public applications that other Marketek users can install and use.

### When to Use OAuth 2.0

You should use the OAuth 2.0 flow if you are building an application that:

*   Will be listed in a Marketplace.
*   Needs to access the data of multiple Marketek user accounts securely.
*   Requires users to grant explicit permission for your app to access their data, without ever sharing their API Keys directly with you.

### How It Works (Simplified Flow)

1. **Redirect to Authorize:** Your application redirects the user to a Marketek authorization page.
2. **User Consent:** The user logs into their Marketek account and sees which permissions (scopes) your app is requesting. They then approve or deny access.
3. **Authorization Code:** After approval, the user is redirected back to your application with a temporary `code`.
4. **Exchange for Access Token:** Your application's backend uses this `code` to make a secure call to the Marketek API and exchanges it for an `access_token` and a `refresh_token`.
5. **Authorized Access:** Your application can now use the `access_token` to make API calls on behalf of the user, respecting the permissions they granted.

This is an advanced topic. For technical implementation details, please refer to the "OAuth 2.0" and "Authorization" sections in the Lead-Connector reference documentation.
