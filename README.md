# API de Games
Esta API é utilizada para TAL e TAL...
## Endpoints
### GET /games
Esse enpoint é responsavel por retornar a listagem de todos os games cadastrados no banco de dados.
#### Parametros
Nenhum
#### Respostas
##### OK! 200
Caso essa resposta aconteça voce vai receber a listagem de todos os games

Exemplo de resposta:
```
[
    {
        "id": 23,
        "title": "Call of Duty WM",
        "year": 2019,
        "price": 69
    },
    {
        "id": 65,
        "title": "Sea of thieves",
        "year": 2018,
        "price": 40
    },
    {
        "id": 2,
        "title": "Minecraft",
        "year": 2012,
        "price": 20
    }
]

```
##### Falha na autenticação! 401

Exemplo de resposta:
```
{
    "err": "Token inválido"
}
```
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durente o processo de autenticação da requisição. Motivos: Token inválido, token expirado.

### POST /auth
Esse enpoint é responsavel por fazer o processo de login.
#### Parametros
email: e-mail do usuario cadastrado no sistema.

password: senha do usuario cadastrado no sistema, com aquele determinado e-mail.

Exemplo:
```
{
    "email": "rbcardoso@gmail.com",
    "password": "node1231"
}
```

#### Respostas
##### OK! 200
Caso essa resposta aconteça voce vai receber o token JWT para conseguir acessar endpoints protegidos na API.

Exemplo de resposta:
```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJyYmNhcmRvc29AZ21haWwuY29tIiwiaWF0IjoxNjU4MDEzMDQxLCJleHAiOjE2NTgxODU4NDF9.8c1KhSa8NBX4iopvnvtgar3DsvaauKeMr1cazwNEIw4"
}

```
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: senha ou email incorretos.

Exemplo de resposta:
```
{
    "err": "Token inválido"
}
```
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durente o processo de autenticação da requisição. Motivos: Token inválido, token expirado.

