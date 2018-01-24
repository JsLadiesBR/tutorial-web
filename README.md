## Tutorial Desenvolvimento Web


Criado para o workshop da Campus Party 2018 de [Introdução ao Desenvolvimento Web](https://campuse.ro/events/campus-party-brasil-2018/workshop/introducao-ao-desenvolvimento-web/).
Os slides estão salvos no [Speaker Deck](https://speakerdeck.com/anabastos/campus-party-2018-workshop-introducao-a-web)

## Conteúdo
- [Passo 1 - Ambiente](chapter/chapter1.md)
- [Passo 2 - HTML](chapter/chapter2.md)
- [Passo 3 - CSS](chapter/chapter3.md)
- [Passo 4 - Bibliotecas](chapter/chapter4.md)
- [Guia](chapter/guide.md)
- [Para estudar](chapter/final.md)

## Ferramental
- Computador com internet
- Git / Github pages
- Cloud9

## Objetivo
Gradualmente criar um site com HTML5/CSS3 usando git para controlar a versão do projeto em cada parte do aprendizado.

## Sobre o JSLadies

Grupo para unir mulheres interessadas em desenvolvimento web e javascript com encontros abertos e gratuitos com o intuito de preparar mulheres(participantes, palestrantes e coachs) e gerar representatividade feminina no desenvolvimento web! Voltado pra qualquer uma com interesse em aprender.

Nosso grupo no telegram: @Jsladies
[Facebook](https://facebook.com/jsladiesbr/) - [Meetup](https://www.meetup.com/JsLadies-BR/) - [GitHub](http://github.com/jsladiesbr) - [Twitter](https://twitter.com/jsladiessp)

Esse repósitório está em [github.com/JsLadiesBR/tutorial-web](https://github.com/JsLadiesBR/tutorial-web)

## Colaborar com o tutorial
Como instalar, servir e buildar esse tutorial.
Para quem quiser adicionar conteúdo ou corrigir erros :)

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

#### [Ir para o passo 1](chapter/chapter1.md)
