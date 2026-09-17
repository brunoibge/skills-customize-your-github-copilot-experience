# 📘 Atividade: Persisting FastAPI Data with SQLite

## 🎯 Objetivo

Adicionar persistência de dados a uma API FastAPI usando SQLite e o módulo `sqlite3` da biblioteca padrão do Python. Ao final, a API deverá manter seus dados entre reinicializações e continuar oferecendo operações CRUD.

## 📝 Tarefas

### 🛠️ Criar o banco de dados SQLite

#### Descrição

Crie a estrutura inicial do banco para armazenar os itens da API, definindo uma tabela com identificador, nome, descrição e quantidade.

#### Requisitos

O programa concluído deve:

- Criar ou abrir um arquivo de banco SQLite ao iniciar a aplicação.
- Criar a tabela de itens automaticamente quando ela ainda não existir.
- Definir uma chave primária para identificar cada item.
- Definir tipos e restrições adequados para os campos obrigatórios.

### 🛠️ Implementar acesso seguro aos dados

#### Descrição

Organize funções responsáveis por abrir conexões, executar operações e fechá-las corretamente, evitando deixar recursos abertos durante as requisições.

#### Requisitos

O programa concluído deve:

- Abrir uma conexão SQLite para cada operação ou requisição necessária.
- Fechar a conexão mesmo quando ocorrer um erro.
- Usar consultas parametrizadas para inserir e buscar valores.
- Separar o acesso ao banco da lógica dos endpoints da API.

### 🛠️ Persistir as operações CRUD

#### Descrição

Substitua a coleção em memória da API por operações SQLite para criar, consultar, atualizar e remover itens.

#### Requisitos

O programa concluído deve:

- Inserir novos itens usando `POST` e retornar o registro criado.
- Listar todos os itens usando `GET`.
- Buscar um item por identificador e retornar `404` quando ele não existir.
- Atualizar um item usando `PUT` ou `PATCH`.
- Remover um item usando `DELETE`.
- Manter os dados disponíveis depois que a aplicação for reiniciada.

### 🛠️ Integrar validação e transações na API

#### Descrição

Finalize a integração entre os modelos Pydantic, os endpoints FastAPI e o banco SQLite, tratando entradas inválidas e confirmando que as alterações foram gravadas.

#### Requisitos

O programa concluído deve:

- Validar os dados recebidos antes de executar comandos no banco.
- Confirmar inserções, atualizações e remoções com transações explícitas.
- Fazer rollback quando uma operação de escrita falhar.
- Retornar códigos HTTP coerentes para sucesso, validação e recurso inexistente.
- Permitir verificar os endpoints pela documentação automática em `/docs`.
