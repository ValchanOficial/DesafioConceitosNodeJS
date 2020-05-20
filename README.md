# Rocketseat - Desafio: Conceitos do Node.js

## Sobre o desafio

Aplicação para armazenar os repositórios do portfólio, permite a criação, listagem, atualização e remoção dos repositórios, e além disso permite que os repositórios possam receber "likes".

## Start

```js
    yarn install    // instala dependências
    yarn dev        // inicia aplicação em modo desenvolvedor
    yarn test       // executa os testes
```

## Rotas da aplicação

- POST /repositories: Recebe um title, url e techs no corpo da requisição, armazena os dados, e retorna um objeto. 
Exemplo response: { id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }

- GET /repositories: Lista todos os repositórios;

- PUT /repositories/:id: Recebe e altera o title, a url e as techs do repositório que possua o id igual ao id presente nos parâmetros da rota;

- DELETE /repositories/:id: Deleta o repositório com o id presente nos parâmetros da rota;

- POST /repositories/:id/like: Aumenta o número de likes do repositório específico escolhido através do id presente nos parâmetros da rota, a cada chamada dessa rota, o número de likes é aumentado em 1;
