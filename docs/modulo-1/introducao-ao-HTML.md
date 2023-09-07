# Introdução ao HTML
Como você já viu na [introdução ao desenvolvimento Web](introducao-ao-desenvolvimento-web.md), o HTML é a linguagem de marcação que utilizamos para criar páginas Web. Neste módulo, você vai aprender os conceitos básicos do HTML e como utilizá-lo para criar páginas Web.

> O contéudo deste módulo foi baseado no site [HTML Standard](https://html.spec.whatwg.org/multipage/), que é a especificação oficial do HTML. O HTML Standard é um documento técnico e muito extenso, por isso, não é recomendado para iniciantes. Porém, se você quiser se aprofundar no HTML, recomendo que leia o HTML Standard.

## O que é o HTML?
HTML é a sigla para HyperText Markup Language, ou seja, Linguagem de Marcação de Hipertexto. O HTML é uma linguagem de marcação(e não de programação) utilizada para criar páginas Web. O HTML é a linguagem que utilizamos para estruturar o conteúdo de uma página Web.

E não se preocupe, você não precisa decorar o que significa cada uma das palavras que formam a sigla HTML. O importante é saber que o HTML é uma linguagem de marcação utilizada para criar páginas Web.

## História do HTML
O HTML foi criado em 1991 por Tim Berners-Lee, um físico britânico que trabalhava no CERN, o Laboratório Europeu de Física de Partículas. O HTML foi criado para ser uma linguagem simples e de fácil entendimento, para que qualquer pessoa pudesse criar páginas Web.

[Veja esse video para saber mais sobre a história do HTML](https://youtu.be/NSmapCNcSyI?si=8nPL0z7gl8MTyrDr&t=81) e inclusive recomendo que você assista a playlist completa do canal [Curso em Vídeo](https://www.youtube.com/playlist?list=PLHz_AreHm4dlAnJ_jJtV29RFxnPHDuk9o) que trás um curso completo de HTML5. (Conhecimento nunca é demais)

## Sintaxe do HTML
A sintaxe do HTML é a forma como escrevemos o HTML. O HTML é uma linguagem de marcação, ou seja, uma linguagem que utiliza marcações para definir a estrutura de um documento. As marcações do HTML são chamadas de tags.

As tags do HTML são escritas entre os símbolos `<` e `>`. Por exemplo, a tag para definir um título é escrita como `<h1>`. A tag para definir um parágrafo é escrita como `<p>`. A tag para definir uma imagem é escrita como `<img>`. E assim por diante.

## Estrutura básica do HTML
Toda página Web precisa ter uma estrutura básica para que o navegador consiga interpretar o seu conteúdo. A estrutura básica de uma página Web é formada por duas tags: `<html>` e `<body>`. A tag `<html>` é a tag que define o início do documento HTML. A tag `<body>` é a tag que define o corpo do documento HTML.

```html
<html>
  <body>
    <!-- Conteúdo da página -->
  </body>
</html>
```

Os arquivos HTML são salvos com a extensão `.html`. Por exemplo, `index.html`, `sobre.html`, `contato.html`, etc. 

Esses arquivos HTML são abertos no navegador e o navegador interpreta o conteúdo desses arquivos e exibe o conteúdo para o usuário. Podendo ser um texto, uma imagem, um vídeo, um formulário, e assim por diante.

> Se você ainda não tem um editor de código, recomendo que instale o [Visual Studio Code](https://code.visualstudio.com/). Ele é um editor de código gratuito e multiplataforma, ou seja, funciona no Windows, Linux e Mac. Além disso, ele possui diversos plugins que facilitam o desenvolvimento Web.

## Primeiro arquivo HTML
Vamos criar o nosso primeiro arquivo HTML. Abra o Visual Studio Code e crie um novo arquivo. Para criar um novo arquivo, clique no menu `File` e depois em `New File`. Ou utilize o atalho `Ctrl + N` no Windows ou `Cmd + N` no Mac.

Para que o navegador saiba que o arquivo se trata de um arquivo HTML5, você precisa adicionar no topo do arquivo a seguinte linha de código:

```html
<!DOCTYPE html>
```
Ele define o conjunto de regras e padrões que o navegador deve seguir ao processar e exibir a página HTML, garantindo a compatibilidade e a consistência na exibição em diferentes navegadores.

Agora, vamos adicionar a estrutura básica do HTML no arquivo. Digite o seguinte código no arquivo:

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>Meu primeiro arquivo HTML</h1>
  </body>
</html>
```
Mas o que é esse código? Vamos analisar linha por linha.

A primeira linha é a declaração do tipo de documento. Ela é escrita como `<!DOCTYPE html>`. Essa declaração informa ao navegador que o arquivo é um documento HTML na versão 5.

A segunda linha é a tag `<html>`. Essa tag define o início do documento HTML. Tudo que estiver dentro dessa tag é considerado conteúdo HTML.

A terceira linha é a tag `<body>`. Essa tag define o corpo do documento HTML. Tudo que estiver dentro dessa tag é considerado conteúdo do corpo do documento HTML.

A quarta linha é a tag `<h1>`. Essa tag define um título. O número 1 indica que é um título de primeiro nível. O HTML possui 6 níveis de títulos, sendo o 1 o maior e o 6 o menor.

A quinta linha é o fechamento da tag `<body>`. Essa tag indica o fim do corpo do documento HTML.

A sexta linha é o fechamento da tag `<html>`. Essa tag indica o fim do documento HTML.

Agora, salve o arquivo usando o atalho `Ctrl + S` no Windows ou `Cmd + S` no Mac.
Navegue até a pasta `curso-fullstack` e crie uma pasta chamada `modulo1`, dentro dessa pasta, crie outra pasta chamada `meu-site`. Salve o arquivo com o nome `index.html` dentro da pasta `meu-site`.

> É uma boa prática criar uma pasta para cada projeto. Dentro dessa pasta, você pode criar outras pastas para organizar os arquivos do projeto. Por exemplo, uma pasta para os arquivos HTML, uma pasta para os arquivos CSS, uma pasta para os arquivos JavaScript, etc.

Agora, abra o arquivo `index.html` no navegador. Para abrir o arquivo no navegador, você pode ir até a pasta pelo gerenciador de arquivos e clicar duas vezes no arquivo. Ou use [essa extensão do Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) para abrir o arquivo no navegador.

Para instalar o Live Server, clique no link acima e depois clique no botão `Install`. Depois de instalar, clique no botão `Reload` para reiniciar o Visual Studio Code. Agora, abra o arquivo `index.html` no Visual Studio Code e clique no botão `Go Live` no canto inferior direito da tela. O navegador será aberto com o arquivo `index.html` e sempre que você salvar o arquivo, o navegador será atualizado automaticamente.

Mas lembre-se de salvar o arquivo antes de atualizar o navegador. Para salvar o arquivo, use o atalho `Ctrl + S` no Windows ou `Cmd + S` no Mac.

## Head
O HTML possui duas seções principais: `<head>` e `<body>`. A seção `<head>` é utilizada para definir informações sobre o documento HTML. Por exemplo, o título da página, o autor da página, a codificação de caracteres, etc.

A seção `<head>` é escrita entre as tags `<head>` e `</head>` e fica localizada antes da seção `<body>`. Por exemplo:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Meu primeiro arquivo HTML</title>
  </head>
  <body>
    <h1>Meu primeiro arquivo HTML</h1>
  </body>
</html>
```
A tag `<title>` é utilizada para definir o título da página. O título da página é exibido na aba do navegador. Por exemplo:

```html
<title>Semana do HTML</title>
```

> O head é uma seção muito importante do HTML, porém, não vamos nos aprofundar nela agora. Por enquanto, vamos aprender apenas o básico.

## Principais tags do HTML
Agora que você já sabe como criar um arquivo HTML, vamos aprender as principais tags do HTML. As tags do HTML são divididas em duas categorias: tags de conteúdo e tags de formatação.

### Parágrafo
A tag `<p>` é utilizada para definir um parágrafo. Por exemplo:

```html
<p>Este é um parágrafo.</p>
```

### Títulos
O HTML possui 6 níveis de títulos, sendo o 1 o maior e o 6 o menor. Os títulos são definidos pelas tags `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` e `<h6>`. Por exemplo:

```html
<h1>Título 1</h1>
<h2>Título 2</h2>
<h3>Título 3</h3>
<h4>Título 4</h4>
<h5>Título 5</h5>
<h6>Título 6</h6>
```
Lembre-se dessa hierarquia de títulos, pois ela é muito importante para a acessibilidade da página e para o SEO que veremos mais adiante.

### Formatação de texto
O HTML possui diversas tags para formatação de texto. As principais são: `<strong>`, `<em>`, `<mark>`, `<del>`, `<ins>`, `<sub>` e `<sup>`. Por exemplo:

```html
<p>Este é um texto <strong>forte</strong>.</p>
<p>Este é um texto <em>enfatizado</em>.</p>
<p>Este é um texto <mark>marcado</mark>.</p>
<p>Este é um texto <del>excluído</del>.</p>
<p>Este é um texto <ins>inserido</ins>.</p>
<p>Este é um texto <sub>subscrito</sub>.</p>
<p>Este é um texto <sup>sobrescrito</sup>.</p>
```
#### O resultado será:

Este é um texto **forte**.

Este é um texto _enfatizado_.

Este é um texto <mark>marcado</mark>.

Este é um texto ~~excluído~~.

Este é um texto <ins>inserido</ins>.

Este é um texto <sub>subscrito</sub>.

Este é um texto <sup>sobrescrito</sup>.

### Citação
A tag `<blockquote>` é utilizada para definir uma citação. Por exemplo:

```html
<blockquote>
  <p>Este é um texto citado.</p>
</blockquote>
```
#### O resultado será:

<blockquote>
  <p>Este é um texto citado.</p>
</blockquote>

### Lista não ordenada
A tag `<ul>` é utilizada para definir uma lista não ordenada. Por exemplo:

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```
#### O resultado será:

<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>

### Lista ordenada
A tag `<ol>` é utilizada para definir uma lista ordenada. Por exemplo:

```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>
```
#### O resultado será:

<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>

Como você já deve ter percebido, a tag `<li>` é utilizada para definir um item de uma lista. Por exemplo:

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>

<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>
```
As listas podem ser aninhadas, ou seja, uma lista dentro de outra lista. Por exemplo:

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>
    Item 3
    <ul>
      <li>Item 3.1</li>
      <li>Item 3.2</li>
      <li>Item 3.3</li>
    </ul>
  </li>
</ul>
```
#### O resultado será:

<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>
    Item 3
    <ul>
      <li>Item 3.1</li>
      <li>Item 3.2</li>
      <li>Item 3.3</li>
    </ul>
  </li>
</ul>

> As listas são bem mais complexas do que isso, mas por enquanto, vamos aprender apenas o básico.

### Imagem
A tag `<img>` é utilizada para definir uma imagem. Por exemplo:

```html
<img src="https://picsum.photos/200/300" alt="Imagem">
```
#### O resultado será:

<img src="https://picsum.photos/200/300" alt="Imagem">

A tag `<img>` possui dois atributos obrigatórios: `src` e `alt`. O atributo `src` é utilizado para definir o caminho da imagem. O atributo `alt` é utilizado para definir um texto alternativo para a imagem. Esse texto é exibido caso a imagem não seja carregada ou caso o usuário utilize um leitor de tela.

Mas o que é um leitor de tela? Um leitor de tela é um software que lê o conteúdo da tela para o usuário. Esse software é utilizado por pessoas com deficiência visual. Por isso, é muito importante definir um texto alternativo para as imagens.

### Atributos
> Não se preocupe se você não entendeu o que são atributos. Você vai aprender sobre eles mais adiante.

Os atributos são utilizados para definir informações adicionais sobre uma tag. Por exemplo, a tag `<img>` possui os atributos `src` e `alt`. O atributo `src` é utilizado para definir o caminho da imagem. O atributo `alt` é utilizado para definir um texto alternativo para a imagem.   

Os atributos são escritos dentro da tag. Por exemplo:

```html
<img src="https://picsum.photos/200/300" alt="Imagem">
```
Nesse exemplo, a tag `<img>` possui dois atributos: `src` e `alt`. O atributo `src` é utilizado para definir o caminho da imagem. O atributo `alt` é utilizado para definir um texto alternativo para a imagem.

### Link
A tag `<a>` é utilizada para definir um link. Por exemplo:

```html
<a href="https://google.com">Google</a>
```
#### O resultado será:

<a href="https://google.com">Google</a>

A tag `<a>` possui um atributo obrigatório: `href`. O atributo `href` é utilizado para definir o destino do link. Por exemplo, o link pode ser um endereço Web, um endereço de e-mail, um telefone, um arquivo, etc.

#### Exemplos de links:

```html
<a href="https://google.com">Esse é um link para o Google</a>
<a href="mailto:exemplo@gmail.com">Esse é um link para um e-mail</a>
<a href="tel:+5511999999999">Esse é um link para um telefone</a>
<a href="arquivo.pdf">Esse é um link para um arquivo</a>
```
Se atentou para o atributo `href`? Ele é utilizado para definir o destino do link. Por exemplo, o link pode ser um endereço Web, um endereço de e-mail, um telefone, um arquivo, e assim por diante.

Por último, vamos aprender como abrir um link em uma nova aba. Para abrir um link em uma nova aba, você precisa adicionar o atributo `target` na tag `<a>` e definir o valor `_blank`. Por exemplo:

```html
<a href="https://google.com" target="_blank">Google</a>
```
> Lembre-se de testar todos os exemplos no navegador para ver o resultado de cada um.

### Tabela
Todos nós já vimos uma tabela, seja em um site, em um documento ou em uma planilha. As tabelas são utilizadas para organizar dados em linhas e colunas. No HTML, as tabelas são definidas pela tag `<table>`. Por exemplo:

```html
<table>
  <tr>
    <th>Nome</th>
    <th>Idade</th>
  </tr>
  <tr>
    <td>João</td>
    <td>20</td>
  </tr>
  <tr>
    <td>Maria</td>
    <td>30</td>
  </tr>
</table>
```
#### O resultado será:

<table>
  <tr>
    <th>Nome</th>
    <th>Idade</th>
  </tr>
  <tr>
    <td>João</td>
    <td>20</td>
  </tr>
  <tr>
    <td>Maria</td>
    <td>30</td>
  </tr>
</table>

- A tag `<table>` é utilizada para definir uma tabela.
- A tag `<tr>` é utilizada para definir uma linha da tabela.
- A tag `<th>` é utilizada para definir um cabeçalho da tabela.
- A tag `<td>` é utilizada para definir uma célula da tabela.

> As tabelas são bem mais complexas do que isso, mas por enquanto, vamos aprender apenas o básico.

### Tag Div
A tag `<div>` é utilizada para definir uma área genérica no documento. Por exemplo:

```html
<div>
  <p>Este é um parágrafo dentro de uma div.</p>
</div>
```
A principal função da tag `<div>` é agrupar elementos HTML para que eles possam ser estilizados com CSS que veremos mais adiante.

Mas o que vimos até agora é apenas a ponta do iceberg. O HTML possui diversas outras tags. Porém, essas são as principais tags que você precisa conhecer para avançar nesse curso. [Aqui está o básico do HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element) para você consultar sempre que precisar.

< [Introdução ao Desenvolvimento Web](introducao-ao-desenvolvimento-web.md) | [Sumário](../README.md) | [Introdução ao CSS](introducao-ao-CSS.md) >