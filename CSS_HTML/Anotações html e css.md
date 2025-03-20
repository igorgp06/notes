## 1: Básico do HTML
usamos 
~~~html
<!DOCTYPE html>
~~~
para dizer que o arquivo é do tipo HTML, ele deve estar no topo do código

como o HTML eh uma linguagem de marcação WEB, devemos dizer qual o idioma nosso site
será, para isso usamos 
~~~html
<html lang="pt-br">
~~~
Dentro dos parênteses deve estar a linguagem do site

para darmos o cabeçalho do site, usamos 
~~~html
<head> </head>
~~~
o último head deve estar localizado onde termina nosso cabeçalho

usamos o 
~~~html
<meta charset="UTF-8">
~~~
para que os assentos e carácteres especias em português funcionem, como o Ç ou os assentos 

definimos os tamanhos e proporções inicias com 
~~~html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
~~~
isto dá ao site a informação de qual tamanha ele deve estar

e usamos 
~~~html
<title>Módulo 1</title>
~~~
para dar o título do site que aparece lá em cima na barrinha

o 
~~~html
<body> </body>
~~~
serve para inserirmos o corpo do nosso site, segue a mesma lógica do head

o termo
~~~html
<h1> </h1>
~~~
informa o título de algo, podemos usar o exemplo do markdown que usa as # para falar
se eh um título, sub-título e etc

já o 
~~~html
<p> </p>
~~~
serve para informar um parágrafo

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Módulo 1</title>
    </head>

    <body>

        <h1>Olá, mundo!</h1>
        <p>Este é um parágrafo.</p>

    </body>
</html>
~~~

Explicação do código:
cria um simples site que escreve as informações que inserimos nas funções que vimos antes


-----------------------------------------------------------------


## 2: Parágrafos e quebras de linhas

apertar somente enter não dá certo para podermos quebrar linhas dentro do HTML, para fazermos
isto devemos adicionar a tag 
~~~html
<br>
~~~
ela eh responsável por quebrar as linhas

como dentro dos parágrafos nós não podemos usar as tags "<>", pois, elas irão cortar nossa marcação,
ou seja, se eu tenho um parágrafo assim:
~~~html
<p>Eu sou um parágrafo</p>
~~~
nós não podemos adicionar as tags ali dentro, já que quebraria nosso site, então a solução para isso eh
usarmos "&lt;" para < e "&gt;" para >

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Olá, mundo!</title>
</head>
<body>
    <h1>Paragrafos e quebras de linhas</h1>
    <hr>
    <p>Para quebrarmos linhas
        não basta apenas apertar
        enter e achar que funciona,
        para quebramos uma linha devemos
        usar o <br> (breakline) e assim
        nós <br> quebramos as linhas
    </p>
    <p>Para usarmos a tag da boquinha
        do jacaré, usamos &lt;(exemplo de alguma
        aqui)&gt;
    </p>
</body>
</html>
~~~

Explicação do código:
um simples código em HTML que nos dá um exemplo do que vimos anteriormente, ele tem
dois parágrafos, o primeiro mostrando o uso do <br> e o exemplo do &lt; e &gt;


----------------------------------------------------------------- 


## 3: Símbolos e emojis

Para usarmos emojis funciona da msm lógica que o "&lt;" e "&gt;"
após adicionarmos o & escrevemos o nome do símbolo que queremos usar,
assim:
"&copy;"
aqui nós adicionamos o símbolo do copyright

os emojis seguem a mesma lógica, entre no site "emojipidia", procure o emoji
que você deseja, procure o codepoint do emoji e no HTML adicione o seguinte código
antes de adicionar o emoji "*#x", após isso vc pode adicionar o código do emoji

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Olá, mundo!</title>
</head>
<body>
    <h1>Símbolos e emojis</h1>
    <hr>
    <p>Símbolos: <br> 
        &reg;
        &copy;
        &trade;
        &euro;
        &pound;
        &yen;
        &cent;
        &delta;
        &Delta;
        &uarr;
    </p>

    <p>Emojis: <br>
        &#x1F596;
        &#x1F913;
        &#x1F9D1;
        &#x1F9D9;
        &#x1F9DB;
        &#x1F9DD;
    </p>
</body>
</html>
~~~

Explicação do código:
aqui fizemos o mesmo dos dois últimos emojis, porém usando emojis e símbolos


-----------------------------------------------------------------


## 4: Uso de imagens

Para usarmos imagens no HTML temos que usar o comando 
~~~html
<img src="" alt="">
~~~

o "<src="">" significa onde está localizada a imagem que queremos abrir, o lugar indicado
pode ser uma sub-pasta, link direto da imagem e etc

já o "<alt="">" significa qual o significado da imagem, exemplo, se usamos a logo do HTML5 em nosso site, devemos no alt informar que a imagem eh a logo do HTML5, isso serve para para que pessoas com alguma dificuldade tenha o mínimo de acessibilidade

Use o Gimp para redimensionar as imagens, não deixe NENHUMA imagem pesada em seu site!!

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imagens no HTML</title>
</head>
<body>
    <link rel="stylesheet" href="style.css">
    <h1>Usando imagens no HTML5</h1>
    <hr>
    <h3>Veja abaixo como usar imagens no HTML5</h3>
    <hr>
    <p>Logo do HTML5</p>
    <img src="images/HTML5_redimensionado.png" alt="Logo HTML5">
    <p>Logo do CSS3</p>
    <img src="images/CSS3_redimensionado.png" alt="Logo CSS3">
    <p>Logo do JavaScript</p>
    <img src="https://freesvg.org/img/js_logo.png_" alt="Logo JavaScript">
</body>
</html>
~~~

