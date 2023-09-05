# Introdução ao CSS
CSS ou Cascading Style Sheets é uma linguagem de estilo utilizada para definir a apresentação de documentos escritos em uma linguagem de marcação, como HTML ou XML. O CSS define como os elementos devem ser exibidos na tela, no papel, ou em outras mídias.

## Sintaxe
A sintaxe do CSS é composta por um seletor e um bloco de declaração. O seletor aponta para o elemento HTML que será estilizado e o bloco de declaração contém uma ou mais declarações separadas por ponto e vírgula.

```css
seletor {
    propriedade: valor;
    propriedade: valor;
    propriedade: valor;
}
```
## Seletores
Os seletores são utilizados para selecionar os elementos que serão estilizados. Existem vários tipos de seletores, os mais comuns são:

### Seletor de tipo
Seleciona todos os elementos de um determinado tipo.

```css
p {
    color: red;
}
```
Se você se lembra do HTML, o elemento `<p>` é utilizado para criar parágrafos. O código acima irá selecionar todos os parágrafos e aplicar a cor vermelha.

Para nosso primeiro teste, dentro do arquivo `index.html` adicione o seguinte código:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Introdução ao CSS</title>
        <style>
            p {
                color: red;
            }
        </style>
    </head>
    <body>
        <p>Olá mundo!</p>
    </body>
</html>
```
Salve o arquivo e abra-o no navegador. Você deve ver o texto "Olá mundo!" em vermelho.

#### Tag Style
O código acima funciona, mas não é a melhor forma de utilizar o CSS. O ideal é que o CSS seja separado do HTML. Mas por enquanto vamos continuar utilizando o CSS dentro do HTML e a melhor forma de fazer isso é utilizando a tag `<style>`.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Introdução ao CSS</title>
        <style>
            body {
                background-color: #ccc;
            }
            p {
                color: red;
            }
        </style>
    </head>
    <body>
        <p>Olá mundo!</p>
    </body>
</html>
```
Perceba que usei o seletor `body` para alterar a cor de fundo da página e o seletor `p` para alterar a cor do parágrafo.

Com CSS podemos estilizar qualquer elemento HTML, para isso basta utilizar o seletor correto. Por exemplo, para estilizar um elemento `<h1>` basta utilizar o seletor `h1`.

```css
h1 {
    color: blue;
}
```
#### CSS inline
Outra forma de utilizar o CSS é utilizando o atributo `style` dentro da tag HTML. Essa forma não é recomendada, mas é importante conhecer.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Introdução ao CSS</title>
    </head>
    <body>
        <p style="color: red;">Olá mundo!</p>
    </body>
</html>
```
Perceba que o style é um atributo da tag `<p>` e que o valor do atributo é um código CSS.

#### CSS externo
A forma mais recomendada de utilizar o CSS é utilizando um arquivo externo. Para isso basta criar um arquivo com a extensão `.css` na mesma pasta do arquivo HTML e adicionar o seguinte código:

```css
p {
    color: red;
}
```
Agora dentro do arquivo HTML basta adicionar o seguinte código:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Introdução ao CSS</title>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <p>Olá mundo!</p>
    </body>
</html>
```
O atributo `href` da tag `<link>` recebe o caminho do arquivo CSS.

A tag `<link>` é utilizada para carregar arquivos externos, como arquivos CSS, fontes e outros arquivos. E sempre deve ser adicionada dentro da tag `<head>`.

Lembre-se que o arquivo CSS deve estar na mesma pasta do arquivo HTML ou você deve informar o caminho correto.

> Dica: Para criar um arquivo CSS no VS Code basta clicar com o botão direito do mouse na pasta e selecionar a opção "Novo arquivo".

Agora podemos voltar a falar sobre seletores.

### Seletor de classe
Seleciona todos os elementos que possuem o atributo `class` com o valor especificado.

```css
.classe {
    color: red;
}
```
Para utilizar esse seletor basta adicionar o nome da classe no atributo `class` do elemento HTML.

```html
<p class="classe">Olá mundo!</p>
```
### Seletor de ID
Seleciona um elemento que possui o atributo `id` com o valor especificado.

