# Node - Desafio 4 (Novo)

[![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/osvaldokalvaitir/reactjs-desafio4-novo/blob/master/LICENSE)
![](https://img.shields.io/github/package-json/v/osvaldokalvaitir/reactjs-desafio4-novo.svg)
![](https://img.shields.io/github/last-commit/osvaldokalvaitir/reactjs-desafio4-novo.svg?color=red)
![](https://img.shields.io/github/languages/top/osvaldokalvaitir/reactjs-desafio4-novo.svg?color=yellow)
![](https://img.shields.io/github/languages/count/osvaldokalvaitir/reactjs-desafio4-novo.svg?color=lightgrey)
![](https://img.shields.io/github/languages/code-size/osvaldokalvaitir/reactjs-desafio4-novo.svg)
![](https://img.shields.io/github/repo-size/osvaldokalvaitir/reactjs-desafio4-novo.svg?color=blueviolet)
[![made-for-VSCode](https://img.shields.io/badge/Made%20for-VSCode-1f425f.svg)](https://code.visualstudio.com/)
![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)

Aplicação Facebook usando ReactJS, Babel, Webpack, Style Loader, CSS Loader, File Loader, prop-types e React DevTools.

## Desafio 04. Introdução ao React

Crie uma aplicação do zero utilizando **Webpack, Babel, Webpack Dev Server e ReactJS**.

Nessa aplicação você irá desenvolver uma **interface** semelhante com a do **Facebook** utilizando React.

As informações contidas na interface são **estáticas** e não precisam refletir nenhuma API REST ou back-end.

### Tela da aplicação

![Facebook](/.github/assets/facebook.png)

O layout não precisa ficar exatamente igual, você pode utilizar sua criatividade para modificar da maneira que preferir.

O mais importante é que todos elementos apareçam em tela.

O layout da aplicação está em [nesse link](/.github/assets/layout.sketch) que pode ser aberto por essa ferramenta gratuita e online: https://www.figma.com/

### Componentes

Na imagem abaixo destaquei cada componente que você criará e abaixo da imagem está a descrição e responsabilidades de cada um:

![Componentes](/.github/assets/components.png)

**Header (Amarelo):** Responsável por exibir a logo e o link para acessar o perfil;

**PostList (Verde):** Responsável por armazenar os dados da listagem de post, esses dados devem ficar dentro do `state` do componente e não em uma variável comum, por exemplo:

```js
class PostList extends Component {
  state = {
    posts: [
      {
        id: 1,
        author: {
          name: 'Julio Alcantara',
          avatar: 'http://url-da-imagem.com/imagem.jpg'
        },
        date: '04 Jun 2019',
        content: 'Pessoal, alguém sabe se a Rocketseat está contratando?',
        comments: [
          {
            id: 1,
            author: {
              name: 'Diego Fernandes',
              avatar: 'http://url-da-imagem.com/imagem.jpg'
            },
            content: "Conteúdo do comentário"
          }
        ],
      },
      {
        id: 2,
        // Restante dos dados de um novo post
      }
    ]
  };
}
```

**Post (Vermelho):** Responsável por exibir os dados do post, esses dados devem vir através de uma propriedade recebida do componente PostList, ou seja, lá no PostList você terá algo assim:

```js
posts.map(post => <Post key={post.id} data={post} />)
```

**Comment (Azul):** Responsável por exibir um comentário. Os dados do comentário virão por uma propriedade do componente. Dentro do componente Post você terá um novo `.map` para listar os comentários do post:

```js
data.comments.map(comment => <Comment key={comment.id} data={comment} />)
```

## Índice

- [Capturas de Tela](#capturas-de-tela)

  - [Principal](#principal)

- [Desenvolvimento](#desenvolvimento)

  - [Configuração do Ambiente](#configuração-do-ambiente)

  - [Instalação do Projeto](#instalação-do-projeto)

  - [Execução do Projeto](#execução-do-projeto)

- [Utilizados no Projeto](#utilizados-no-projeto)

  - [Bibliotecas](#bibliotecas)

  - [Ferramentas](#ferramentas)

## Capturas de Tela

### Principal

![Main](/.github/assets/main.png)
Esta é a única tela do site, onde aparecem os posts estáticos dos usuários.

## Desenvolvimento

### Configuração do Ambiente

Clique [aqui](https://github.com/osvaldokalvaitir/projects-settings/blob/master/README.md) e siga `Configuração de Ambiente`.

### Instalação do Projeto

Clique [aqui](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/nodejs.md) e siga `Instalação de Projeto`.

### Execução do Projeto

Clique [aqui](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/webpack.md) e siga `Execução de Projeto para Desenvolvimento` ou `Construção e Execução de Projeto para Produção`.

## Utilizados no Projeto

### Bibliotecas

- [@babel/core](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/@babel-core.md)

- [@babel/plugin-proposal-class-properties](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/@babel-plugin-proposal-class-properties.md)

- [@babel/preset-env](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/@babel-preset-env.md)

- [@babel/preset-react](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/@babel-preset-react.md)

- [Babel Loader](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/babel-loader.md)

- [CSS Loader](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/css-loader.md)

- [File Loader](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/file-loader.md)

- [prop-types](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/prop-types.md)

- [React](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/react.md)

- [react-dom](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/react-dom.md)

- [Style Loader](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/style-loader.md)

- [webpack](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/webpack.md)

- [webpack-cli](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/webpack-cli.md)

- [webpack-dev-server](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/webpack-dev-server.md)

### Ferramentas

- [React Developer Tools](https://github.com/osvaldokalvaitir/projects-settings/blob/master/browser/chrome/extensions/react-developer-tools.md)