Explicação do código:
usamos o código padrão que o VSCode gera automaticamente quando usamos o !
dentro do corpo do nosso site usamos duas imagens, a logo do HTML5 e a logo
do CSS3, as duas estão localizadas dentro de uma pasta chamada "images" e a logo 
do JavaScript está em um link direto


-----------------------------------------------------------------


## 5: Favicons

Para usarmos os Favicon eh extremamente simples. Eles são as imagens que fica no cabeçalho,
aquela imagem bem do lado d nome do site

precisaremos primeiramente de uma imagem que gostaríamos de ter como um favicon, após termos a
imagem que queremos, vamos ao site:
https://favicon.io/favicon-converter/
e vamos transformar nossa imagem num favicon, lembre-se que após converter a imagem
devemos usar a que tem a extensão de ".ico"

usamos o código 
~~~html
<link rel="" href="" type=""> dentro do <head> 
~~~
para termos nosso favicon

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imagens no HTML</title>
    <link rel="shortcut icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>
    <h1>Olha o favicon aqui em cima!!</h1>
</body>
</html>
~~~

Explicação do código:
aqui temos um código que tem na logo do nosso porrifólio sendo exibida, simples assim


-----------------------------------------------------------------


## 6: Hierarquia de Títulos

Dentro do HTML5 existe uma hierarquia de títulos, sendo elas do menor até o maior, começando
de 
~~~html
<h1> </h1> até <h6> </h6>
~~~

cada um faz referencia ao outro, ou seja, podemos dizer que o h1 eh o título principal
e o h2 o sub-título, o h2 vai fazer referência com o h1 enquanto o h3 faz fazer referência ao
h2 e assim sucessivamente

os estilos, tamanhos de texto, cores e etc podem ser alterados depois com o CSS, então não se
preocupe se o tamanho está muito grande ou muito pequena, esse não eh o foco por agora

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imagens no HTML</title>
    <link rel="shortcut icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>
    <h1>Entendendo Portugal</h1>
    <h2>Introdução</h2>
    <h3>Justificação da Temática</h3>
    <p>Texto aqui</p>
    <h3>Caráter EXECIONAL</h3>
    <p>Texto aqui</p>
    <h3>Perguntas de partida</h3>
    <p>Texto aqui</p>
    <h3>Metodologia de Investigação</h3>
    <h4>Etapas de Investigação</h4>
    <p>Texto aqui</p>
    <h4>Instrumentos de Análise</h4>
    <p>Texto aqui</p>
    <h2>Ordenamento do Território em Portugal</h2>
    <h3>Os instrumentos de gestão</h3>
    <h4>Os instrumentos de planejamento</h4>
    <p>Texto aqui</p>
    <h4>Os regimes territoriais</h4>
    <p>Texto aqui</p>
</body>
</html>
~~~

Explicação do código:
aqui fizemos um simples código que faz referência a um artigo, ele mostra
bem como funciona a hierarquia de cada um dos títulos e sub-tútulos


-----------------------------------------------------------------


## 7: Negrito e Itálico

Dentro do HTML5 podemos deixar frases em negrito ou em itálico sem precisar do CSS, para isso
temos as formas com e sem semântica, use somente a forma semântica e tenha preferência em fazer
estilos no CSS

para deixarmos algo em negrito usamos o comando 
~~~html
<strong> </strong>
~~~

já o itálico usamos 
~~~html
<em> </em>
~~~

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imagens no HTML</title>
    <link rel="shortcut icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>
    <h1>Principais formatações</h1>
    <h2>Negrito / Destaque</h2>
    <p>Aqui nessa frase usamos o <b>negrito</b> com a tag B (sem semântica)</p>
    <p>Usando a tag <strong>STRONG</strong> (com semântica) </p>
    <h2>Italico / Ênfase</h2>
    <p>Nesta frase temos um <i>termo itálico</i> usando a tag i (sem semântica)</p>
    <p>Nesta frase temos um <em>termo em ênfase</em> usando a teh EM (com semântica)</p>
</body>
</html>
~~~

Explicação do código:
aqui usamos o msm de sempre, apresentamos como usar o negrito e o itálico com e sem
semântica


-----------------------------------------------------------------


## 8: Listas

Para usarmos listas dentro do HTML existe um comando chamado 
~~~html
<ul> </ul>
~~~
junto dele existe também as listas ordenadas que seguem uma ordem e as listas não ordenadas onde não seguem nenhuma ordem

para listas não ordenadas usamos 
~~~html
<ol> </ol>
~~~
o comando "<type="">" serve para dizer qual o tipo de
lista ela eh, se usa números romanos, letras e etc. Os possiveis tipos são: 1 A a I i

já para as listas não ordenadas usamos o comando 
~~~html
<ul> </ul>
~~~
existe três tipos de type para as listas não ordenadas, sendo eles: disc circle square

não esqueça de sempre uma o comando 
~~~html
<li>
~~~
quando for colocar algo dentro de uma lista

existe também os aninhamentos de listas, coisa que vc já conheçe e tá mto acostumado a ver no python por exemplo

o comando 
~~~html
<dl> </dl>
~~~
eh pra listas de definição, ou seja, um assunto principal em cima e um abaixo explicando sua definição, algo nesse estilo

o 
~~~html
<dt> </dt>
~~~
eh o começo,  o conteúdo a ser definido, já o 
~~~html
<dd> </dd>
~~~
é a definição do conteúdo

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML</title>
    <link rel="shortcut icon" href="images/favicon.ico" type="image/x-icon">
</head>

