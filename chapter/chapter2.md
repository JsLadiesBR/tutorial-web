## Passo 2

#### Indice
* [Conteúdo em HTML](#conteudo-em-html)
* [Sobre html](#sobre-html)
* [Seu primeiro commit](#seu-primeiro-commit)

## Conteudo em HTML

#### O que é HTML?

HTML descreve cada parte de uma pagina web no seu navegador.
Quando você visita um site ele consegue diferenciar cada tipo de texto pq ele tem um HTML tag diferente
All the text on this page you’re reading right now lives inside HTML tags that tell your browser how to order the content on the page. 

Headlines geralmente são `<h1>`, `<h2>`, `<h3>` enquanto paragramos são a tag <p>

```html
<h1>Headline</h1>
<p>Paragrafo</p>
```

No html todas as tags são abertas com a tag em si e fechadas com um / 

bbalablabalbalabal html

Para nossa pagina copie e cole o seguinte

```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha Pagina</title>
</head>
<body>
    <h1>Hello World</h1>
    <p>Campus Pary 2018</p>
</body>
</html>
```

- html é a tag que define tudo dentro do html
- Todo html tem um head e body, head tem informações sobre a página enquanto o body tem o conteúdo da página

Todo o conteúdo a ser modificado deve ficar dentro do `<body>`

Note que ao invés de 
`<body><h1>Hello World</h1><p>Campus Pary 2018</p></body>`

Fica muito mais legivel se colocassemos o conteúdo em outra linha.
Mas é importante sempre dar **tab** ou **4 espaços** para simbolizar que o conteúdo do `h1` e do `p` estão dentro do `body` e deixar o código mais legivel.

```css
<body>
    <h1>Hello World</h1>
    <p>Campus Pary 2018</p>
</body>
```

## Sobre HTML
html
conteudo etc

## Seu primeiro commit

Nas abas de console existe uma chamada "bash - "seu nome""
img

Clique na aba e você vai ter como se fosse um terminal em que podemos usar comandos git.
Para inserir no nosso repositório as modificações que fizemos é preciso seguir os seguintes passos:
```bash
# Verifique status do repositório.
git status
# Adicione arquivo index p/ staging
git add index.html
# Faz commit
git commit -m "Initial Commit"
# Adiciona modificações
git push
```

Agora se você acessar o link [https://NOMEDASUACONTA.github.io](https://NOMEDASUACONTA.github.io) verá o conteúdo do seu site
Demora algns minutos para as mudanças realmente irem ao ar mas em pouco será posivel ver suas modificações no ar.

#### [Ir para o passo 3](chapter3.md)