```css
#id {
    color: red;
}
```
Para utilizar esse seletor basta adicionar o nome do ID no atributo `id` do elemento HTML.

```html
<p id="id">Olá mundo!</p>
```
Mas a final o que é uma classe e o que é um ID?

#### Classe
Uma classe é um atributo HTML que pode ser utilizado em vários elementos para aplicar o mesmo estilo.

Por exemplo, podemos criar uma classe chamada `vermelho` e utilizar ela em vários elementos.

```css
.vermelho {
    color: red;
}
```
```html
<p class="vermelho">Olá mundo!</p>
<p>Olá mundo!</p>
<h1 class="vermelho">Olá mundo!</h1>
<h1>Olá mundo!</h1>
```
Perceba que a cor vermelha foi aplicada apenas nos elementos que possuem a classe `vermelho`.

#### ID
Um ID é um atributo HTML que deve ser utilizado apenas uma vez na página.

Em tese ele funciona igual a uma classe, mas deve ser um identificador único do elemento.

```css
#vermelho {
    color: red;
}
```
```html
<p id="vermelho">Olá mundo!</p>
<p>Olá mundo!</p>
```
Perceba que a cor vermelha foi aplicada apenas no elemento que possui o ID `vermelho`.

### Seletor de descendente
Seleciona todos os elementos que são descendentes de um elemento especificado.

```css
elemento1 elemento2 {
    color: red;
}
```
```html
<div>
    <p>Olá mundo!</p>
</div>
```
No exemplo acima o elemento `<p>` é descendente do elemento `<div>`, então o texto "Olá mundo!" será exibido em vermelho.

> Dica: O seletor de descendente é muito utilizado para estilizar elementos dentro de uma lista. 

### Seletor de filho
Seleciona todos os elementos que são filhos de um elemento especificado.

```css
elemento1 > elemento2 {
    color: red;
}
```
```html
<div>
    <p>Olá mundo!</p>
</div>
```

No exemplo acima o elemento `<p>` é filho do elemento `<div>`, então o texto "Olá mundo!" será exibido em vermelho.

### Seletor de atributo
Seleciona todos os elementos que possuem o atributo especificado.

```css
a[target] {
    color: red;
}
```
```html
<a href="https://www.google.com" target="_blank">Google</a>
```
No exemplo acima a cor vermelha será aplicada apenas nos links que possuem o atributo `target`.

### Seletor de atributo com valor
Seleciona todos os elementos que possuem o atributo especificado com o valor especificado.

```css
a[target="_blank"] {
    color: red;
}
```
```html
<a href="https://www.google.com" target="_blank">Google</a>
```
No exemplo acima a cor vermelha será aplicada apenas nos links que possuem o atributo `target` com o valor `_blank`.

> Fonte do contéudo: [MDN](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_selectors)

## Comentários
Os comentários são utilizados para adicionar anotações no código. Eles não são interpretados pelo navegador e não afetam o código.

```css
/* Esse é um comentário */

/* 
    Esse é um comentário
    de várias linhas
*/

body {
    background-color: #ccc; /* Esse é um comentário */
}
```

## Propriedades
As propriedades são utilizadas para definir o estilo dos elementos. Existem várias propriedades, as mais comuns são:

### Cor
A propriedade `color` é utilizada para definir a cor do texto.

```css
p {
    color: red;
}
```
### Cor de fundo
A propriedade `background-color` é utilizada para definir a cor de fundo do elemento.

```css
body {
    background-color: #ccc;
}
```
### Fonte
A propriedade `font-family` é utilizada para definir a fonte do texto.

```css
p {
    font-family: Arial;
}
```
### Tamanho da fonte
A propriedade `font-size` é utilizada para definir o tamanho da fonte.

```css
p {
    font-size: 16px;
}
```
### Alinhamento
A propriedade `text-align` é utilizada para definir o alinhamento do texto.

```css
p {
    text-align: center;
}
```
### Largura
A propriedade `width` é utilizada para definir a largura do elemento.

```css
p {
    width: 100px;
}
```
### Altura
A propriedade `height` é utilizada para definir a altura do elemento.

```css
p {
    height: 100px;
}
```
### Margem
A propriedade `margin` é utilizada para definir a margem do elemento.