<body>
    <h1>Trabalhando com Listas</h1>
    <h2>Listas ordenadas</h2>
    <ol type="1">
        <li>Acordar</li>
        <li>Ligar para a Mari</li>
        <li>Tomar cafe</li>
        <li>Escovar os dentes</li>
        <li>Estudar</li>
        <li>Almocar</li>
        <li>Trabalhar</li>
        <li>Voltar para casa</li>
        <li>Jantar</li>
        <li>Dormir</li>
    </ol>

    <h2>Listas não ordenadas</h2>
    <ul type="circle">
        <li>Pão</li>
        <li>Leite</li>
        <li>Tomate</li>
        <li>Alface</li>
        <li>Manteiga</li>
        <li>Arroz</li>
        <li>Feijão</li>
    </ul>
    <h2>Minhas linguagens favoritas</h2>
    <ol>
        <li>Antigas</li>
        <ol type="I">
            <li>Clipper</li>
            <li>Visual Basic</li>
            <li>Fortran</li>
            <li>Delphi</li>
        </ol>
        <li>Novas</li>
        <ol type="A" start="5">
            <li>Python</li>
            <li>Java</li>
            <li>JavaScript</li>
            <li>Kotlin</li>
        </ol
    </ol>

    <h2>Listas aninhadas</h2>
    <ol>
        <li>NES</li>
        <ul>
            <li>Mario Bros</li>
            <ul type="circle">
                <li>Mario Bros 3</li>
                <li>Mario: Lost Levels</li>
            </ul>
            <li>Ninja Gaiden</li>
        </ul>
        <li>SNES</li>
        <ul>
            <li>Mario</li>
            <li>Donkey Kong</li>
        </ul>
        <li>PlayStation</li>
        <ul>
            <li>Final Fantasy</li>
            <li>Castlevania</li>
        </ul>
    </ol>

    <h2>Listas de definições</h2>
    <dl>
        <dt>HTML</dt>
        <dd>Linguagem de marcaçao para a criaçao de sites</dd>
        <dt>CSS</dt>
        <dd>Linguagem de marcação para o design de sites</dd>
        <dt>JavaScript</dt>
        <dd>Linguagem de programação para a criação de interatividade de sites</dd>
    </dl>
</body>
</html>
~~~

Explicação do código:
usamos a msm base de sempre, fizemos uma lista sequancial e depois uma lista
que não segue uma sequencia, listas aninhadas e uma lista de definição


-----------------------------------------------------------------


## 9: Links externos

Para usarmos links externos no HTML usamos o comando 
~~~html
<a href=" target="" rel""> </a>"
~~~
quando escrevemos apenas a os dois últimos parâmetros não vem junto com eles, porém eh uma boa prática adicionarmos eles, já que estamos falando de links externos que levam a algum outro site

"<href="">" eh onde devemos inserir o link que desejamos que queremos que o usuário seja direcionado

"<target="">" informa oq vai acontecer após o usuário apertar no link, se uma nova guia vai abrir, se vai sobrepor o site e etc
SEMPRE coloque "_blank" quando se trata de algum link externo!!

"<rel="">" serve para dizer se o link eh externo ou interno
SEMPRE coloque "external" quando se trata de link externo!!

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML</title>
    <link rel="shortcut icon" href="images/favicon.ico" type="image/x-icon">
</head>

<body>
    <h1>Usando links externos</h1>
    <p>Você pode me encontrar também no <a href="https://github.com/igorgp06" target="_blank" rel="external">GitHub</a></p>
    <p>Você também pode me encontrar no <a href="https://www.linkedin.com/in/igorgp06/">Linkedin</a></p>
</body>
</html>
~~~

Explicação do código:
aqui criamos um código padrão em HTML, o primeiro link está da maneira recomendada, onde ele vai me levar pro meu GitHub
criando uma nova guia, já o que leva pro meu Linkedin irá sobrepor meu site e não eh isso que queremos


-----------------------------------------------------------------


## 10: Usando links internos e links de downloads

Para usarmos links internos fazemos uma coisa bem parecida com o uso dos links externos, como nosso link interno vai redirecionar o usuário a um link dentro do nosso próprio site onde não tem a necessidade de abrir uma guia nova, nós não usamos o "_blank" e "external"

para dizermos que um link eh interno fazemos o mesmo de sempre, damos o caminho da sub-pasta que ele está (se estiver em uma)
e informamos o seguinte:
~~~html
<a href="#" rel="next" target="_self"</a>
~~~
assim nós informamos que o link eh interno, o "next" quer dizer queo link eh interno, já o "_self" fala que ele vai sobrepor o site atual por outra página nossa

Os links de downloads servem de um jeito parecido, devemos informar onde está o item que o usuário vai baixar, dizer oq o usuário
vai baixar e definir o tipo de item que o usuário vai baixar
~~~html
<a href="#" dowload="" type=""</a>
~~~
no "dowload" dizemos oq o usuário vai baixar e no "type" falamos o tipo de coisa que o usuário vai baixar, visite:
https://www.iana.org/assignments/media-types/media-types.xml
para ver todos os tipos de dowloads que podemos usar

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML</title>
    <link rel="shortcut icon" href="images/favicon.ico" type="image/x-icon">
</head>

<body>
    <h1>Usando links internos</h1>
    <h2>Segunda página</h2>
    <p>Acesse minha segunda página <a href="pag02.html" rel="next">aqui</a></p>
    <p>Acesse também a nossa página de notícias <a href="notices/pag03.html" rel="next" target="_self"> aqui</a></p>

    <h1>Usando links para downloads</h1>
    <ul>
        <li><a href="livros/meulivro.pdf" download="meulivro.pdf" type="application/pdf">Baixar o livro em PDF</a></li>

        <li><a href="livros/meulivro.zip" download="meulivro.zip" type="application/zip">Link para download do livro em ZIP</a></li>
    </ul>    
