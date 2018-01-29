## Passo 3

#### Indice
- [O que é CSS](#o-que-e-css)
- [Estilizando o HTML](#estilizando-o-html)
- [Seu segundo commit](#seu-segundo-commit)

## Estilizando com CSS

## O que e CSS

**CSS** vem de **Cascading Stylesheets**, que não é realmente uma linguagem de programação. É uma linguagem de folhas de estilos. Que são códigos contam pro browser de que forma você quer mostrar as tags HTML, mudando sua aparencia, posição, etc e estilizar seletivamente os elementos no documentos HTML. 

## Estilizando o HTML

Clique em **"File/New File"**, uma nova aba vai abrir no editor.
Tecle **Crtl + S** ou então clique em **"File/Save as..."** e mude o Filename para **style.css** e clique no botão verde de **Save**.

No style.css cole:
```css
body {
    background-color: red;
    font-family: "Gill Sans Extrabold", sans-serif;
}
```

O que isso quer dizer? Tudo dentro do nosso body ficará com cor de background vermelho. O background pode ser uma cor em ingles, uma cor em hexadecimal e até uma imagem. E a fonte de tudo dentro do body vai será *"Gill Sans Extrabold"*

O body é o nosso **seletor**, ou seja, selecionamos tudo que está dentro do body. O que está entre parenteses é a **declaração**, nela temos a **propriedade** e o valor dela seguido do `:`. Cada propriedade deve ter um `;` no final para representar o fim da linha.

Agora, é necessário importar esse arquivo CSS dentro do nosso HTML para que os estilos funcionem.
Pra isso, dentro do `<head>` cole esta linha `<link rel="stylesheet" type="text/css" href="style.css">`

```html
<head>
    <title>Minha Pagina</title>
       <link rel="stylesheet" type="text/css" href="style.css">
</head>
```

Clique no botão verde de **Run**. Logo abaixo no terminal e ao entrar no link verifique se o fundo está de fato vermelho.

![Exemplo do estado atual](imgs/cap3-css.png)

### Mais CSS

#### Fontes e Cores
Cores podem ser em hexadecimal os nomes defaults do CSS que você pode ver aqui: [https://www.w3schools.com/colors/colors_names.asp](https://www.w3schools.com/colors/colors_names.asp).

Ou você pode selecionar sua cor em hexadecinal aqui: [https://www.w3schools.com/colors/colors_picker.asp](https://www.w3schools.com/colors/colors_picker.asp).

Anteriormente definimos o background como **red** mas podemos também usar o seu valor hexadecimal **#FF0000**:

```css
body {
  background-color: #FF0000;
}
```

Para modificar as caracteristicas de todos os paragrafos podemos usar diversas propriedades:

```css
p {
  font-size: 20px;
  color: darkgray;
  font-family: Arial;
  font-style: bold;
  text-align: center;
  line-height: 2;
  letter-spacing: 1px;
  text-align: center;
  text-shadow: 3px 3px 1px black;
}
```
- **font-size** é o tamanho da fonte em pixels.
- **color** é a cor do texto.
- **font-family** é a fonte do texto.
- **font-style** é propriedades como negrito ou italico.
- **line-height** é a altura da letra.
- **letter-spacing** é o espaçamento das letras.
- **text-align** é o alinhamento do texto.
- **text-shadow** sombra do texto.

**Não precisa usar todas!!**


#### Selecionando elementos HTML

Para não selecionarmos sempre a propria tag html devemos usar uma propriedade `class` dentro de todos os elementos html que queremos selecionar.
Assim podemos nomear o que o conteúdo é e pela propria nomemclatura de `class` o selecionamos e estilizamos.

No css colocamos um ponto e o nome da classe para definir os estilos da classe.

HTML:
```html
<p class="titulo">Titulo</p>
<img class="logo" src="url">
```

```css
.titulo {
  font-size: 30px;
}
.logo {
  width: 300px;
}
```

No exemplo, criamos as classes **"titulo"** pra uma tag `<p>` e **"logo"** para uma imagem. Isso possibilita que possamos estilizar esses elementos especificos. Todo elemento que tiver classe **titulo** terá tamanho de fonte 30px, e todo elemento que tiver classe **logo** terá tamanho de 300px.

É importante usar classes pois podemos também reutilizar estilos e definir o que cada coisa é. Lembrando que cada elemento pode ter mais de uma classe.

#### Background

```css
body {
   background-image: url("https://i2.wp.com/likecoaching.com.br/wp-content/uploads/2016/11/Fundo-Estrelas.jpg");
   background-repeat: no-repeat, repeat
   background-color: #cccccc;
}
```


Gradiente
```css
body {
   background-color: #cccccc;  
   background-image: linear-gradient(red, yellow);
}
```

#### Tamanho

Uma coisa que você vai notar sobre escrever CSS é que um bocado disso é sobre caixas — indicar seu tamanho, cor, posição, etc. Muitos dos elementos HTML da sua página podem ser pensados como caixas umas em cima das outras.
Como esperado, o layout CSS é baseado principalmente no modelo de caixas. Cada um dos blocks que ocupam espaço na sua página tem propriedades como essas:

<img src="imgs/cap3-pad.png" alt="Exemplo de padding e border">

- **padding**: o espaço ao redor do conteúdo (ex.: ao redor do texto de um parágrafo)
- **border**: a linha sólida do lado de fora do padding
- **margin**: o espaço externo a um elemento

Pra isso vamos criar uma caixa com algum texto.

```html
<div class="box">
  <p>Campus Party 2018</p>
</div>
```

Se pintarmos a caixinha de azul, podemos ver mais claramente sua caixinha.

```css
.box {
  background-color: blue;
}
```
E a caixinha do texto está mais ou menos assim:

<div style="background-color: blue;" class="box">
  <p>Campus Party 2018</p>
</div>

O padding no css, representa o que está ao redor do conteudo antes da borda, então de aumentarmos para 10px ficará visivel o espaço que até então estava zerado.

```css
.box {
  background-color: blue;
  padding: 10px;
}
```

Fica algo assim:

<div style="background-color: blue;padding: 10px;" class="box">
  <p>Campus Party 2018</p>
</div>

O padding pode receber 4 valores como espaço no conteúdo. Se fosse `padding: 0 20px 20px 20px;` — nós não estamos indicando padding no topo do corpo, e 20 pixels na esquerda, chão e direita. Os valores do padding são topo, direita, chão, esquerda, nessa ordem.

Podemos ajustar o tamanho da altura e largura da caixinha

```css
.box {
  background-color: gray;
  padding: 10px;
  height: 80px;
  width: 100px;
}
```

Mudando pra cinza, temos um resultado bem legal

<div style="background-color: gray;padding: 10px;height: 80px;width: 100px;" class="box">
  <p>Campus Party 2018</p>
</div>


#### Deixando redondo

Para arredondar objetos usa-se a propriedade border-radius em que "arredondamos" as bordas do elemento:

```css
.avatar{
  border-radius: 50%;
}
```

Supondo que temos um avatar de cachorro:
```html
<img class="avatar" src="imgs/cap3-dog.jpeg" alt="Avatar do cachorro">
```

A medida é em porcentagem de arredondamento e 50% equivale a um circulo, tendo este resultado:

<img class="avatar" style="border-radius: 50%;width:150px;" src="imgs/cap3-dog.jpeg" alt="Avatar do cachorro">

#### Centralizando uma imagem

```css
img {
  border-radius: 50%;
  display: block;
  margin: 0 auto;
}
```
 Então, para aplicar margens a uma imagem, nós temos que dar a ela um comportamento de bloco usando `display: block;`.

Resultando em:

<img class="avatar" style="border-radius: 50%;width:150px;display: block;margin: 0 auto;" src="imgs/cap3-dog.jpeg" alt="Avatar do cachorro">

#### Estilizando Bordas

Como já vimos, todo elemento tem padding, border e margin. Podemos estilizar suas bordas.
A borda recebe 3 valores, o seu tamanho, estilo e cor.

```css
img {
  border-radius: 50%;
  display: block;
  margin: 0 auto;
  border: 2px solid black;
}
```
No exemplo, acriamos uma borda de 2px, solida de cor preta.
Resultando em:

<img class="avatar" style="border: 2px solid black;border-radius: 50%;width:150px;display: block;margin: 0 auto;" src="imgs/cap3-dog.jpeg" alt="Avatar do cachorro">


#### Posicionamento

A propriedade de float é usada para posicionamento e layout

```css
.avatar {
  float: left;
}
```

Seus valores significam:
- **left** - O elemento flutua para a esquerda do seu container
- **right**- O elemento flutua para a direita do seu container
- **none** - O elemento não flutua
- **inherit** - O elemento herda de o float de seu elemento pai.

Podemos também posicionar pra esquerda, direita, cima e baixo por pixels:
```css
.avatar {
  top: 10px;
  left: 10px;
  right: 10px;
  bottom: 10px;
}
```

#### Exemplo

![Exemplo estilizado](imgs/cap3-exemplo.png)

Adicionando alguns estilos e classes no HTML anterior podemos chegar nesse resultado sem muitas linhas de código.
Usamos o *background-image* para criar um fundo gradiente e encapsulamos a biografia dentro de uma `<div>` com a classe `.bio`.

Nele, criamos uma caixinha de com 50% de largura e 90% de altura, pintamos o fundo de branco, alinhamos o texto para o centro e adicionamos uma borda solida e deixamos um padding de 30px na caixinha.

O avatar ficou com a classe `.avatar` e teve sua largura alterada para 300px, adicionamos uma leve borda circular e flutuamos a imagem pra esquerda.

Criamos uma classe `.center` com as propriedades que centralizam blocos, assim, tudo que tiver a classe `center` estará centralizado.

```css
body {
    background-color: lightblue;
    background-image: linear-gradient(lightblue, rgb(93, 93, 192));
    font-family: "Gill Sans Extrabold", sans-serif;
    color: #383838;
    
}

.avatar {
    width: 300px;
    border-radius: 20%;
    float: left;
}

.bio {
    height: 90%;
    text-align: center;
    background: white;
    width: 50%;
    padding: 30px;
    border: 1px solid gray;
}

.center {
    display: block;
    margin: 0 auto;
}

.content {
    margin: 70px;
}
```

Adicionando suas respectivas classes no HTML:

```html

<!DOCTYPE html>
<html>
<head>
    <title>Minha Pagina</title>
    <link rel="stylesheet" type="text/css" href="main.css">
</head>
<body>
    <div class="bio center">
      <h1>Maria Lúcia do Carmo</h1>
      <img class="avatar center" src="http://vidadiaria.com.br/images/2017/educacao/agosto/estudante3.jpg" alt="Foto da Maria Lúcia">
      
      <h2>Estudante de ciência da computação</h3>
      <p>Brasileira, solteira, 22 anos - São Paulo - SP<p>
      <a href="http://fb.com">Facebook</a> - <a href="http://github.com">Github</a> - <a href="http://twitter.com">Twitter</a>

      <div class="content">
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
      </div>
    </div>
</body>
</html>

```

## Seu segundo commit

Repita o mesmo procedimento anterior:
```bash
# Verifique status do repositório
git status
# Adiciona todos os arquivos modificados p/ staging
git add *
# Ou individualmente
git add style.css
git add index.html
# Faz commit
git commit -m "Adicionando estilos"
# Adiciona modificações
git push
```

Escrever o que foi desenvolvido para cada commit é muito importante pois ajuda pode te guiar e também ajudar ao grupo de pessosas trabalhando no mesmo projeto ao verificar o que foi desenvolvido em cada passo do projeto.

#### [Ir para o passo 4](chapter4.md)
