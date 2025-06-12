# Biblioteca de Mídia / Media Library

### Biblioteca de Mídia

A API da Biblioteca de Mídia permite que você faça upload e gerencie arquivos, como imagens para e-mails, anexos para contatos ou vídeos para cursos, diretamente no armazenamento da sua subconta Marketek.

**Listar Arquivos e Pastas**

Recupere uma lista de todos os arquivos e pastas na raiz da sua biblioteca de mídia.

*   **Endpoint:** `GET /media-library/`
*   **Parâmetros de Query:** `locationId` (obrigatório)

**Exemplo (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/media-library/?locationId=SEU_LOCATION_ID' \
--header 'Authorization: Bearer SUA_CHAVE_API' \
--header 'Version: 2021-07-28'
```

**Fazer Upload de um Arquivo**

Envie um novo arquivo para a sua biblioteca. Esta requisição utiliza o formato `multipart/form-data`.

*   **Endpoint:** `POST /media-library/`
*   **Corpo da Requisição:** Deve ser `multipart/form-data` contendo o `locationId` e o `file`.

  

* * *

### Media Library

The Media Library API allows you to upload and manage files, such as images for emails, attachments for contacts, or videos for courses, directly to your Marketek sub-account's storage.

**List Files and Folders**

Retrieve a list of all files and folders in the root of your media library.

*   **Endpoint:** `GET /media-library/`
*   **Query Parameters:** `locationId` (required)

**Example (cURL):**

Bash

  

```plain
curl --location --request GET 'https://services.leadconnectorhq.com/media-library/?locationId=YOUR_LOCATION_ID' \
--header 'Authorization: Bearer YOUR_API_KEY' \
--header 'Version: 2021-07-28'
```

**Upload a File**

Send a new file to your library. This request uses the `multipart/form-data` format.

*   **Endpoint:** `POST /media-library/`
*   **Request Body:** Must be `multipart/form-data` containing the `locationId` and the `file`.
