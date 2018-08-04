## Passo 2

#### Indice
* [O que é HTML](#O-que-e-HTML?)
* [Adicionando Conteúdo](#adicionando-conteudo)
  * [Headers e texto](#headers-e-texto)
  * [Formatação](#formatação)  
  * [Listas](#listas)
  * [Tables](#tables)
  * [Links](#links)
  * [Images](#images)
  * [Exemplo](#exemplo)  
* [Seu primeiro commit](#seu-primeiro-commit)

## O que e HTML?

**HTML** significa **Hyper Text Markup Language** e funciona para descrever cada parte da estrutura de uma pagina web no seu navegador.
Quando você visita um site ele consegue diferenciar cada tipo de texto pois ele os elementos são diferenciados por tags HTML diferentes que contam pro navegador como ordenar e mostrar o conteúdo da página que renderizam de forma correta o conteúdo.

```html
<h1>Headline</h1>
<p>Paragrafo</p>
```

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

- `<!DOCTYPE html>` define a versão do HTML.
- `<html>` é a tag que define tudo dentro do HTML.
- O `<head>` tem meta informações sobre a página 
- O `<body>` contém todo conteúdo visivel da página.



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

Atualmente se apertamos o botão de **run** não temos nada demais além de um Hello World.

![Exemplo do estado atual](imgs/cap2-hello.png)

Mostrar **"Hello, World!"** é como se fosse uma "tradição" no mundo da programação quando é nossa primeira vez em alguma linguagem e geralmente é usada pra mostrar sintaxe basica de algo funcional.

## Adicionando conteúdo

### Headers e texto

Headlines são `<h1>`, `<h2>`, `<h3>` enquanto paragrafos são a tag `<p>`.

Geralmente toda página tem um `<h1>` que é o nome da pagina em si.

```html
<h1>Maria Lúcia - Portfolio</h1>
```
Resultado:
# Maria Lúcia - Portfolio
<hr>
```html
<h2>Portfolio da Maria Lúcia</h2>
```
Resultado:
## Portfolio da Maria Lúcia
<hr>
```html
<h4>Test</h4>
```
Resultado:
#### Item
<hr>

```html
<p>Este site é um portfolio de minha habilidades e experiencias<p>
```
Resultado:
Este site é um portfolio de minha habilidades e experiencias

### Formatação

Para formatar textos usa-se estas tags em volta das palavras:

- `<b>` - <b>Negrito</b>
- `<strong>` - <strong>Importante</strong>
- `<i>` - <i>Italico</i>
- `<em>` - <em>Emfatizado</em>
- `<mark>` - <mark>Marcado</mark>
- `<small>` - <small>Pequeno</small>
- `<del>` - <del>Deletado</del>
- `<ins>` - <ins>Inserido</ins>
- `<sub>` - <sub>Subscrito</sub>
- `<sup>` - <sup>Superscrito</sup>

### Listas

**Listas não-enumeradas**

Listas não enumeradas tem a tag `<ul>` e cada item da lista fica dentro da tag `<li>`.

```html
<ul>
  <li>Café</li>
  <li>Chá</li>
  <li>Leite</li>
</ul>
```
Resultado:

- Café
- Chá
- Leite

Podemos colocar listas dentro de listas também:

```html
<ul>
  <li>Café</li>
  <li>Chá
    <ul>
      <li>Black tea</li>
      <li>Green tea</li>
    </ul>
  </li>
  <li>Leite</li>
</ul>
```
Resultado:

- Café
- Chá
    - Black tea
    - Green tea
- Leite


**Listas enumeradas**

Em listas enumeradas usa-se a tag `<ol>` ao invés de `<ul>`. Cada item ainda fica dentro da tag `<li>`.

```html
<ol>
  <li>Coffee</li>
  <li>Tea
    <ol>
      <li>Black tea</li>
      <li>Green tea</li>
    </ol>
  </li>
  <li>Milk</li>
</ol>
```
Resultado:

1. Café
1. Chá
   1. Chá Preto
   1. Chá Verde
1. Leite


### Tables

Tables usam a tag `<table>`. `<tr>` define uma coluna da tabela enquanto `<td>` define a celular.
Para o header da table usa-se a tag `<th>` conforme o exemplo:.

```html
<table>
  <tr>
    <th>Nome</th>
    <th>Sobrenome</th> 
    <th>Idade</th>
  </tr>
  <tr>
    <td>João</td>
    <td>Smith</td> 
    <td>50</td>
  </tr>
  <tr>
    <td>Eva</td>
    <td>Maria</td> 
    <td>94</td>
  </tr>
</table>
```
Resultado:

<table>
  <tr>
    <th>Nome</th>
    <th>Sobrenome</th> 
    <th>Idade</th>
  </tr>
  <tr>
    <td>João</td>
    <td>Smith</td> 
    <td>50</td>
  </tr>
  <tr>
    <td>Eva</td>
    <td>Maria</td> 
    <td>94</td>
  </tr>
</table>


### Links

Para linkar textos usa-se a tag `<a>`, em que a propriedade `href` é a url do texto e o texto em si fica dentro da tag.

Esta sintaxe:
```html
<a href="http://fb.com">Facebook</a>
<a href="http://google.com">Google</a> - <a href="http://github.com">Github</a>
```
Resultado:

[Facebook](http://fb.com)
[Google](http://google.com) - [Github](http://github.com)

### Images

Para adicionar imagens usa-se a tag `<img>`, em que a propriedade `src` é a url da imagem ou então o caminho no projeto até a imagem. A propriedade `alt` descreve o conteúdo da imagem caso ela não seja carregada corretamente.

```html
<img src="url imagem" alt="Foto da Maria Lúcia">
```

### Exemplo

Juntando tudo isso podemos ter algo assim:

![Exemplo](imgs/cap2-exemplo.png)

Você pode usar esse exemplo de referência:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha Pagina</title>
</head>
<body>
    <img src="http://vidadiaria.com.br/images/2017/educacao/agosto/estudante3.jpg" alt="Foto da Maria Lúcia">
    <h1>Maria Lúcia do Carmo</h1>
    <h2>Estudante de ciência da computação</h3>

    <p>Brasileira, solteira, 22 anos - São Paulo - SP<p>
    <a href="http://fb.com">Facebook</a> - <a href="http://github.com">Github</a> - <a href="http://twitter.com">Twitter</a>
    <p><b>Email:</b> maria@gmail.com</p>
    <p><b>Phone:</b> (+55)11-986993010</p>

    <h3>Experiência</h3>
    <p><i>2017/06 ~ Atual</i> - Estágiaria no Facebook - <a href="http://fb.com">Facebook.com</a></p>

    <h3>Educação</h3>
    <p> Bacharelado em ciencia da computação(<i>Cursando</i>) - USP</p>

    <h3>Habilidades</h3>
    <ul>
      <li>HTML5 / CSS3</li>
      <li>Fazer café</li>
    </ul>

    <h3>Interesses<h3>
    <ul>
      <li>Jogar LoLzinho<i>(Sou platina)</i></li>
    </ul>
</body>
</html>
```

Com HTML podemos também adicionar audio, video, canvas, formulários, dentre muitas outras coisas. No [final do curso](final.md) tem vários links com tutoriais e guias pra esse conteúdo remanescente.

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

Clique em configurações no lado direito da pagina do seu repositório no github e na parte chamada **"Github Pages"**
Selecione para a branch "master", assim todas as modificações que forem feitas no seu projeto dentro deste repositorio vão ser publicadas na url `NOMEDASUACONTA.github.io`.

![Exemplo configuração de github pages](imgs/cap1-config.png)

Se você receber uma mensagem de `"Your site is ready to be published at http://NOMEDASUACONTA.github.io/."`
é porque tudo está ok.

Agora se você acessar o link [https://NOMEDASUACONTA.github.io](https://NOMEDASUACONTA.github.io) verá o conteúdo do seu site
Demora algns minutos para as mudanças realmente irem ao ar mas em pouco será posivel ver suas modificações no ar.

#### [Ir para o passo 3](chapter3.md)