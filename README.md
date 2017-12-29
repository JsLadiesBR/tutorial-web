## Tutorial Desenvolvimento Web

Criado a principio para o workshop da Campus Party 2018 de [Introdução ao Desenvolvimento Web](https://campuse.ro/events/campus-party-brasil-2018/workshop/introducao-ao-desenvolvimento-web/).


## Ferramental
- Computador
- Git / Github pages
- CodeAnywhere

## Objetivo
Gradualmente criar um site com HTML5/CSS3 usando git para controlar a versão do projeto em cada parte do aprendizado.

## Conteúdo
- O que é desenvolvimento web?
- Adicionando conteúdo com HTML
- Estilizando com CSS
- Importanto bibliotecas
- Validando formularios com JS


## Colaborar

#### Install
```bash
npm install -g gitbook-cli
```

#### Server
```bash
gitbook serve
```

#### Build to gh-pages
```bash
gitbook install && gitbook build
cp -R _book/* .
git clean -fx _book
```