</body>
</html>
~~~

Explicação do código:
aqui fizemos o básico, usamos os msm exemplos das explicações acima, criamos um link interno que leva para páginas diferentes
e dois links de download para um .pdf e um .zip


-----------------------------------------------------------------


## 11: Imagens adaptativs com HTML5

A responsividade eh fundamental em qualquer site, aqui vamos ver o básico disto usando só o HTML usando os
comandos 
~~~html
<picture> </picture> e <source> </source>
~~~

dentro do "picture" vem o comando "source", acompanhado com o source vem o "<media="">" o "<srcset="">" e por último
vem o "<type="">"

"media" deve ser usado assim:
"<media="(max-width: 000px)">
isto significa que o máximo que a imagem a qual este comando foi atribuído vai crescer até no máximo o número de pixels(px)
que escolhemos e após isso a imagem vai trocar para uma que se adapte melhor no atual tamanho do dispositivo que o usuário
está

"<srcset="">" tem esse uso e função:
"<srcset="image_path">"
ele diz qual a imagem deverá aparecer após o tamanho do site atingir ou passar do tamanho que escolhemos no "media"

"<type="">" tem o uso e função:
"<type="tipo/imagem">"
aqui nós devemo s dizer qual o tipo da imagem, se ela eh um jpeg, um png ou etc

os comandos devem seguir uma sequencia específica, ou seja, se estamos usando o "max-width" dentro do
"media" deve-se usar a sequencia da menor imagem para a maior imagem

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML</title>
    <link rel="shortcut icon" href="images/favicon.ico" type="image/x-icon">

</head>
<body>
    <h1>Imagens dinâmicas</h1>
    <p>Tente abrir esse site em varios dispositivos diferentes ou simplesmente aumente e diminua o tamanho do seu navegador</p>

    <picture>
        <source media="(max-width: 750px)" srcset="images/foto-p.png" type="image/png">
        <source media="(max-width: 1050px)" srcset="images/foto-m.png" type="image/png">
        <img src="images/foto-g.png" alt="foto grande flexível">
    </picture>
</body>
</html>
~~~

Explicação do código:
fizemos o msm de sempre, a diferença eh que dentro do "picture" demos três imagens dinâmicas que se adaptam
sozinhas após o tamanho do navegador atingir certo tamanho, note a sequencia que elas seguem, da menor para a maior


-----------------------------------------------------------------


## 12: Vídeos em HTML

No HTML existem duas formas de colocarmos vídeos no site, sendo elas a forma interna e a forma externa, o nome eh autoexplicativo, ent vou pular explicações

Hospedando de forma interna:

para colocarmos vídeos internos, ou seja, que estão nos arquivos raiz do nosso projeto usamos o comando:
~~~html
<video> </video>
~~~
dentro do comando vídeo podemos adicionar seus parâmetros, ou seja, podemos dizer se os vídeo(s) vão ter os controles básicos, se vão estar em loop, seu tamanho máximo, tamanho mínimo e assim por diante

dentro do comando vídeo, entre as boquinhas devemos apresentar quais vídeos vão aparecer usando o comando:
~~~html
<source src="">
~~~
note que dentro dele precisamos dizer qual vai ser o vídeo exibido, seu tipo e etc, além de que eh uma boa prática colocarmos o vídeo em vários formatos diferente, já que cada navegador pode ou não ser compatível com aql formato de vídeo

Hospedando de forma externa:

esse métado em questão eh mais burocrático que programático, ou seja, devemos tomar MUITO cuidado com os vídeos que hospedamos em
nosso site, já que o dono pode cobrar os direitos autorais, entretanto, caso o vídeo seja do cliente a história muda, ele pode
postar no YouTube para que todos possam ver (publico) ou invisível aos mecanismos de busca (não listado), entretanto, quando estamos
falando de vídeos exclusivos como os de algum curso por exemplo, nós NÃO podemos usar o YouTube já que ai qualquer um pode piratear os
vídeos que deveriam ser exclusivos, para isso podemos usar a ferramenta (paga) do "vimeo", onde ele não permite o compartilhamento
do vídeo, diferente do YouTube

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML</title>
    <link rel="shortcut icon" href="images/favicon.ico" type="image/x-icon">

</head>
<body>
    <h1>Inserindo vídeos hospedando localmente</h1>
    <p>Este vídeo está hospedado no meu próprio servidor</p>
    <video controls poster="images/yunk.png" width="560" height="315">
        <source src="videos/Cadastro E Db.mp4" type="video/mp4">
        <source src="videos/Cadastro E Db.mkv" type="video/mkv">
        <source src="videos/content_warning1.webm" type="video/webm">
        <p>Seu navegador não tem compatibilidade com reprodução de vídeos</p>
    </video>

    <h1>Inserindo vídeos de forma Externa</h1>
    <h2>Usando um vídeo externo do YouTube</h2>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/rWr3unZs-vE?si=zyIsouQKo1HTpiMj" 
     title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; 
     gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" disablefullscreen></iframe>

    <h2>Podemos usar o vimeo também, porém ele eh pago e caro</h2>
</body>
</html>
~~~

Explicação do código:
aqui usamos o msm de sempre, mostramos como hospedar um vídeo localmente (ñ recomendado) e como hospedar
um vídeo de maneira externa (recomendado) 


-----------------------------------------------------------------


## 13: Cores

Dentro do CSS podemos alterar as cores, leia sobre os detalhes de como usar as cores e quais ferramentas usar
veja o PDF do Curso em Vídeo

