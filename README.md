## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

## Users

GET/users

Pega todos os usuários cadastrados

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

**GET/users - FORMATO DA REQUISIÇÃO**

{
"email":"leo_rodrigues@hotmail.com",
"password": "123456",
"name": "leonam",
"age": 21
}

_OBS: Email e senha são obrigatórios_

**FORMATO DA RESPOSTA**

{
"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6Imxlb19yb2RyaWd1ZXNAaG90bWFpbC5jb20iLCJpYXQiOjE2MzU1NDQ0NzAsImV4cCI6MTYzNTU0ODA3MCwic3ViIjoiNCJ9.JZ1DQBW8Q1weZSsm8IFTpWkKs1_H8YzzEqLMJMOLtkk",
"user": {
"email": "leo_rodrigues@hotmail.com",
"name": "leonam",
"age": 21,
"id": 4
}
}

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

**POST/login - FORMATO DA REQUISIÇÃO**

{
"email": "leonam_5000@hotmail.com",
"password": "123456"
}

_OBS: Email e senha são obrigatórios_

**FORMATO DA RESPOSTA**

{
"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6Imxlb25hbV81MDAwQGhvdG1haWwuY29tIiwiaWF0IjoxNjM1NTQ0ODA5LCJleHAiOjE2MzU1NDg0MDksInN1YiI6IjIifQ.CLeHCKaPOmvKTMX26FsZqA5yvT7ksSk13gZylEMCXww",
"user": {
"email": "leonam_5000@hotmail.com",
"name": "leonam",
"age": 21,
"id": 2
}
}

## PRODUCTS

GET/products

Lista todos os produtos existentes na loja

## CREATE PRODUCTS

**FORMATO DA REQUISIÇÃO**

POST/products

{
"image":"",
"name": "HamburguerX",
"type": "Sanduiche",
"price": 13.99,
"userId": 2
}

_OBS_: Uso do "userId" é obrigatório

## PROMOTIONS

GET/promotions

Lista todas as promoções existentes

_OBS: Apenas para usuários logados_

## CONTRIBUTORS

GET/contributors

Lista todos os contribuidores da aplicação

_OBS: Apenas leitura mas não pode ser alterado_
