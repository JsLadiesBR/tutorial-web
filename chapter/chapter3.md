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

##### Fontes e Cores
Cores podem ser em hexadecimal os nomes defaults do CSS que você pode ver aqui: [https://www.w3schools.com/colors/colors_names.asp](https://www.w3schools.com/colors/colors_names.asp).
Ou você pode selecionar sua cor em hexadecinal aqui: [https://www.w3schools.com/colors/colors_picker.asp](https://www.w3schools.com/colors/colors_picker.asp).

Anteriormente definimos o background como **red** mas podemos também usar o seu valor hexadecimal **#FF0000**

```css
body {
  background-color: #FF0000;
}
```

Para modificar as caracteristicas de todos os paragrafos podemos:

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
}
```
- **font-size** é o tamanho da fonte em pixels.
- **color** é a cor do texto.
- **font-family** é a fonte do texto.
- **font-style** é propriedades como negrito ou italico.
- **line-height** é a altura da letra.
- **letter-spacing** é o espaçamento das letras.
- **text-align** é o alinhamento do texto.

##### Selecionando elementos HTML

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

##### Background

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

##### Tamanho

```css
.box {
  width: 300px;
  height: 500px;
}
```

500px de altura e 300px de largura.

##### Bordas

##### Deixando redondo
Para arredondar objetos usa-se a propriedade border radius

.avatar{
  border-radius: 50%;
}

A medida é em porcentagem de arredondamento e 50% equivale a um circulo.

##### Posicionamento
left right float

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

#### [Ir para o conteúdos de estudo](final.md)