Para darmos cores ao fundo de algo nós usamos o "background-color:  " e depois informamos a cor da mesma, já para 
fazermos cores lineares que começam em uma e vão mudando gradativamente para outra nós usamos o
"background-image: linear-gradient( );" 
dentro dos parênteses nós devemos dizer de onde ela vai vim, por exemplo o "(to right, )" ou podemos fazer isso usando
graus "(90deg, )" e depois colocarmos as cores separadas por vírgula

O "color: ;" serve literalmente para dizer a cor de algo, se ali colocassemos black, o objeto ser ser todo preto


-----------------------------------------------------------------


## 14: Tipografia

Prestar atenção nas serifas, nas fontes que possuem serifas. Não muito diferente das cores, as fontes devem seguir um 
padrão visual, devem ter como se fosse uma regra de vestimenta, onde pra apresentarmos assuntos sérios nos devemos 
manter uma fonte séria, fechada sem decorações já que ela remete a importância e atenção do usuário, isso vale para todos
os tipos de fontes, estilos e assuntos a serem tratados naquele momento

Não muito diferente das imagens, as fontes também sofrem de incompatibilidade, isso significa que certas fontes podem ou não serem
incompativeis com certos dispositivos e navegadores, por isso nós combinamos as fontes na hora de montar o site, assim:
"font-family: Arial, Helvetica, sans-serif;"

isso se chama safe combinations, pois caso ele não encontra uma ele pula para a outra e isso se repete até uma fonte compativel
for encontrada, recomenda-se sempre no final da safe combination por uma fonte genérica como a "sans-serif" que SEMPRE vai ser
identificado independente do dispositivo ou navegador

Visite o site:
https://www.w3schools.com/cssref/css_websafe_fonts.php
para ver todas as fontes seguras (safe combination)

### 14.1: Tamanhos de Fontes

Recomenda-se seguir oq foi imposto pelas normas da "W3C"
Existem dois tipos de tamanhos de fontes dentro da criação de sites, sendo elas:

-Medidas Absolutas:
cm = Centímetros
mm = Milímetros
in = Polegada
px = Pixel
pt = Ponto: medida de datilografia, não recomendado para exibir conteudo em tela
pc = Paica: medida de datilografia, não recomendado para exibir conteudo em tela

Alguns problemas relacionados as tamanhos das fontes absolutas são a diferença de tamanho entre os dispositivos, existem
situações que as pessoas vão ver os sites em diferentes ligares a as vezes o navegador do usuário não vai conseguir
alcançar o 1cm que foi imposto sobre o tamanho da fonte

-medidas relativas;
em = Relativo ao tamanho atual da fonte
ex = Relativo ao tamanho da letra "x" de uma fonte
rem = Relativo ao root que está configurada no body
vw = Relativo ao "view-port" do dispositivo (largura em %)
vh = Relativo ao "view-port" do dispositivo (altura em %)


O em: Segue o tamanho do "M" de uma fonte
O ex: todas as fontes seguem a medida da letra x quando estão em minusculas, tendo seu corpo pricipal dentro de uma única medida
(Recomendo ver o pdf do curso em vídeo para mais detalhes)

Recomenda-se, além de seguir as normas da W3C, sempre dar preferência ao uso do "px" para tamanhos definitivos e "em" para os
tamanhos relativos

### 14.2: Peso, Estilo e Shorthand

Usando o comando "font-weight: ;" nós conseguimos dar um peso para a nossa fonte, existindo alguns nome de pesos literais, sendo eles:
-lighter
-normal
-bold
-bolder
ou nós podemos usar números para definir o peso da fonte, sendo o 400 o peso padrão das fontes

Usando o "font-style: ;"nós podemos definir o estilo da fonte, deixando ela em itálico por exemplo, já o "text-decoration: ;" nós
podemos defnir a decoração do texto, assim nós podemos deixa-lo sublinhado por exemplo 

Usando as shorthand nós podemos fazer com uqe 4 linhas de código em CSS acabem virando uma única linha, tendo o nome de "shorthand font", ela
segue obrigatoriamente uma sequência, sendo ela "font-style -> font-weight -> font-size -> font-family", assim:

"font: italic bolder 3em 'Work Sans, sans-serif;"

deste jeito nós conseguimos fazer que 4 linhas virem uma única linham, deixando o código ligeiramente menor e fazendo também que
nós escrever menos


-----------------------------------------------------------------


## 15: Seletores

Dentro do HTML nós podemos dar classes(class) e identificadores(id) para as coisas, e dentro do CSS nós podemos chamar essa classe ou id separadamente, assim
nós podemos personalizar cada item específico do nosso site sem alterar os genêricos. Para chamarmos os seletores do HTML no CSS nós usamos:
id = #
class = .
pseudo-class = :
pseudo-element = ::
children = >

Segundo as normas do W3C, não se deve usar dois id para diferentes coisas, neste caso vc deve usar uma class, normalmente nós usamos class para quando
queremos colocar vários elementos usando o mesmo nome de classe, resumindo:
id = elemento único (1000 de prioridade)
class = multiplos elementos (100 de prioridade)
o id sempre vai ter preferência sobre as classes, isso significa que se um elemtno estiver dentro de uma classe com a configuração X e um id único com configuração
Y, a configuração Y vai sobrepor a configuração X

Nós podemos colocar duas classes num mesmo elemento, pra isso basta colocar o nome das classes desejadas dentro dos parentêses com um  espaço, não
precisa por vírgula para separar os nomes

### 15.1: Pseudo-Class

Para nós representarmos uma pseudo-class nós usamos o ":", ela precisa estar se referindo ao elemento ou uma classe, ela se refere ao estado de um 
elemento(ativo, desligado, marcado, vazio e etc), por exemplo, digamos que tenhamos uma div e dentro do css fizemos o seguinte:

