## Tutorial Desenvolvimento Web


Este tutorial foi criado para o workshop do JSLadies RJ, realizado no dia 22/09/2018 na [Caelum](https://www.caelum.com.br).

## Conteúdo
- [Passo 1 - Ambiente](chapter/chapter1.md)
- [Passo 2 - HTML](chapter/chapter2.md)
- [Passo 3 - CSS](chapter/chapter3.md)
- [Passo 4 - Bibliotecas](chapter/chapter4.md)
- [Guia](chapter/guide.md)
- [Para estudar](chapter/final.md)

## Ferramentas
- Computador com internet
- Git / Github Pages

## Objetivo
Neste workshop iremos ensinar conceitos básicos de HTML e CSS, que serão suficientes para que você consiga criar o seu site. Também ensinaremos Git, uma ferramenta que irá te ajudar a colocar no ar tudo o que você construiu durante o evento :)

## Sobre o JSLadies
Nós somos o primeiro grupo nacional e exclusivamente feminino focado em ensinar e ajudar mais mulheres a programar.
Nossa iniciativa nasceu da necessidade de promover um ambiente seguro, agradável e produtivo para qualquer pessoa cis, trans, binária ou não-binária que se identifique com o gênero feminino e que se interesse por computação.

Conheça nossas redes sociais:

- [Facebook](https://facebook.com/jsladiesbr/)
- [Meetup](https://www.meetup.com/JsLadies-BR/)
- [GitHub](http://github.com/jsladiesbr)
- [Twitter](https://twitter.com/jsladiesrj)

Temos também um grupo no Telegram! Se caso você tiver interesse em participar dele, por favor entre em contato com as organizadoras, pois elas te enviarão um convite :)

## Quer colaborar com o tutorial?
Segue abaixo um pequeno manual de como instalar, servir e buildar esse tutorial:

#### Install
```bash
npm install -g gitbook-cli
```

#### Server
```bash
gitbook serve
```

#### Build
```bash
gitbook install && gitbook build
cp -R _book/* .
git clean -fx _book
```

#### [Ir para o passo 1](chapter/chapter1.md)
