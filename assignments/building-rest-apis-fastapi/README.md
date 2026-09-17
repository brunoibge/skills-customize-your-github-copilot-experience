# 📘 Atividade: Building REST APIs with FastAPI

## 🎯 Objetivo

Construir uma API REST usando o framework FastAPI para praticar criação de endpoints, parâmetros, validação de dados e operações CRUD em Python.

## 📝 Tarefas

### 🛠️ Criar o primeiro endpoint

#### Descrição

Configure uma aplicação FastAPI e crie um endpoint inicial que responda a uma requisição HTTP GET.

#### Requisitos

O programa concluído deve:

- Criar uma aplicação FastAPI executável localmente.
- Disponibilizar o endpoint `GET /`.
- Retornar uma resposta JSON contendo uma mensagem de boas-vindas.
- Permitir visualizar a documentação automática em `/docs`.

### 🛠️ Adicionar parâmetros e validação

#### Descrição

Amplie a API com um endpoint que receba informações pela URL e valide os dados enviados pelo cliente.

#### Requisitos

O programa concluído deve:

- Disponibilizar um endpoint `GET /items/{item_id}` que receba um identificador inteiro.
- Aceitar um parâmetro de consulta opcional para filtrar ou personalizar a resposta.
- Retornar os dados recebidos em formato JSON.
- Responder com erro HTTP apropriado quando os dados forem inválidos.

### 🛠️ Implementar operações CRUD

#### Descrição

Crie uma coleção de itens armazenada em memória e implemente as operações para criar, consultar, atualizar e remover registros.

#### Requisitos

O programa concluído deve:

- Implementar endpoints `GET`, `POST`, `PUT` ou `PATCH` e `DELETE` para a coleção.
- Usar modelos Pydantic para validar o corpo das requisições.
- Retornar status HTTP coerentes com cada operação, incluindo `201` ao criar um recurso.
- Retornar `404` quando o cliente solicitar um item inexistente.
- Manter os itens criados, atualizados e removidos durante a execução da aplicação.

### 🛠️ Documentar e tratar erros da API

#### Descrição

Finalize a API organizando as respostas e documentando o comportamento dos endpoints para que outro desenvolvedor consiga utilizá-la.

#### Requisitos

O programa concluído deve:

- Exibir descrições, parâmetros e modelos na documentação automática do FastAPI.
- Validar regras de negócio além dos tipos básicos, como campos obrigatórios ou valores positivos.
- Retornar mensagens de erro JSON claras para entradas inválidas e recursos inexistentes.
- Testar pelo menos um endpoint usando a documentação interativa ou uma ferramenta HTTP.