~~~css
div:hover {
    background-color: rgb(255, 255, 255);
}
isso significa que quando nós passarmos o mouse por cima da div algo foi acontecer, neste caso ela vai mudar a cor de fundo dela para a
cor branca
~~~

Dentro do CSS nós podemos costumizar os filhos q estão dentro do algo, por exemplo, se temos uma div e dentro desta div nós temos um parágrafo (p), usando
o ">" nós podemos dizer que dentro da div queremos que o p seja ou faça isso, exemplo:

~~~css
div > p {
    display: none;
}
básicamente aqui nós estamos informando ao CSS que o <p> dentro da <div> terá seu exibição escondida
~~~

Nós podemos também misturar os métados, ou seja, podemos usar uma pseudo-class e uma child selector ao mesmo tempo, assim:

~~~css
div:hover > p {
    display: block;
    color: white;
}
isso quer dizer que quando o mouse passar por cima da <div> o <p> que anteriormente estaja escondido vai aparecer na cor branca
~~~

Exemplo extras de pseudo-class:

~~~css
a {
    color: rgb(112, 108, 53);
    text-decoration: none;
    font-weight: bold;
}

a:visited {
    color: rgb(63, 61, 29);
}

a:hover {
    color: black;
    text-decoration: underline;
}

a:active {
    color: rgb(255, 255, 255);
}
aqui nós criamos um link com a tag <a> e definimos seu atributos, isso significa respectivamente que o <a> vai ter uma seu estilo padrão,
depois de visitado terá outra cor, quando passar  mouse por cima ele vai ter uma cor e uma decoração e por último quando apertado ele vai ter
uma outra cor
~~~

### 15.2: Pseudo-Elements

Os pseudo-elements mexem diretamente com o conteudos das tags do HTML, diferente da pseudo-class que mexe com a estilização. Para nós
definirmos um pseudo-element nós usamos dois "::", exemplo:

~~~css
a::after {
    content: '[ LINK]';
    text-decoration: none;
    font-weight: normal;
    color: white;
}
isso aqui quer dizer que após o link ter sido aberto nós vamos adicionar um text escrito " [LINK]" junto da sua
decoração que vem logo após o "content: ;"
~~~

Lembrese que nós podemos mexer nos conteudos dos pseudo-elements podem ser um "id" ou uma "class", fazemos isso da mesma maneira que
normalmente fazemos com o pseudo-class


-----------------------------------------------------------------


## 16: Modelos de Caixas e shorthands úteis

Os conteudos do HTML são separados por caixas, onde uma pode ser colocada dentro da outra, criando uma hierarquia/aninhamento, as caixas
tem tamanhos, sendo eles:
height = altura da caixa
width = largura da caixa

Nós podemos traçar linhas com volta dos conteudos usando o "border", ela contorna a caixa o mais próximo possível dependendo da altura e largura

O "padding" serve para nós aumentarmos a folga(preenchimento/alchoamento) da borda, nós podemos fazer o padding para qualquer
direção de nossa escolha

Para alterarmos a borda externa do border nós usamos o "margin", ele não altera o tamanho da caixa, porém altera seu contorno externo

"outline" eh o termo usado para o conteudo que fica entre o border e entre o margin

Existem dois tipos de caixas dentro do HTML, sendo elas do tipo "box-level" e o "inline-level", veja detalhes abaixo:
 box-level = digamos que temos um parágrafo incompleto e queremos criar um novo parágrafo dentro do elemento, o box-level vai pular essa
linha e preencher a largura da linha de baixo já que os elementos em box-level preenchem 100% da view-port do dispositivo, exemplo:
<div></div>
<p></p>
<nav></nav>
...etc...

 inline-level = ele faz justamente o contrário do box-level, ela se ajusta para caber dentro do parágrafo por exemplo, sem quebrar
as linhas e continuando o conteúdo a seguir dela, ocupando somente o tamanho que ele precisa, exemplo:
~~~html
<span></span>
<a></a>
<em></em>
...etc...
~~~

Existe diversas formas de simplificar os comandos no CSS, um exemplo disso são as bordas, normalmente para podermos dizermos as bordas nós usamos:

~~~css
border-width:
border-style:
border-color:
~~~
porém, existe um jeito de simplificar isto, podemos simplesmente fazer isso:

~~~css
boder: 10px solid black;
~~~
na mesma sequencia que fizemos no comando onde usamos três linhas, usamos apenas uma única linha para passarmos três atributos a um único elemento.

e quando nós temos o "padding" e nós usamos:

~~~css
padding-top: ;
padding-right: ;
padding-bottom: ;
padding-left: ;
~~~
desse jeito nós usamos 4 linhas para um único elemento enquanto podíamos(nessa ordem) termos feito isso de uma maneira mais simplificada com:

~~~css
padding: 10px 10px 10px 10px;
~~~

se todos os lados do "padding" forem iguais nós podemos usar apenas 1 10px, assim:

~~~css
padding: 10px;
~~~

podemos interpretar assim:
4 valores = configuração de cima, direita, baixo e esquerda
2 valores = o de cima e de baixo ficam iguais enquanto o dos lados ficam iguais, respectivamente
1 valor = o mesmo para todos 

podemos fazer o mesmo para vários comandos do CSS, isso inclui o "margin" por exemplo também.

Podemos transformar elementos para in-line com o 
~~~css
display: inline;
~~~

ou transformá-los em block-level assim:

~~~css
display: block;
~~~

com o
~~~css
display: inline-block;
~~~
podemos fazer com que um elemento continue no in-line porém agora ele eh capaz de receber características do block-level


-----------------------------------------------------------------


## 17: Grouping tags semânticas

