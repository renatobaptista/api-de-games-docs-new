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
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durente o processo de autenticação da requisição. Motivos: Token inválido, token expirado.
