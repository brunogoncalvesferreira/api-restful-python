# API RESTful com PYTHON

Esta é uma API RESTful simples desenvolvida com Flask, que permite realizar operações CRUD (Create, Read, Update, Delete) em uma lista de usuários. A API oferece rotas para listar, obter, criar, atualizar e deletar usuários.

# Requisitos
- Python
- Flask
- insomnia ou postman para testar a API

# Para rodar a aplicação

1. Clone o repositório para a sua máquina local:
```git
git clone https://github.com/brunogoncalvesferreira/api-restful-python.git
```

2. Navegue até o diretório do projeto:
```git
cd api-restful-python
```

3. Instale as dependências:
```git
pip install Flask
```

4. Para iniciar a aplicação, execute o seguinte comando no terminal:
```git
python app.py
```

A API estará disponível em http://127.0.0.1:8080 ou http://localhoost:8080

# Endpoints da API
1. Listar todos os usuários

- URL: /users
- Método HTTP: GET
- Descrição: Retorna a lista de todos os usuários.
- Resposta de sucesso:

```json
[
    {'id': 1, 'name': 'Alice', 'email': 'alice@example.com'},
    {'id': 2, 'name': 'Bob', 'email': 'bob@example.com'},
    {'id': 3, 'name': 'João', 'email': 'joao@example.com'}
]
```

2. Obter um usuário específico
- URL: /users/<int:user_id>
- Método HTTP: GET
- Descrição: Retorna um usuário específico pelo ID.
- Resposta de sucesso:

```json
{'id': 1, 'name': 'Alice', 'email': 'alice@example.com'}
```
- Resposta de erro:

```json
{'message': 'User not found'}
```

3. Criar um novo usuário
- URL: /users
- Método HTTP: POST
- Descrição: Cria um novo usuário.
- Corpo da requisição (JSON):

```json
{
    "name": "Carlos",
    "email": "carlos@example.com"
}
```

- Resposta de sucesso:

```json
{'id': 4, 'name': 'Carlos', 'email': 'carlos@example.com'}
```

4. Atualizar um usuário existente
- URL: /users/<int:user_id>
- Método HTTP: PUT
- Descrição: Atualiza os dados de um usuário existente.
- Corpo da requisição (JSON):

```json
{
    "name": "Alice Updated",
    "email": "alice_updated@example.com"
}
```

- Resposta de erro:

```json
{'message': 'User not found'}
```

5. Deletar um usuário
- URL: /users/<int:user_id>
- Método HTTP: DELETE
- Descrição: Remove um usuário da lista.
- Resposta de sucesso:

```json
{'message': 'User deleted'}
```

# Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests para melhorias ou correções.

# Licença
Este projeto está licenciado sob a licença MIT.