Antigamente era muito comum o uso excessivo de divs no HTML4, porém com os avanços do HTML5 existe uma semântica a ser seguida por bom costume e boas práticas no mundo da programação, por exemplo, temos o:
~~~html
<header> </header>
~~~
que usamos para o cabeçalho do site, onde normalmente ficam as coisas que ficam no topo. Não confunda head com header e assim por diante

Um exemplo de um site semântico é:

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<title>Grouping Tags</title>
	<link rel="stylesheet" href="style.css" />
</head>
<body>
	<header>
		<h1>Grouping Tags</h1>
			<nav>
				<a href="#">Home</a>
				<a href="#">About</a>
				<a href="#">Contact</a>
			</nav>
	</header>
	<main>
		<section id="assuntos"></section>
		<section id="noticias">
			<article>
				<h2>Noticias sobre o Brasil</h2>
				<p>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem
					mollitia hic culpa dolor, magnam suscipit sunt maiores explicabo,
					earum consectetur unde? Rem, amet expedita suscipit delectus
					accusantium sit tempora quis!
				</p>
				<aside>
					<p>Criado por Igor Gonçalves</p>
			</aside>
			</article>
		</section>
		<article></article>
		<article></article>
	</main>
	<footer>
		<p>Copyright &copy; Igor Gonçalves | DEV 2024</p>
	</footer>
</body>
</html>
~~~

essas tags podem ser organizadas de várias maneiras, nada impede de usar um monte de div, porém a boa prática para um bom site eh seguir a semântica, usando artigos, navs, assides e ir brincado com eles, entender que existem diversas formas de organizá-los e estilizá-los.

o CSS do nosso site ficará muito mais bonito, ficará mais fácil a organização e manutenção, temo o exemplo abaixo de como ele ficaria:

~~~css
body {
	font-family: Arial, Helvetica, sans-serif;
	background-color: darkslategray;
	margin: 0px;
}

header {
	background-color: white;
	padding: 10px;
	margin: 10px;
}

nav {
	background-color: lightgray;
	padding: 3px;
}

nav > a {
	text-decoration: none;
	color: white;
	font-weight: bold;
	margin-right: 30px;
}

nav > a:hover {
	text-decoration: underline;
}

main {
	background-color: white;
	padding: 10px;
	margin: 10px;
}

article {
	color: lightslategrey;
	padding: 5px;
}

article > aside {
	background-color: lightgray;
}

footer {
	background-color: black;
	color: white;
	text-align: center;
	padding: 1px;
	margin: 0px;
}
~~~


-----------------------------------------------------------------


## 18: Sombra nas caixas

As sombras são muitas vezes detalhes essenciais em diversos sites, porém cuidado com o exagero de sombras, JAMAIS exagere do uso das sombras. 

Para podermos dar uma sombra básica a um elemento nós usamos o termo 
~~~css
box-shadow: 1px 1px 1px black;
~~~
eh importante saber que os termos do box-shadow podem ser resumidos numa única shorthand, nessa sequencia a shorthand do "box-shadow" é, respectivamente:
1. deslocamento horizontal; 
2. deslocamento vertical;
3. espalhamento.
e um regra não falada eh nunca colocar uma sombra colorida ou ela não pode ser de cor sólida, de preferencia sempre a uma sombra espalhada, não muito chamativa e com uma baixa opacidade.


-----------------------------------------------------------------


## 19: Vértices arredondados

O arredondamento de caixas eh muito comum em sites, o comando para fazermos uma borda mais arredondada é:
~~~css
border-radius: ;
~~~
ela também tem uma shorthand, onde se todos os lados da borda tiverem um mesmo valor podemos passar um único número, caso contrário, podemos passar os valores individuas com essa ordem de precedência:

~~~css
1. border-top-left-radius: 5px;
2. border-top-right-radius: 5px;
3. border-bottom-right-radius: 5px;
4. border-bottom-left-radius: 5px;
~~~

pode-se também passar somente duas características, exatamente como na margem.

Usando o arredondamento de vertices podemos até mesmo criarmos elementos redondos, observe o HTML e o CSS:

~~~html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<title>Grouping Tags</title>
	<link rel="stylesheet" href="style.css" />
</head>
<body>
	<header>
		<h1>Grouping Tags</h1>
		<nav>
			<a href="#">Home</a>
			<a href="#">About</a>
			<a href="#">Contact</a>
		</nav>
	</header>
	<main>
		<section id="assuntos">
			<p>Esportes, Politica e Tecnologia</p>
		</section>
		<section id="noticias">
			<article>
				<h2>Noticias sobre o Brasil</h2>
				<p>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. 
					mollitia hic culpa dolor, magnam suscipit sunt maiores 
					earum consectetur unde? Rem, amet expedita suscipit delectus
					accusantium sit tempora quis!
				</p>
				<aside>
					<p>Criado por Igor Gonçalves</p>
				</aside>
			</article>
		</section>
		<article></article>
		<article></article>
	</main>
	<footer>
		<p>Copyright &copy; Igor Gonçalves | DEV 2024</p>
	</footer>
	<div id="bola"></div>
</body>
</html>
~~~

~~~css
body {
	font-family: Arial, Helvetica, sans-serif;
	background-color: rgb(66, 66, 66);
	margin: 0px;
}

header {
	background-color: white;
	padding: 10px;
	margin: 10px;
}

nav {
	background-color: lightgray;
	padding: 3px;
}

nav > a {
	text-decoration: none;
	color: white;
	font-weight: bold;
	margin-right: 30px;
}

nav > a:hover {
	text-decoration: underline;
}

main {
	background-color: white;
	padding: 10px;
	margin: 10px;
	border-radius: 5px;
}

