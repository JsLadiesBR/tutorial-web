## Passo 2

## O que é HTML?

**HTML** significa **Hyper Text Markup Language** e como o próprio nome já diz, é uma linguagem de marcação de texto, que serve para definir quais informações sua página irá exibir. Essas marcações de texto são feitas através das tags, que dizem para o navegador o que significa cada informação inserida no documento HTML:

```html
<h1>Título</h1>
<p>Parágrafo</p>
```

Para criarmos nossa página, copie e cole o seguinte código:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha página</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>JSLadies RJ</p>
</body>
</html>
```

- `<!DOCTYPE html>` - tag que avisa aos browsers qual é o tipo de documento que está sendo renderizado.
- `<html>` - tag que define o início do documento, indicando ao navegador que todo o conteúdo dentro dele é um código HTML.
- `<head>` - tag de cabeçalho, que traz informações sobre o documento que está sendo aberto.
- `<title>` - tag que indica o título do seu documento.
- `<body>` - tag que indica o corpo do documento, que engloba toda a parte visível pelo navegador. É aqui que colocamos os textos, imagens, links etc.

Note que o seu código ficará muito mais legível se você colocar o conteúdo dentro da tag `<body>` em outras linhas. É muito importante dar **tab** ou **4 espaços**, pois assim você simboliza que os conteúdos do `<h1>` e do `<p>` estão dentro da tag `<body>`. Essa estrutura se chama **indentação**.


## Adicionando conteúdo

### Títulos

No HTML temos seis tipos de marcações específicas para títulos:

```html
<h1>Título nível 1</h1>
<h2>Título nível 2</h2>
<h3>Título nível 3</h3>
<h4>Título nível 4</h4>
<h5>Título nível 5</h5>
<h6>Título nível 6</h6>
```

Note que quanto menor o número, menor e menos importante será o título dentro do documento. Logo, o exemplo acima ficará assim:

# Título nível 1
## Título nível 2
### Título nível 3
#### Título nível 4
##### Título nível 5
###### Título nível 6

Obs: não confundir as tags de títulos com a tag `<title>`. Enquanto a tag `<title>` define o título que irá ser exibido na barra de título dos navegadores, as tags de `<h1>` a `<h6>` representam as marcações de títulos que são exibidos dentro do documento HTML.

### Parágrafo

A marcação que indica um parágrafo é representada pela tag `<p>`:

```html
<p>
  Este site é um portfólio de minhas habilidades e experiências.
</p>
```

Resultado:

Este site é um portfólio de minhas habilidades e experiências.

### Formatação

Existem diversas tags de formatação de texto no HTML. Segue abaixo uma lista das que são mais usadas:

- `<b>` - <b>negrito</b>
- `<i>` - <i>itálico</i>
- `<u>` - <u>sublinhado</u>
- `<mark>` - <mark>marcado</mark>
- `<small>` - <small>pequeno</small>
- `<del>`  ou `<s>`- <s>riscado</s>

Vale lembrar que podemos usar essas tags de formatação dentro dos títulos e dos parágrafos:

```html
<h2>
    <b>Hello, World em negrito</b>
</h2>
<p>
    <i>JSLadies RJ em itálico</i>
</p>
```

Resultado:

<h2>
    <b>Hello, World em negrito</b>
</h2>
<p>
    <i>JSLadies RJ em itálico</i>
</p>

### Listas

#### Listas não-enumeradas

Listas não enumeradas são marcadas pela tag `<ul>`. Já cada item dessa lista é marcado pela tag `<li>`:

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


#### Listas enumeradas

Em listas enumeradas usamos a tag `<ol>` ao invés de `<ul>`. Cada item dentro dessa lista é marcado pela tag `<li>`:

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


### Tabelas

Tabelas usam a tag `<table>`. Já a tag `<tr>` define uma linha dessa tabela, enquanto `<td>` define uma célula.

Para definir o cabeçalho da tabela, usamos a tag `<th>`:

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

Para linkar textos usamos a tag `<a>`. Essa tag possui um atributo `href`, que receberá a url de destino. Já o nome do link ficará dentro da marcação:

```html
<a href="http://fb.com">Facebook</a>
<a href="http://google.com">Google</a>
<a href="http://github.com">Github</a>
```

Resultado:

[Facebook](http://fb.com)
[Google](http://google.com)
[Github](http://github.com)


### Imagens

Para adicionar imagens no documento, usamos a tag `<img>`. Ela receberá um atributo `src` com a url ou o caminho da imagem. 

```html
<img src="https://avatars1.githubusercontent.com/u/28883362?s=200&v=4" />
```

Resultado:

![https://avatars1.githubusercontent.com/u/28883362?s=200&v=4](https://avatars1.githubusercontent.com/u/28883362?s=200&v=4)

Ao contrário das outras tags que já vimos até agora, a tag `<img>` não possui uma tag específica para fechamento. Neste caso, ela poderá ser fechada de maneira diferente das demais, bastando apenas colocar uma barra no final.

## Montando o portfólio

Juntando tudo o que nós vimos até agora, já podemos fazer algo assim:

![Exemplo](imgs/cap2-exemplo.png)

Você pode usar esse exemplo de referência:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha página</title>
</head>
<body>
    <img src="http://vidadiaria.com.br/images/2017/educacao/agosto/estudante3.jpg">
    <h1>Maria Lúcia do Carmo</h1>
    <h3>Estudante de ciência da computação</h3>

    <p>Brasileira, solteira, 22 anos - Rio de Janeiro - RJ<p>
    <a href="http://fb.com">Facebook</a> - <a href="http://github.com">Github</a> - <a href="http://twitter.com">Twitter</a>
    <p><b>Email:</b> maria@gmail.com</p>
    <p><b>Phone:</b> (21) 98765-4321</p>

    <h4>Experiência</h4>
    <p><i>2017/06 ~ atual</i> - estágiaria no Facebook - <a href="http://fb.com">Facebook.com</a></p>

    <h4>Educação</h4>
    <p> Bacharelado em ciência da computação - <i>cursando</i> - UFRJ</p>

    <h4>Habilidades</h4>
    <ul>
      <li>HTML5 / CSS3</li>
      <li>Fazer café</li>
    </ul>

    <h4>Interesses</h4>
    <ul>
      <li>Estudar</li>
    </ul>
</body>
</html>
```

Com HTML podemos também adicionar áudio, vídeo, canvas, formulários, dentre muitas outras coisas. No [final do curso](final.md) temos vários links com tutoriais e guias pra esse conteúdo remanescente.

## Seu primeiro commit

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

Clique em configurações no lado direito da pagina do seu repositório no Github e na parte chamada **Github Pages** selecione a branch `master`. Assim, todas as modificações que forem feitas no seu projeto dentro deste repositório vão ser publicadas na url `NOMEDASUACONTA.github.io`.

![Exemplo configuração de github pages](imgs/cap1-config.png)

Se você receber uma mensagem como `Your site is ready to be published at http://NOMEDASUACONTA.github.io/.`
é porque tudo está ok.

Agora se você acessar o link [https://NOMEDASUACONTA.github.io](https://NOMEDASUACONTA.github.io), você verá o conteúdo do seu site! Demora alguns minutos para as mudanças realmente irem ao ar, mas em pouco tempo será possível ver as suas modificações.

#### [Ir para o passo 3](chapter3.md)