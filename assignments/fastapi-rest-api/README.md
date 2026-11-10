# 📘 Atividade: Building REST APIs com FastAPI

## 🎯 Objetivo

Construa uma API REST para gerenciar um catálogo de livros usando FastAPI. Você praticará rotas HTTP, validação de dados com Pydantic, códigos de status e a documentação interativa do FastAPI.

## 📝 Tarefas

### 🛠️ Criar a aplicação e consultar livros

#### Descrição
Crie `main.py`, inicialize uma aplicação FastAPI e prepare uma lista em memória com pelo menos dois livros, cada um com `id`, `title` e `author`. Instale FastAPI e Uvicorn e execute o servidor localmente.

#### Requisitos
O programa concluído deve:

- Criar a aplicação FastAPI e disponibilizar `GET /health`, que retorna `{"status": "ok"}`.
- Disponibilizar `GET /books`, retornando a lista de livros como JSON.
- Iniciar com o comando `uvicorn main:app --reload` e permitir testar as rotas em `/docs`.

### 🛠️ Consultar e cadastrar livros

#### Descrição
Adicione operações para consultar um livro pelo identificador e cadastrar livros usando um modelo Pydantic para validar os dados recebidos.

#### Requisitos
O programa concluído deve:

- Disponibilizar `GET /books/{book_id}` e retornar o livro correspondente.
- Retornar o código HTTP `404` quando o identificador solicitado não existir.
- Disponibilizar `POST /books`, validar `title` e `author` como campos obrigatórios e atribuir um identificador único ao novo livro.
- Retornar o livro criado com o código HTTP `201`.

### 🛠️ Atualizar e remover livros

#### Descrição
Complete as operações de gerenciamento para atualizar ou remover um livro existente, preservando respostas HTTP claras para cada resultado.

#### Requisitos
O programa concluído deve:

- Disponibilizar `PUT /books/{book_id}` para atualizar o título e o autor de um livro existente.
- Disponibilizar `DELETE /books/{book_id}` para remover um livro existente e responder com o código HTTP `204`.
- Retornar `404` nas operações de atualização e remoção quando o identificador não existir.
- Manter os dados em memória durante a execução; não é necessário implementar persistência em banco de dados.
