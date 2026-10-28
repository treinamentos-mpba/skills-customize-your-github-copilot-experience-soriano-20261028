# 📘 Assignment: Persistência com SQLite em uma API FastAPI

## 🎯 Objective

Expanda a API de catálogo de livros criada na atividade de FastAPI para armazenar os dados em um banco SQLite. Você praticará operações SQL básicas, persistência entre reinicializações, busca, validação e testes automatizados.

## 📝 Tasks

### 🛠️ Criar o Banco e a Tabela de Livros

#### Descrição
Continue a API de catálogo da atividade anterior. Use o módulo `sqlite3`, incluído no Python, para criar ou abrir um arquivo de banco de dados e preparar uma tabela para os livros.

#### Requisitos
A API concluída deve:

- Criar ou abrir um arquivo SQLite sem apagar os dados existentes
- Criar uma tabela `books` com colunas para `id`, `title`, `author` e `available`
- Usar `id` como chave primária e exigir título e autor
- Confirmar que a tabela é criada ao iniciar a aplicação


### 🛠️ Persistir as Operações do Catálogo

#### Descrição
Substitua a coleção mantida em memória por consultas ao SQLite. Implemente as operações de leitura e escrita para que as mudanças continuem disponíveis após reiniciar a API.

#### Requisitos
A API concluída deve:

- Ler os livros do banco em `GET /books` e `GET /books/{book_id}`
- Salvar novos livros em `POST /books` e retornar o código HTTP `201`
- Atualizar livros em `PUT /books/{book_id}` e removê-los em `DELETE /books/{book_id}`
- Retornar `404` quando uma operação solicitar um identificador inexistente
- Manter os dados após parar e iniciar a API novamente


### 🛠️ Adicionar Busca, Validação e Testes

#### Descrição
Torne o catálogo mais fácil de consultar e confiável para seus usuários. Adicione uma busca simples e escreva testes para os principais comportamentos da API.

#### Requisitos
A API concluída deve:

- Permitir filtrar livros por parte do título ou pelo autor, sem diferenciar maiúsculas de minúsculas
- Validar os campos enviados e rejeitar título ou autor vazio e tipos inválidos
- Usar parâmetros nas consultas SQL em vez de montar comandos com valores recebidos nas requisições
- Incluir testes automatizados para criar e buscar livros, dados inválidos, identificadores inexistentes e persistência
- Executar os testes com um banco temporário ou separado para não alterar os dados usados pela aplicação
