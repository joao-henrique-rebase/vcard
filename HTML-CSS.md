# HTML, CSS e JS
O intuito desse Mini Curso será aprender os conceitos básicos e os principais elementos do `HTML`, `CSS` e `JS`

Após isso vamos por a mão na massa e fazer nosso próprio carão de vista WEB.

Podemos brincar que `HTML` seria o "Esqueleto" do nosso corpo, o `CSS` seria a "Pele" e a "Maquiagem" talvez e já o `JAVASCRIPT` seria o "Músculos"

# Html

## O que é Html
É o acrónimo de `Hypertext Markup Language`, ou seja ela não é uma linguagem de programação e sim uma linguagem de marcação.
Vamos `Marcar` com `Tags` elas funcionam como comandos de formatação de textos, formulários, links, imagens, tabelas, entre outros.

Os browsers identificam as tags e apresentam conforme está especificada a marcação.

Vamos lá, estrutura básica de qualquer pagina Web.
```
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="utf-8">
<title>Título da página</title>
</head>
<body>
... aqui vai todo o conteudo visivel da sua pagina WEB...
</body>
</html>
```

### `<!DOCTYPE html>` 

- o doctype avisa aos browsers, robôs de busca, leitores de tela e outras coisas que tipo de documento e aquele que eles estao prestes a carregar, no nosso caso é `HTML`.

### `<html></html>`
- o elemento `html` envolve todo o conteúdo da página e às vezes é conhecido como o elemento raiz.

### `<head></head>`
- o elemento `<head>` age como um recipiente de tudo o que você deseja incluir em uma página HTML que não é o conteúdo que você quer mostrar para quem vê sua página, incluindo coisas como palavras-chave e uma descrição que você quer que apareça nos resultados de busca, CSS para dar estilo ao conteúdo, declarações de conjuntos de caracteres e etc...

### `<meta charset="utf-8">`
- esse elemento aponta qual conjunto de caracteres seu documento deve usar para o utf-8.

### `<title></title> `
- indica o título da sua página que aparece no topo de browser.

### `<body></body> `
- o elemento `<body>` contém o conteúdo que você quer mostrar ao público que visita sua página, seja texto, imagens, vídeos, jogos, faixas de áudio tocáveis ou seja lá o que for.


## TAGS

Que tal conhecermos as principais `Tags` de marcação do `HTML`


### Tags estruturais


#### `<!– –>`
- Cria um comentário.

#### `<html> </html>`
- Envolve todo um documento html.

#### `<head> </head>`
- Envolve o cabeçalho de um documento html.

#### `<meta >`
- Fornece informações gerais sobre o documento.

#### `<style> </style>`
- Informações de estilo.

#### `<script> </script>`
- Linguagem script.

#### `<title> </title>`
- O título do documento.

#### `<body> </body>`
- Envolve o corpo (texto e tags) do documento html.
- Aceita como atributos, por exemplo:
  - bgcolor – Cor de fundo.
  - background – Imagem como plano de fundo.
  - text – Cor do texto principal.

### `<footer></footer>`
- Define o rodapé de uma página.

### `<header></header>`
- Define o cabeçalho de uma página.

### `<nav></nav>`
- Define os links de navegação.

### `<section></section>`
- Define uma área ou sessão.


### Parágrafos


#### `<p> </p>`
- Paragrafo, um texto.
- Aceita como atribulo, por exemplo:
  - align – Alinhamento do parágrafo: left, right, center e justify.


## Links


### `<a> </a>`
- Cria um link para uma pagina interna, externa ou âncora para um texto especifico.
- Aceita como atributos, por exemplo:
  - href – O URL para direcionamento do link.
  - target – Identifica local em que o link deverá ser aberto: blank, self, top, parent.


## Listas


### `<ol> </ol>`
- Uma lista ordenada.

### `<ul> </ul>`
- Uma lista não ordenada.

### `<li> </li>`
- Um item da lista.

### `<dl> </dl>`
- Uma lista de definições ou glossário.

### `<dt> </dt>`
- Marca o texto especificado como um termo de definição de um glossário.

### `<dd> </dd>`
- Especifica o texto referente a um termo criado pela tag <dt> dentro de uma lista de definição.


## Formatação de Texto


### `<em> </em>`
- Ênfase em texto itálico.

### `<strong> </strong>`
- Ênfase em texto em negrito.

### `<b> </b>`
- Texto em negrito.

### `<i> </i>`
- Texto em itálico.

### `<u> </u>`
- Texto sublinhado.

### `<big> </big>`
- Texto em fonte maior do que o padrão.

### `<small> </small>`
- Texto em fonte menor do que o padrão.

### `<hr>`
- Uma régua horizontal.


## Outras Tags


### `<br>`
- Uma quebra de linha.

### `<center> </center>`
- Centralizar.

### `<div> </div>`
- Qualquer conteúdo.
- Aceita como atribulo, por exemplo:
  - align – Alinhamento: left, center e right.

### `<font> </font>`
- Alterna tamanho , cor e tipo de fonte exibida.
- Aceita como atributos, por exemplo:
  - size – O tamanho da fonte varia de 1 a 7.
  - color – A cor da fonte.
  - face – O tipo da fonte.


## Imagens


