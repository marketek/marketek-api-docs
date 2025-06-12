# Changelog e Política de Versionamento

### Changelog e Política de Versionamento

Nosso objetivo é manter uma API estável, mas também evoluir e adicionar novas funcionalidades. Esta página descreve como gerenciamos as mudanças.

**Versionamento via Cabeçalho**

Nós usamos um cabeçalho de versionamento (`Version: 2021-07-28`) para garantir que suas integrações existentes não quebrem quando introduzirmos atualizações. Você deve **sempre** incluir este cabeçalho em suas requisições para travar sua implementação em uma versão específica da API.

**Tipos de Mudanças**

*   **Não Quebráveis (Non-Breaking):** Adição de novos endpoints, novos campos opcionais em requisições existentes ou novos campos em respostas. Essas mudanças são aplicadas e podem ser usadas por todos, independentemente da versão.
*   **Quebráveis (Breaking):** Remoção de um campo, alteração do tipo de um campo ou modificação de um endpoint existente de forma que não seja retrocompatível. Essas mudanças só ocorrerão em novas versões da API (identificadas por uma nova data).

**Changelog (Histórico de Mudanças)**

Todas as mudanças na API serão documentadas aqui.

*   **\[Data da Próxima Mudança\]** - \[Descrição da mudança. Ex: Adicionado o endpoint `GET /surveys/` para listar pesquisas.\]
*   **\[Data da Mudança Anterior\]** - \[Descrição da mudança.\]

* * *

### Changelog & Versioning Policy

Our goal is to maintain a stable API while also evolving and adding new features. This page describes how we manage changes.

**Versioning via Header**

We use a versioning header (`Version: 2021-07-28`) to ensure that your existing integrations do not break when we introduce updates. You should **always** include this header in your requests to lock your implementation to a specific API version.

**Types of Changes**

*   **Non-Breaking Changes:** Adding new endpoints, new optional fields in existing requests, or new fields in responses. These changes are applied and can be used by everyone, regardless of the version.
*   **Breaking Changes:** Removing a field, changing a field's type, or modifying an existing endpoint in a way that is not backward-compatible. These changes will only occur in new API versions (identified by a new date).

**Changelog**

All API changes will be documented here.

*   **\[Date of Next Change\]** - \[Description of the change. Ex: Added the `GET /surveys/` endpoint to list surveys.\]
*   **\[Date of Previous Change\]** - \[Description of the change.\]