article {
	color: rgb(66, 66, 66);
	padding: 5px;
}

article > aside {
	background-color: lightgray;
}

footer {
	background-color: black;
	color: white;
	text-align: center;
	padding: 1px;
	margin: 0px;
}

footer > p {
	margin: 0px;
}

div#bola {
	height: 100px;
	width: 100px;
	margin: 10px;
	background-color: white;
	border-radius: 50%;
}
~~~

preste atenção na última div do HTML e na do CSS, observe como usamos a borda em porcentagem para fazermos um bola usando somente o controle das bordas.


-----------------------------------------------------------------


## 20: Variáveis em CSS

Sabemos que diversas linguagens trabalham com variáveis, o  CSS não foge muito dessa ideia. Para que seja possível a criação de uma variável no CSS nós usamos o root, desse jeito:

~~~css
:root {
	
}
~~~
assim desse jeito tudo que for colocado dentro do root vai passar a ser uma regra, pois ele eh a raiz do projeto e estamos mexendo diretamente na raiz com o root.

entretanto ainda não temos variáveis dentro do root, para podermos criar elas devemos usar o "--" antes de instanciar o nome da variável, observe um exemplo mais prático:

~~~css
:root {
	--cor1: rgb(197, 235, 214);
	--cor2: rgb(131, 225, 173);
	--cor3: rgb(61, 220, 132);
	--cor4: rgb(47, 168, 102);
	--cor5: rgb(26, 92, 55);
	--cor6: rgb(6, 61, 30);
}
~~~
assim vemos um exemplo prático de como usar essas variáveis, desse jeito podemos criamos uma especie de central de cores, podendo adicionarmos quantos itens quiser com os nomes que quisermos.

Uma das vantagens de usarmos essas variáveis eh o fato de que basta alterarmos uma única vez a cor diretamente da variável que todas as outras que recebem essas variável vão automaticamente se alterar junto, facilitando alterações.


-----------------------------------------------------------------


## 21: Responsividade Básica

A responsividade eh algo básico quando falamos de desenvolvimento web, ter um site responsivo e adaptativo para qualquer dispositivo eh um pilar fundamental para um desenvolvedor web. Uma maneira básica de tratar da responsividade eh usando os termos do CSS que definem uma altura e largura máxima e/ou mínima, por exemplo:

~~~css
main {
	min-width: 320px;
	max-width: 800px;
	margin: auto;	
}
~~~
esse eh um exemplo muito básico de responsividade básica, isso quer dizer que o conteúdo que se localiza no main (com exceção das imagens por exemplo) vão se adaptar para ter uma tamanho máximo e um minimo enquanto permaneçam sempre localizados ao centro do site.

Para a imagem podemos apenas fazer isso:

~~~css
img {
	width: 100%;
}
~~~
não eh o melhor método de se fazer isso, porém eh uma possibilidade.

Um método de trabalhar com a responsividade eh usando o termo picture, ele serve como um if e else, podemos interpretar o uso do "picture" junto do "source" e a "img" como um if e else, onde quando atinge certo tamanho a imagem muda para se adaptar a necessidade do usuário, veja o exemplo:

~~~html
<picture>
	<source media="(max-width: 600px)" srcset="imagem menor q a original">
	<img src="imagem original" alt="irina criadora do bugdroid"/>
</picture>
~~~
neste exemplo caso o tamanho da tela do usuário for menor que 600px automaticamente o "source" vai entrar em ação, alterando a imagem original por uma adaptativa confronte o tamanho da tela do usuário.


-----------------------------------------------------------------


## 22: background-image

Nós podemos usar imagens personalizadas estáticas, isso quer dizer que elas não precisam necessariamente ter uma interação com o usuário ou fazer parte de algum conteúdo, ela pode simplesmente ser estática como uma mera decoração. Um exemplo básico para que seja possível usarmos uma imagem de fundo num div por exemplo é informando a url dela, desse jeito:

~~~css
div#q3 {
	background-image: url('static/images/pattern001.png');
}
~~~
assim desse jeito pegamos uma div com o id igual a "q3" e passamos o caminho da imagem que nós queremos usar.

Por padrão, todas as imagens quando carregadas vão ser em seu tamanho padrão, ou seja, elas não vão automaticamente se adaptar ao tamanho de fundo do site ou qualquer outra coisa.

Pode ser usado também imagens de fora, com os links externos, bastando apenas botar o link da imagem no lugar do caminho. é válido lembrar que 

-----------------------------------------------------------------


## 23: background-repeat 

As repetições das imagens sempre serão repetidas para se ajustarem o tamanho da viewport. Agora que entra o "background-repeat", ele tem alguns comandos aceitos, como o repeat, no-repeat. Temos alguns repeats mais específicos, como o o repeat-y e o repeat-x, seus nomes são autossugestivos e sempre começam do canto superior esquerda da viewport..


-----------------------------------------------------------------






-----------------------------------------------------------------





-----------------------------------------------------------------









-----------------------------------------------------------------











-----------------------------------------------------------------



-----------------------------------------------------------------


## --: Observações Importantes

para adicionarmos comentários em HTML, usamos "<!-- -->", lógicamente dentro do espaço
que sobrou adicionamos nosso comentário

Preste atenção na semântica! Pense no significado das palavras e não nos resultados, ou seja:
sentido/semântica faz no HTML
forma/estilo faz no CSS

No CSS tudo oq for uma ID eh representada por uma #
já a classe eh representada por um .

o * representa uma configuração global, desse jeito:
~~~css
* {
	margin: 0px;
	padding: 0px;
}
~~~
assim desse jeito **todos** os elementos do HTML não vão ter margem e nem um padding.


-----------------------------------------------------------------