### `<img>`
- Insere uma imagem in-line no documento.
- Aceita como atribultos, por exemplo:
  - src – O URL da imagem.
  - alt – Um texto referente ao conteudo da imagem.
  - height – É a altura da imagem em pixels.
  - width – É a largura da imagem em pixels.


## Tabelas


### `<table> </table>`
- Cria uma tabela.
- Aceita como atribultos, por exemplo:
  - background – Imagem de plano de fundo.
  - bgcolor – Cor de plano de fundo.
  - border – Largura da borda.
  - cellpadding – Espaçamento nas células.
  - cellspacing – Espaçamento entre as células.
  - width – Largura da tabela.
  - align – Alinhamento da tabela: left, center, right.

### `<tr> </tr>`
- Uma linha na tabela.

### `<th> </th>`
- Um cabeçalho de célula da tabela.

### `<td> </td>`
- Define uma coluna da tabela.


## Formulários

### `<form> </form>`
- Define um formulário.
- Aceita como atribultos, por exemplo:
  - action – local para onde as informações coletadas no formulário serão enviadas.
  - method – método de empacotamento dos dados do formulário: get, post e enctype="multipart/form-data".
  - name – nome do objeto.

### `<input>`
- Caixa de texto ou botão.
- Aceita como atribultos, por exemplo:
  - type – tipo de dado: text, file, radio, checkbox, hidden, password, submit, reset, button, image.
  - name – nome do objeto.
  - value – valor do objeto.

### `<textarea> </textarea>`
- Caixa de texto.
- Aceita como atribultos, por exemplo:
  - rows – Tamanho da linha da caixa de texto.
  - cols – Tamanho da coluna da caixa de texto.
  - name – nome do objeto.

### `<select> </select>`
- Caixa de seleção.
- Aceita como atribulto, por exemplo:
  - name – Identificador.

### `<option> </option>`
- Opção da caixa de seleção.
- Aceita como atribulto, por exemplo:
  - value – valor do objeto.


# CSS

CSS é uma linguagem de folha de estilos, que tem o papel de tornar uma página apresentável na web, relacionada diretamente com o design e aparência.

O CSS funciona com a personalização de estilos de três elementos:

- `TAG` (personalização das tags do html como `body`, `div`, `p`, `table` e etc..).
- `#id` (adiciona um ID por tag html fazendo uma personalização).
- `.classes` (é possível adicionar mais de uma classe por tag html).

Que tal conhecermos as principais `Atributos` do `CSS`:

## Background-color:    
Especifica a cor, com seu nome ou seu valor.

**Exemplo:** `background-color: #000055;` 


## background-image:
Espeficida o url da imagem de plano de fundo.

**Exemplo:** `background-image: url(http://www.site.com/logo.png)`


## border: 
Define a largura, estilo e cor de todas as quatro bordas (ordem: top, right, bottom, left).

**Exemplo:** `border: 1px solid #eee;`


## color:
Especifica a cor do texto.

**Exemplo:** `color: #333;`


## cursor: 
Define o tipo do ponteiro/cursor do mouse.

**Exemplo:** `cursor: pointer;`


## height: 
Especifica a altura de um elemento.

**Exemplo:** `height: 30px;`


## width: 
Especifica a largura de um elemento.

**Exemplo:** `width: 30px;`


## font-family: 
Estabelece os tipos de fonte que serão utilizados no elemento.

**Exemplo:** `font-family: 'Montserrat', sans-serif;`


## font-size: 
Determina o tamanho da fonte.

**Exemplo:** `font-size: 14px;`


## font-weight: 
Especifica quão grossa é a fonte, caso o estilo bold seja ativado.

**Exemplo:** `font-weight: bold;`


## display: 
Determina se um elemento estará visível e reserva um espaço para o mesmo ou não.

**Exemplo:** `display: none;`


## top: 
Determina a posição superior do elemento.

**Exemplo:** `top: 10%;`


## right: 
Especifica a posição direita de um elemento.

**Exemplo:** `right: 10%;`


## left: 
Especifica a posição esquerda de um elemento.

**Exemplo:** `left: 10%;`


## bottom: 
Especifica a posição abaixo de um elemento.

**Exemplo:** `bottom: 10%;`


## margin: 
Especifica o tamanho da margem de um elemento em todos os lados (ordem: top, right, bottom, left).

**Exemplo:** `margin: 10px 20px; 10px 20px;`


## padding:
Estabelece um espaço interno em torno de um elemento em todos os lados (ordem: top, right, bottom, left).

**Exemplo:** `padding: 10px 20px; 10px 20px;`


## position: 
Determina como o elemento está posicionado na página.

**Exemplo:** `position: absolute;`


## float: 
Determina com o elemento flutuará na página.

**Exemplo:** `float: left;`


## text-align:
Especifica o alinhamento do texto.

**Exemplo:** `text-align: center;`


## text-decoration: 
Especifica um tipo de decoração para o texto.

**Exemplo:** `text-decoration: none;`


## visibility: 
Especifica se o elemento estará visível.

**Exemplo:** `visibility: hidden;`


## z-index: 
número Estabelece a posição do elemento em uma pilha, se está por cima ou por baixo de outros elementos.

**Exemplo:** `z-index: 1`

