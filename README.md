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
