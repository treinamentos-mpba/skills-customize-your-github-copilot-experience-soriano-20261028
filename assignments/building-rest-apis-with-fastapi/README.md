# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Construa uma API REST para gerenciar um catálogo de livros usando FastAPI. Você praticará a criação de rotas, o uso dos métodos HTTP, a validação de dados e a escolha de códigos de status apropriados.

## 📝 Tasks

### 🛠️ Create the Book Catalog API

#### Descrição
Crie uma aplicação FastAPI que mantenha uma coleção de livros em memória. Cada livro deve ter um identificador, título, autor e indicação de disponibilidade. Inicie o servidor localmente e use a documentação interativa do FastAPI para explorar as rotas.

#### Requisitos
A API concluída deve:

- Definir um modelo de livro com os campos `id`, `title`, `author` e `available`
- Implementar `GET /books` para retornar todos os livros
- Implementar `GET /books/{book_id}` para retornar um livro pelo identificador
- Retornar o código HTTP `404` quando o identificador solicitado não existir
- Incluir pelo menos dois livros iniciais para facilitar a verificação das rotas


### 🛠️ Add Create, Update, and Delete Operations

#### Descrição
Expanda o catálogo para permitir que clientes criem livros, atualizem seus dados e removam livros existentes. Use os métodos HTTP apropriados e valide o corpo das requisições com modelos do FastAPI/Pydantic.

#### Requisitos
A API concluída deve:

- Implementar `POST /books` para criar um livro e retornar o livro criado com o código HTTP `201`
- Implementar `PUT /books/{book_id}` para substituir os dados de um livro existente
- Implementar `DELETE /books/{book_id}` para remover um livro existente
- Retornar `404` para atualizações ou remoções de identificadores inexistentes
- Confirmar que as operações alteram a coleção e que as alterações podem ser verificadas com `GET /books`


### 🛠️ Validate Requests and Verify the API

#### Descrição
Revise a API para responder de forma consistente a entradas inválidas e demonstre os principais fluxos de uso. Use a página `/docs` ou comandos HTTP para testar as rotas.

#### Requisitos
A API concluída deve:

- Validar os campos obrigatórios e seus tipos usando modelos Pydantic
- Rejeitar dados inválidos com uma resposta de erro HTTP apropriada, sem adicionar ou modificar livros
- Retornar códigos de sucesso apropriados para cada operação e documentar o comportamento de cada rota
- Demonstrar um fluxo completo: listar livros, criar um, consultá-lo por ID, atualizá-lo e removê-lo
- Informar como instalar FastAPI e Uvicorn e como iniciar o servidor local para testar a API
