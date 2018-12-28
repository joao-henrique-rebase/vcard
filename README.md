# Tutorial

## Projeto Cartão de Visitas

Dado um Template em `.PDF` vamos criar recria-lo com nossas próprias informações para um possível carão de visitas WEB.

[Template](https://github.com/JoaoHenriqueVale/vcard/blob/master/v-card.pdf)

Modelo Final do Nosso Cartão:
![](https://raw.githubusercontent.com/JoaoHenriqueVale/vcard/master/preview/v-card.png) 

Vamos Criar a estrutura de pastas do nosso projeto `vcard`:

Dentro da nossa pasta raiz `vcard`, criaremos duas pasta para imagens e estilos sendo elas,
`css` e `images`

- images (colocaremos todas imagens para nosso projeto)
- `avatar.png` (imagem de perfil)
- `background.jpg` (Imagem de fundo)
- css (colocaremos nossas folhas de estilo, nossos `css`)

Ainda dentro da raiz `vcard` criaremos nosso arquivo `index.html`

Vamos lá,

Começaremos pela estrutura básica de um HTML:

```
<!DOCTYPE html>
<html lang="pt-br">
  <head>
  <meta charset="utf-8">
    <title>João Henrique - Cartão de Visitas</title>
  </head>
  <body>
    ...
  </body>
</html>
```

Dentro do nosso `<body></body>`, vamos criar uma sessão `<section></section>` para o conteúdo.

```
...
<body>
  <section>
    ...
  </section>
</body>
...
```

Olhando para o Template do `Vcard` vamos começar de cima para baixo, e criar uma divisão `<div></div>` para o "corpo" do `Vcard` em si, dentro da sessão, vamos dar um classe para ela já, chama-la de `vcard-body`:

```
...
<body>
  <section>
    <div class="vcard-body">
      ...
    </div>
  </section>
</body>
...
```

Vamos iniciar dentro do "corpo" do `Vcard`, começando pela imagem de perfil, podemos criar uma divisão `<div></div>` para imagem e importar a imagem `<img>` em si, vamos dar o nome da divisão de `vcard-profile-img` e da imagem `profile-img`:

Para importar a imagem, vamos colocar o caminho da foto de perfil localizada na pasta de images:

```
...
<div class="vcard-profile-img">
  <img src="images/avatar.png" class="profile-img" alt="avatar">
</div>
...
```

Partindo para os textos do `VCard` podemos criar uma divisão `<div></div>` para ela, e começar a implementar os titulos `<h1></h1>` e subtiulos `<h2></h2>` no caso "texo de apresentação" e "profisão", lembrando que no "texo de apresentação" vamos tratar "nome" de forma diferenciada podemos criar uma marcação `<span></span>` para isso, lembrando de sempre colcoar nomes descritivos para as "classes" das `TAGS` que vamos customizar.

Vamor inserir tambem uma regua de marcação `<hr>`, após os titulos, para o texto descritivo do card:

```
...
  <div class="vcard-profile-description">
    <h1 class="profile-title">Oi, Eu sou o <span class="profile-title-color">João Henrique!</span></h1>
    <h2 class="profile-subtitle">Desenvolvedor Web</h2>
    <hr />
    ...
  </div>
...
```

Ainda dentro da divisão de descrição `<div class="vcard-profile-description">`, vamos inserir uma divisão `<div></div>` para os textos `<p></p>` de informação do nosso card, contanto um pouco da nossa experiencia.
Vamos chamar a classe divisão de `vcard-profile-description-text`
```
<div class="vcard-profile-description">
  ...
  <div class="vcard-profile-description-text">
    <p>
      Desenvolver Web a 5 anos, experiência em Ruby on Rails, PHP e VUE.JS,
      Residindo em São Paulo e Músico nas horas vagas.
    </p>
  </div>
  ...
</div>
```

Agora vamos destacar uma divisão `<div></div>` de texto `<p></p>` para os nosso meios de contato ainda dentro da `<div class="vcard-profile-description">` , vamos chamar a classe de `vcard-profile-description-contact`

```
...
<div class="vcard-profile-description-contact">
  <p>email: joao.vale@campuscode.com.br / tel: +12 3456 6789</p>
</div>
...
```

E por fim vamos criar uma nova divisão `<div></div>` para o rodapé contendo os links `<a></a>` das nossas redes sociais, isso fora da "divisão de descrição", podemos chamar a classe de `vcard-footer`

O Conteudo de cada Link será um icone de uma rede social, para isso podemos recorrer ao [Font Awesome](https://fontawesome.com/) a um site bem legal cheio de ícones vetoriais e logotipos:

Para integra-lo ao nosso projeto bastas importar no Cabeçalho `<head></head>` do nosso HTML
a seguinte linha:

```
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.3/css/all.css">
```
Para saber mais:
https://fontawesome.com/start

ficando assim:

```
<head>
  ...
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.3/css/all.css">
</head>
<body>
  ...
  ...

  <div class="vcard-footer">
    <a href="#" class="footer-icon"><i class="fab fa-instagram"></i></a>
    <a href="#" class="footer-icon"><i class="fab fa-facebook-f"></i></a>
    <a href="#" class="footer-icon"><i class="fab fa-twitter"></i></a>
    <a href="#" class="footer-icon"><i class="fab fa-linkedin-in"></i></a>
    <a href="#" class="footer-icon"><i class="fab fa-youtube"></i></a>
  </div>
  ...
<body>
```

Pronto, nosso esqueleto do `VCard` está feito, fácil certo?, o conteúdo a até o momento ficou algo assim:

```
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.3/css/all.css">
    <title>João Henrique - Cartão de Visitas</title>
  </head>
  <body>
    <section>
      <div class="vcard-body">
        <div class="vcard-profile-img">
          <img src="images/avatar.png" class="profile-img" alt="avatar">
        </div>
        <div class="vcard-profile-description">
          <h1 class="profile-title">Oi, Eu sou o <span class="profile-title-color">João Henrique!</span></h1>
          <h2 class="profile-subtitle">Desenvolvedor Web</h2>
          <hr />
          <div class="vcard-profile-description-text">
            <p>
              Desenvolver Web a 5 anos, experiência em Ruby on Rails, PHP e VUE.JS,
              Residindo em São Paulo e Músico nas horas vagas.
            </p>
          </div>
          <div class="vcard-profile-description-contact">
            <p>email: joao.vale@campuscode.com.br / tel: +12 3456 6789</p>
          </div>
        </div>
        <div class="vcard-footer">
          <a href="#" class="footer-icon"><i class="fab fa-instagram"></i></a>
          <a href="#" class="footer-icon"><i class="fab fa-facebook-f"></i></a>
          <a href="#" class="footer-icon"><i class="fab fa-twitter"></i></a>
          <a href="#" class="footer-icon"><i class="fab fa-linkedin-in"></i></a>
          <a href="#" class="footer-icon"><i class="fab fa-youtube"></i></a>
        </div>
      </div>
    </section>
  </body>
</html>
```

Caso abrirmos no "navegador" o arquivo `index.html`, teremos algo assim:
![](https://raw.githubusercontent.com/JoaoHenriqueVale/vcard/master/preview/esqueleto-html.png) 

Bom agora que tal colocarmos um estilo no nosso esqueleto maquiar ele e deixar mais apresentável para os nossos futuros clientes que acessarem nosso cartão de visita.

Primeiramente vamos criar nosso arquivo de CSS, então dentro da pasta `css` criaremos um arquivo chamado `style.css` e após isso precisamos importa-lo no nosso HTML, para isso inserimos no nosso cabeçalho `<head></head>` a seguinte linha:

```html
<link href="css/style.css" rel="stylesheet">
```

Olhando o Template final, notamos de cara que ele tem uma imagem de fundo e uma fonte diferente, no caso a fonte será `Montserrat`, para isso podemos importá-la também no nosso cabeçalho `<head></head>`:

```html
<link href="https://fonts.googleapis.com/css?family=Montserrat" rel="stylesheet">
```

Agora sim podemos começar a implementar nosso estilo no arquivo de `CSS`, começando pelo `body`, vamos destacar as customizações que queremos:

- Personalização fonte.
- Imagem de fundo.
- Cor do texto cinza escuro.

Então vamos criar os atributos de customização do body, seria algo assim:

```css
body {
  font-family: 'Montserrat', sans-serif; /* Atribuir fonte Montserrat e sans-serif como fonte alternativa*/
  background: url('../images/background.jpg') no-repeat center center fixed; /* Inserir imagem de fundo passando o caminho localizado na pasta de images, centraliza-la e fixa-la ao centro */
  background-size: cover; /* Imagem preencher todo o espaço do body */
  font-size: 14px; /* Tamanho de fonte 14 pixels */
  color: #333; /* Cor de fonte #333 */
}
```
>INFO: para saber Hexadecimais de cores de fontes recomendo o site: [Color Blindness](http://www.color-blindness.com/color-name-hue/)

O corpo do Card na nossa divisão do `VCard`, `<div class="vcard-body">`:

- Borda verde no topo.
- Fundo claro.
- Centralizado.
- Tamanho definido.
- Espaçamento interno.

```css
.vcard-body {
  max-width: 468px; /* Tamanho máximo do card para 468 pixels */
  width: 100%; /* Tamanho do Card ocupar 100% do espaço da tela respeitando o máximo a cima */
  margin: 80px auto; /* Centralizar Card horizontalmente e colocando margens no top e bottom de 80px;*/
  background: #f4f4f4; /* Inserir cor de fundo para o Card*/
  padding: 45px; /* Inserir espaçamento interno no Card de 45px */
  border-top: 6px solid #08aeac; /* Inserir borda verde no topo do card de 6 pixels */
}
```

Na divisão da imagem de perfil `<div class="vcard-profile-img">`:

- Tamanho definido.
- Conteudo alinahdo ao centro.

```css
.vcard-profile-img {
  width: 200px; /* Tamanho definido a 200 pixels */
  margin: 0 auto; /* Centralizar conteúdo horizontalmente */
}
```

Na imagem de perfil `<img class="profile-img">`:

- Tamanho definido.
- Imagem arredondada.

```css
.profile-img {
  width: 100%; /* Tamanho da imagem ocupar 100% do espaço */
  border-radius: 100%; /* Arredondar borda da imagem 100% torando-a arredondada */
}
```

No texto de apresentação `<h1 class="profile-title">` e no nome `<span class="profile-title-color">`:

- Tamanho da fonte.
- Espessura da fonte.
- Alinhamento do texto.
- Cor do fonte verde no nome.

```css
.profile-title {
  margin-bottom: 0; /* Remover margem defult do elemento h1 */
  text-align: center; /* Alinhar o texto ao centro */
  font-weight: bold; /* Inserir fonte em negrito */
  font-size: 30px; /* Alterar tamanho da fonte para 30 pixels */
}
```

```css
.profile-title-color {
  color: #08aeac; /* Alterar cor de fonte para #08aeac */
}
```

No texto da profissão `<h2 class="profile-subtitle">`:

- Tamanho da fonte.
- Espessura do texto.
- Alinhamento do texto.

```css
.profile-subtitle {
  text-align: center; /* Alinhar o texto ao centro */
  font-size: 20px; /* Alterar tamanho da fonte para 20 pixels */
  font-weight: bold; /* Inserir fonte em negrito */
}
```

No texto de informação ` <div class="vcard-profile-description-text">`:

- Alinhamento do texto.

```css
.vcard-profile-description-text {
  text-align: center; /* Alinhar o texto ao centro */
}
```

No texto de meios de contato ` <div class="vcard-profile-description-contact">`:

- Alinhamento do texto.
- Espaçamento entre o fundo e o texto.
- Fundo arredondado.
- Cor de fundo verde.
- Cor do fonte branco.

```css
.vcard-profile-description-contact {
  text-align: center; /* Alinhar o texto ao centro */
  border-radius: 5px; /* Inserir borda arredondada de 5 pixels */
  padding: 5px 10px; /* Inserir espaçamento interno de 5 pixels verticalmente e 10 pixels horizontalmente */
  background: #08aeac; /* Alterar cor do fundo para #08aeac */
  color:#fff; /* Alterar cor de fonte para #fff */
} 
```

Na divisão dos links de redes sociais `<div class="vcard-footer">`:

- Espaçamento ao elemento acima.
- Alimentendo do texto.

```css
.vcard-footer {
  margin-top: 20px; /* Inserir margem no topo de 20 pixels */
  text-align: center; /* Alinhar o texto ao centro */
}
```

Nos links de redes sociais `<a class="footer-icon">`:

- Cor dos ícones
- tamanho da fonte
- Espaçamento entre os ícones

```css
.footer-icon {
  color:#333; /* Alterar cor de fonte para #333 */
  font-size: ; /* Alterar tamanho da fonte para 16 pixels */
  margin-right: 10px; /* Inserir margem na direita de 10 pixels entre os ícones */
}
```

Pronto o conteúdo do arquivo `style.css` deve ter ficado assim:

```css
body {
  font-family: 'Montserrat', sans-serif;
  background: url('../images/background.jpg') no-repeat center center fixed;
  background-size: cover;
  font-size: 14px;
  color: #333;
}

.vcard-body {
  max-width: 468px;
  width: 100%;
  margin: 80px auto;
  background: #f4f4f4;
  padding: 45px;
  border-top: 6px solid #08aeac;
}

.vcard-profile-img {
  width: 200px;
  margin: 0 auto;
}

.profile-img {
  width: 100%;
  border-radius: 100%;
}

.profile-title {
  margin-bottom: 0;
  text-align: center;
  font-weight: bold;
  font-size: 30px;
}

.profile-title-color {
  color: #08aeac;
}

.profile-subtitle {
  text-align: center;
  font-size: 20px;
  font-weight: bold;
}

.vcard-profile-description-text {
  text-align: center;
}

.vcard-profile-description-contact {
  text-align: center;
  border-radius: 5px;
  padding: 5px 10px;
  background: #08aeac;
  color:#fff;
}

.vcard-footer {
  margin-top: 20px;
  text-align: center;
}

.footer-icon {
  color:#333;
  font-size: 16px;
  margin-right: 10px;
}
```

Terminamos nosso Cartão de Visitas WEB!!!