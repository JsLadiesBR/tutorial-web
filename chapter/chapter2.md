## Passo 2

#### Indice
* [O que é HTML](#O-que-e-HTML?)
* [Adicionando Conteúdo](#adicionando-conteudo)
* [Seu primeiro commit](#seu-primeiro-commit)

## O que e HTML?

HTML descreve cada parte de uma pagina web no seu navegador.
Quando você visita um site ele consegue diferenciar cada tipo de texto pq ele tem um HTML tag diferente
All the text on this page you’re reading right now lives inside HTML tags that tell your browser how to order the content on the page. 

```html
<h1>Headline</h1>
<p>Paragrafo</p>
```

No html todas as tags são abertas com a tag em si e fechadas com um / 

Para nossa pagina copie e cole o seguinte.

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

- `<html>` é a tag que define tudo dentro do HTML.
- Todo HTML tem um `<head>` e `<body>`, head tem informações sobre a página enquanto o body tem o conteúdo da página.

Todo o conteúdo a ser modificado deve ficar dentro do `<body>`

Note que ao invés de 
`<body><h1>Hello World</h1><p>Campus Pary 2018</p></body>`

Fica muito mais legivel quando colocamos o conteúdo dentro do body  em outra linha.
É muito importante sempre dar **tab** ou **4 espaços** para simbolizar que o conteúdo do `h1` e do `p` está dentro do `body` e deixar o código mais legivel. O nome disso é **identação**

```css
<body>
    <h1>Hello World</h1>
    <p>Campus Pary 2018</p>
</body>
```

## Adicionando conteúdo

##### Headers e texto

Headlines são `<h1>`, `<h2>`, `<h3>` enquanto paragrafos são a tag `<p>`

`<h1>Test</h1>`
# Test

`<h2>Test</h2>`
## Test

`<h4>Test</h4>`
#### Test

`<p>Test<p>`
Test

##### Listas

**Listas não-enumeradas**

**Listas enumeradas**

##### Tables
##### Links
##### Images
##### Videos
##### Formulários


## Seu primeiro commit

Nas abas de console existe uma chamada "bash - "seu nome""

![Usando o bash do c9](imgs/cap2-git.png)

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