```css
p {
    margin: 10px;
}
```
### Margem superior
A propriedade `margin-top` é utilizada para definir a margem superior do elemento.

```css
p {
    margin-top: 10px;
}

/* ou */

p {
    margin: 10px 0 0 0;
}
```
> Dica: A propriedade `margin` recebe 4 valores, o primeiro é a margem superior, o segundo é a margem direita, o terceiro é a margem inferior e o quarto é a margem esquerda.

### Margem direita
A propriedade `margin-right` é utilizada para definir a margem direita do elemento.

```css
p {
    margin-right: 10px;
}

/* ou */

p {
    margin: 0 10px 0 0;
}
```
### Margem inferior
A propriedade `margin-bottom` é utilizada para definir a margem inferior do elemento.

```css
p {
    margin-bottom: 10px;
}

/* ou */

p {
    margin: 0 0 10px 0;
}
```
### Margem esquerda
A propriedade `margin-left` é utilizada para definir a margem esquerda do elemento.

```css
p {
    margin-left: 10px;
}

/* ou */

p {
    margin: 0 0 0 10px;
}
```
### Espaçamento interno
A propriedade `padding` é utilizada para definir o espaçamento interno do elemento.

```css
p {
    padding: 10px;
}
```
### Espaçamento interno superior
A propriedade `padding-top` é utilizada para definir o espaçamento interno superior do elemento.

```css
p {
    padding-top: 10px;
}

/* ou */

p {
    padding: 10px 0 0 0;
}
```
Como você deve ter percebido, a propriedade `padding` funciona igual a propriedade `margin` então não vou repetir os exemplos.

### Bordas
A propriedade `border` é utilizada para definir as bordas do elemento.

```css
p {
    border: 1px solid red;
}
```
O código acima irá criar uma borda de 1px com a cor vermelha.

O primeiro valor é a largura da borda, o segundo valor é o estilo da borda e o terceiro valor é a cor da borda.

### Estilos de bordas
Existem vários estilos de bordas, os mais comuns são:
- `solid`: Cria uma borda sólida.
- `dotted`: Cria uma borda pontilhada.
- `dashed`: Cria uma borda tracejada.
- `double`: Cria uma borda dupla.
- `groove`: Cria uma borda em relevo.
- `ridge`: Cria uma borda em alto relevo.
- `inset`: Cria uma borda em 3D.
- `outset`: Cria uma borda em 3D.

### Tamanhos
Os tamanhos podem ser definidos em pixels, em porcentagem ou em outras unidades de medida.

#### Unidades de medida
As unidades de medida mais comuns são:

- `px`: Pixels.
- `em`: Tamanho da fonte do elemento.
- `rem`: Tamanho da fonte do elemento raiz.
- `vw`: Porcentagem da largura da tela.
- `vh`: Porcentagem da altura da tela.

> Dica: Para definir o tamanho da fonte do elemento raiz basta adicionar o seguinte código no CSS: `html { font-size: 16px; }`.

### Exemplo
Agora que você já conhece os seletores e as propriedades, vamos criar um exemplo.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Introdução ao CSS</title>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <h1>Introdução ao CSS</h1>
        <p>Esse é apenas um exemplo de como utilizar o CSS.</p>
        <p>Esse será o segundo parágrafo do nosso site.</p>
    </body>
</html>
```
```css
body {
    background-color: #ccc;
    font-family: Arial;
}

h1 {
    color: blue;
    text-align: center;
}

p {
    color: red;
    text-align: justify;
    margin: 10px;
}
```
Salve os arquivos e abra o arquivo HTML no navegador para ver o resultado.

Claro que nessa aula não chegamos nem perto de conhecer todas as propriedades do CSS, vamos aprender mais sobre isso nas próximas aulas.

## Exercícios
Agora que você já conhece os seletores e as propriedades, vamos praticar um pouco.

Teste todos os seletores e propriedades que você aprendeu até agora e debata com seus colegas sobre o que você aprendeu.

## Referências
- https://developer.mozilla.org/pt-BR/docs/Learn/CSS

< [Voltar para o Índice](../../README.md) | Próxima Aula >