# Projeto Super Mario Bros - O Filme

![](https://github.com/edvaldoljr/Projeto-FrontEnd-SuperMarioBros-o-Filme/blob/main/src/imagens/img-projeto.gif?raw=true)

A aplicação é uma ferramenta interativa e intuitiva que oferece aos usuários a possibilidade de visualizar trailers de filmes e séries de maneira rápida e fácil. Com uma interface atraente e fácil de usar, a aplicação permite que os usuários explorem as últimas novidades e tendências em entretenimento, tudo a partir de um único lugar. Além disso, a aplicação inclui uma função de modal que permite aos usuários assistir a trailers em tela cheia, com uma excelente qualidade de imagem e som. Se você é apaixonado por entretenimento e gosta de ficar por dentro das últimas novidades, não perca a chance de experimentar esta incrível aplicação.

## Requisitos:

Você precisará de um editor de código, como o Visual Studio Code, para escrever o código e visualizá-lo em um navegador. Além disso, você precisará ter conhecimento básico de HTML para estruturar o conteúdo da página, CSS para estilizá-lo e JavaScript para adicionar interatividade à página.

# Desenvolvimento:

## index.html

Este código HTML é uma página web para promover o filme "Super Mario Bros". A página consiste em uma estrutura básica de HTML, com tags head e body.

No head, há metadados sobre a página, como o tipo de codificação de caracteres e a compatibilidade com navegadores. Além disso, são incluídas referências a arquivos CSS e a uma fonte externa do Google Fonts.

No body, há um fundo com um vídeo em loop e um header com um logo e um menu. O conteúdo principal da página consiste em informações sobre o filme, incluindo uma descrição curta, uma imagem dos personagens e um botão para ver o trailer. Quando o botão é clicado, uma janela modal aparece com o trailer do filme em um iframe do YouTube.

O JavaScript é usado para adicionar interação à página, como abrir e fechar a janela modal ao clicar no botão.

Em geral, este código HTML cria uma página web simples e atraente para promover o filme "Super Mario Bros".

```html
<!DOCTYPE html>
<html lang="pt-BR">
	<head>
		<meta charset="UTF-8" />
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />

        <link rel="shortcut icon" href="./src/imagens/favicon.ico" type="image/x-icon">

		<link rel="preconnect" href="https://fonts.googleapis.com" />
		<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
		<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@100;300;500&display=swap" rel="stylesheet" />

		<link rel="stylesheet" href="./src/css/reset.css">

		<link rel="stylesheet" href="./src/css/estilos.css">


		<link rel="stylesheet" href="./src/css/responsivo.css">

		<title>Super Mario Bros - O Filme</title>
	</head>
	<body>
		<div class="fundo-video">
			<video class="video" autoplay loop muted>
				<source src="./src/video/video-mario.mp4" type="video/mp4" />
			</video>
		</div>

		<header class="cabecalho">
			<a>
				<img class="logo" src="./src/imagens/logo-chapeu-mario.png" alt="logo chapéu Mario" />
			</a>
			<nav>
				<ul class="menu">
					<li><a href="#">Home</a></li>
					<li><a href="https://www.thesupermariobros.movie/" target="_blank">Site Oficial</a></li>
				</ul>
			</nav>
		</header>
		<main class="container">
			<div class="informacoes">
				<img class="imagem-titulo" src="./src/imagens/super-mario-bros-personagens-removebg-preview.png" />
				<p class="descricao">Mario é um encanador junto com seu irmão Luigi. Um dia, eles vão parar no reino dos cogumelos, governado pela Princesa Peach, mas ameaçado pelo rei dos Koopas, que faz de tudo para conseguir reinar em todos os lugares.</p>
				<button class="botao-trailer">Veja o trailer</button>
			</div>
			<img class="mario" src="./src/imagens/The_Super_Mario_Bros_Movie_logo-removebg-preview.png"" />

			<div class="modal">
				<div class="conteudo-modal">
					<span class="fechar-modal">X</span>
					<iframe id="video" width="560" height="315" src="https://www.youtube.com/embed/Cb4WV4aXBpk" title="Trailer oficial" frameborder="1" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
				</div>
			</div>
		</main>

		<script src="./src/js/index.js"></script>
	</body>
</html>

```

## reset.css

Este código CSS define três estilos para elementos HTML. O primeiro estilo é para todos os elementos (*) e faz com que as margens e paddings sejam zeradas e que o tamanho da caixa inclua o tamanho da borda.

O segundo estilo é para listas não ordenadas (ul) e remove o estilo de lista padrão, tornando a lista sem marcadores.

O terceiro estilo é para links (a) e remove a decoração de texto padrão, deixando os links sem sublinhado.

```css
* {
 margin: 0;
 padding: 0;
 box-sizing: border-box;
}

ul {
  list-style: none;
}

a {
   text-decoration: none; 
}
```

## estilos.css

O código apresenta uma estrutura de estilo para uma página web, usando CSS. A primeira seção define o estilo geral da página, incluindo a fonte usada em todo o corpo da página.

A tag body define o corpo principal do documento HTML. É dentro desse corpo que todo o conteúdo da página será exibido.

A classe "cabecalho" define um cabeçalho para a página, que terá um display flex (disposição dos itens na tela), alinhamento dos itens justificados entre espaços, um padding de 30 pixels, largura máxima de 1440 pixels e será centralizado na tela.

A classe "logo" define a largura do logo em 40 pixels.

A classe "menu" define o menu de navegação da página, tendo um display flex (disposição dos itens na tela), alinhamento dos itens centrado e uma altura de 100%.

A classe "cabecalho nav li a" define a aparência dos links do menu de navegação. Eles terão fonte em negrito, cor branca, tamanho de fonte 20 pixels, padding de 10 pixels a esquerda e direita e 20 pixels acima e abaixo, borda arredondada com 50 pixels de raio e terão uma transição de 0.2 segundos ao passar o mouse sobre eles.

A classe "container" define o contêiner principal da página, tendo uma largura máxima de 1440 pixels, centralização na tela, display flex (disposição dos itens na tela), alinhamento dos itens centrado e uma altura que será calculada com base na altura da tela menos 132 pixels.

A classe "imagem-titulo" define a largura máxima da imagem de título em 500 pixels.

A classe "descricao" define a aparência da descrição da página, tendo cor cinza claro, largura de 85%, tamanho de fonte 18 pixels e margem de 30 pixels acima e abaixo.

A classe "botao-trailer" define a aparência do botão de trailer, tendo cor vermelha, cor branca para o texto, padding de 15 pixels, tamanho de fonte 14 pixels, fonte em negrito, cursor em forma de mão, borda arredondada com 50 pixels de raio, texto em maiúsculo e uma transição de 0.5 segundos ao passar o mouse sobre ele.

A classe "fundo-video" define o fundo do vídeo, tendo posição absoluta, camada com índice -1, largura e altura de 100% da tela, com conteúdo escondido fora dos limites, display flex (disposição dos itens na tela) e alinhamento dos itens centrado.

A classe "video" define a altura do vídeo em 100% da tela.

A classe "modal" define um modal (janela pop-up) que ficará

```css
body {
    font-family: 'Poppins';
}

.cabecalho {
    display: flex;
    justify-content: space-between;
    padding: 30px;
    max-width: 1440px;
    margin: 0 auto;
}

.cabecalho .logo {
    width: 40px;
}

.cabecalho .menu{
    display: flex;
    align-items: center;
    height: 100%;
}

.cabecalho nav li a {
    font-weight: bold;
    color: #ffffff;
    font-size: 20px;
    padding: 10px 20px;
    border-radius: 50px;
    transition: 0.2s;
}

.cabecalho nav li a:hover {
    background-color: #d5011d;
}

.container {
    max-width: 1440px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    height: calc(100vh - 132px);
    padding: 0 30px 30px;
}

.container .imagem-titulo {
    max-width: 500px;
}

.container .descricao {
    color: #a8adb7;
    width: 85%;
    font-size: 18px;
    margin: 30px 0;
}

.container .botao-trailer {
    background-color: #ff0021;
    color: #ffffff;
    padding: 15px;
    font-size: 14px;
    font-weight: bold;
    cursor: pointer;
    border-radius: 50px;
    text-transform: uppercase;
    transition: 0.5s all ease-in-out;
}

.container .botao-trailer:hover {
    transform: scale(1.1)
}

.fundo-video {
    position: absolute;
    z-index: -1;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    display: flex;
    justify-content: center;
}

.fundo-video .video {
    height: 100vh;
}

.fundo-video::after {
    content: "";
    height: 100vh;
    width: 100vw;
    position: absolute;
    top: 0;
    left: 0;
    background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0.8) 50%, rgba(0,0,0,1) 100%);
}

.modal {
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
    background-color: rgba(52, 52, 50, 0.749);
    opacity: 0;
    visibility: hidden;
}

.conteudo-modal {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 100vh;
    border-radius: 5px;
    gap: 15px;
}

.fechar-modal {
    background-color: #ffffff;
    color: #f03a17;
    font-weight: bold;
    font-size: 20px;
    width: 40px;
    text-align: center;
    cursor: pointer;
    border-radius: 10px;
}

.modal iframe {
    border-width: 0;
    width: 640px;
    height: 360px;
}

.modal.aberto {
    opacity: 1;
    visibility: visible;
}




```

## responsividade.css

Esta seção de código CSS está usando regras de mídia, o que significa que elas serão aplicadas de acordo com as condições de tela especificadas.

A primeira regra @media (max-width: 1200px) é aplicada quando a largura máxima da tela é de 1200 pixels. Neste caso, ele define estilos para o corpo, como fundo, tamanho, cor, fonte, etc. Ele também esconde um elemento com classe "fundo-video". Além disso, ele define estilos para o contêiner, incluindo a exibição, alinhamento, direção, descrição e botão.

A segunda regra @media (max-width: 500px) é aplicada quando a largura máxima da tela é de 500 pixels. Neste caso, ele define estilos para o elemento com classe "cabecalho" e "imagem-titulo". Além disso, ele define estilos para o elemento dentro do modal, incluindo tamanho, largura e altura.

A terceira regra @media (max-width: 376px) é aplicada quando a largura máxima da tela é de 376 pixels. Neste caso, ele define o tamanho e a altura do elemento dentro do modal com classe "#video".

Em resumo, essas regras de mídia permitem que você defina estilos diferentes para diferentes tamanhos de tela, fornecendo uma melhor experiência para o usuário.

```css
@media (max-width: 1200px) {
    body {
        background: -webkit-gradient(
            linear,
            left top,
            left bottom,
            from(rgba(0, 0, 0, 0.7)),
            to(rgba(0, 0, 0, 0.7))
          ),
          url(../imagens/fundo.jpg) no-repeat;
        background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
          url(../imagens/fundo.jpg) no-repeat;
        background-size: cover;
        background-position: center;
        background-attachment: fixed;
        height: 100vh;
        color:#fff;
        min-height: 500px;
        font-family: "Ubuntu", sans-serif;
    }

    .fundo-video {
        display: none;
    }

    .container {
        flex-wrap: wrap;
        justify-content: center;
        height: auto;
        gap: 30px;
    }

    .container .mario {
        max-width: 50%;
    }

    .container .informacoes {
        display: flex;
        align-items: center;
        flex-direction: column;
    }

    .container .descricao {
        color: #ffffff;
        text-align: center;
    }

    .container .botao-trailer {
        background-color: hsl(359, 91%, 48%);
    }
}

@media (max-width: 500px) {
    .cabecalho {
        flex-wrap: wrap;
        justify-content: center;
        gap: 10px;
    }

    .container .imagem-titulo {
        max-width: 75%;
    }

    .modal .fechar-modal {
        width: 30px;
        line-height: 30px;
    }

    .modal #video {
        width: 300px;
        height: 169px;
    }
}

@media (max-width: 376px) {
    .modal #video {
        width: 250px;
        height: 140px;
    }
}
```

## index.js

Este é um código JavaScript que permite alternar a exibição de um modal que contém um vídeo. Quando o botão "botaoTrailer" é clicado, o modal é aberto e o atributo "src" do elemento de vídeo é definido como "linkDoVideo". Quando o botão "botaoFecharModal" é clicado, o modal é fechado e o atributo "src" do elemento de vídeo é definido como uma string vazia.

```javascript
const botaoTrailer = document.querySelector(".botao-trailer");
const botaoFecharModal = document.querySelector(".fechar-modal");
const video = document.getElementById("video");
const modal = document.querySelector(".modal");
const linkDoVideo = video.src;

function alternarModal(){
	modal.classList.toggle("aberto");
}

botaoTrailer.addEventListener("click", () => {
	alternarModal();
	video.setAttribute("src", linkDoVideo);
});

botaoFecharModal.addEventListener("click", () => {
	alternarModal();
	video.setAttribute("src", "");
});
```

## Hospedagem

Estamos hospedando nosso projeto no GitPages, uma plataforma de hospedagem gratuita para projetos baseados em Git. Com GitPages, podemos compartilhar nosso trabalho com o mundo e de forma fácil e rápida. Além disso, a integração com o GitHub torna ainda mais simples o processo de desenvolvimento, teste e implantação de nossas aplicações.

## Acesso o Link e assista o Trailler:

https://edvaldoljr.github.io/Projeto-FrontEnd-SuperMarioBros-o-Filme/

# ⭐️ **Deixe um Star** ⭐️

Obrigado por conferir meu repository! É muito gratificante saber que alguém está interessado no meu trabalho. Se você gostou do que viu, deixar um star seria uma grande ajuda no meu crescimento e me motivaria a continuar fazendo projetos. O apoio de pessoas como você é fundamental para que eu possa seguir evoluindo e produzindo conteúdos cada vez melhores. Obrigado mais uma vez e espero que você possa acompanhar meus futuros projetos!
