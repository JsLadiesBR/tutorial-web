## Passo 3

#### Indice
- [O que é CSS](#o-que-e-css)
- [Estilizando o HTML](#estilizando-o-html)
- [Seu segundo commit](#seu-segundo-commit)

## Estilizando com CSS

## O que e CSS

blablablala explicar melhor
CSS contra pro browser de que forma você quer mostrar as tags html, mudando sua aparencia, posição, etc. 

https://i.ytimg.com/vi/EZ7la-hMNuk/maxresdefault.jpg

https://developer.mozilla.org/pt-BR/docs/Aprender/Getting_started_with_the_web/CSS_basico

#### [Guia CSS](guide.md)

## Estilizando o HTML

Clique em **"File/New File"**, uma nova aba vai abrir no editor.
Tecle **Crtl + S** ou então clique em **"File/Save as..."** e mude o Filename para **main.css** e clique no botão verde de **Save**.

No main.css cole:
```css
body {
    background-color: red;
    font-family: "Gill Sans Extrabold", sans-serif;
}
```

O que isso quer dizer? Tudo dentro do nosso body fica com cor de background vermelho. O background pode ser uma cor em ingles, uma cor em hexadecimal e até uma imagem.
E a fonte de tudo dentro do body vai ser a definida pelo css.

Agora, é necessário importar esse arquivo CSS dentro do nosso HTML para que os estilos funcionem.
Pra isso, dentro do `<head>` cole esta linha `<link rel="stylesheet" type="text/css" href="main.css">`

Clique no botão verde de **Run**. Logo abaixo no terminal e ao entrar no link verifique se o fundo está de fato vermelho. Se sim, você está pronto pro seu segundo commit.s

##### Selecionando elementos HTML
##### Background
background color background img
##### Selecionando elementos com Id
##### Selecionando elementos com Class
##### Fontes e cores
size color font-family etc bold italic
##### Tamanho
##### Deixando redondo
width height
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
git add main.css
git add index.html
# Faz commit
git commit -m "Adicionando estilos"
# Adiciona modificações
git push
```

Escrever o que foi desenvolvido para cada commit é muito importante pois ajuda pode te guiar e também ajudar ao grupo de pessosas trabalhando no mesmo projeto ao verificar o que foi desenvolvido em cada passo do projeto.

#### [Ir para o conteúdos de estudo](final.md)