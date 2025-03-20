

---------------


## 1: Básico do JavaScript

No JavaScript podemos dar alertas básicos no nosso navegador, sendo elas de alerta, confirmação e um
prompt de alguma informação

usando o "window.alert("")" criamos uma alerta assim que abrimos o site

o "window.confirm("")" é para perguntar se o usuário aceita algo ou não

já o "window.prompt("")" serve para o usuário dar alguma informação que queremos solicitar

Exemplo:

window.alert("Olá mundo!")
window.confirm("Olá mundo!")
window.prompt("Olá mundo!")

Explicação do código:
um simples código em JS que faz oq explicamos ali em cima


-----------------------------------------------------------------


## 2: Variáveis e tipos primitivos

As variáveis no JS seguem algumas regras básicas, sendo elas:
podem começar com letra, $ ou _;
não podem começar com números porém eh possível usar eles depois;
pode usar acentos e símbolos;
não pode contar espaços, use o _ para representar um espaço;
não podem ser palavras reservadas do JS

os tipos primitivos funcionam de um jeito muito perecido com o Python, ou seja,
true eh um boleano
123 eh um number
"olá, mundo" eh uma string e assim em diante

para ver o tipo de uma variável usamos o comando "typeof"	

existem três formas de atribuirmos uma variável, sendo elas:
let = pode ser alterado quantas vezes quiser
const = Valor permanente, não pode ser alterado sob nenhuma circunstância
var = ESCOPO GLOBAL, NUNCA USE ISSO

Uma medida padrão das variáveis eh que normalmente as variáveis devem sempre ser primeiro um const já que isso pode precaver conflitos de dados ou nomes de variáveis, caso seja necessário fazer com que o const seja alterado basta apenas mudar do const para let e seguir o código.


-----------------------------------------------------------------


## 3: Tratamento de dados

Para tratarmos dados no JS  eh um pouco diferente, quando se pegamos informações do window.prompt("")
elas serão tratadas como string, sendo número ou não, com a exceção do null

para transformar algo em número no JS, seja uma int um float, devemos declarar ele obrigatóriamente

para tranformar uma string para um int ou float usamos:
"Number.perseInt()" para inteiro
"Number.perseFloat()" para um float
o number não eh obrigatário, porém eh uma boa prática usar ele.Isso eh importante principalmente 
para quando tratamos dados, já que o JS usa o + para soma de números e a concatenação de números, string e etc
 
lembre-se, o novo JS entendo quando usamos somente o Number, o "perseInt()" e o "perseFloat()" eh usado somente
quando queremos forçar o mesmo

Para convertemos algo para string, existem dois jeitos de fazer isto, sendo eles:
String()
n.toString()
note que na segunda forma a variável vem antes do comando em si

No JS existe algo muito parecido com a f string do python, para usarmos estas formatações fazemos assim:
(`exemplo 1 será mostrado a seguir: ${}`)
simples assim, basta adicionamos o $ dentro das crases (``) e oq desejamos mostrar dentro das chaves

O comando "document.write()" tem uma função parecida com a do print, ele escreve diretamente no site oq
passamos dentro dos parenteses dele

Para fazermos uma limitação de caracteres a serem exibidos, como nós faziamos no Python com o f strings
fazendo assim: print(f"Número 1 igual: {n1.:2f}")
no JS podemos fazer coisa parecida, porém o comando eh um pouquinho diferente, após usarmos o ${}
para declaramos oq vai dentro dos parentêses nós devemos adcionar o ".toFixed()" e dentro dos parentêses
devemos declarar quantas casas serão fixadamente exibidas, assim:
var n1 = window.prompt('Escreva um número: ')
var n2 = window.prompt('Escreva outrp número: ')

var soma = Number.perseFloat(n1) + Number.perseFloat(n2)

document.write(`A soma de ${n1} + ${n2} = ${soma.toFixed(2)}`)

e para darmos uma certa beleza a como nosso resultado vai apareçer podemos substituir o "." por ",",
isso eh muito importante já que na programação o "." representa vírgula, diferente da vida real. Para fazermos
isso usamos o comando ".replace()", simples assim

podemos usar o ".replace()" após u ".toFixed()", isso deixaria nosso código com essa cara mais ou menos:
var n1 = window.prompt('Escreva um número: ')
var n2 = window.prompt('Escreva outrp número: ')

var soma = Number.perseFloat(n1) + Number.perseFloat(n2)

document.write(`A soma de ${n1} + ${n2} = ${soma.toFixed(2).replace('.', ',')}`)


-----------------------------------------------------------------


## 4: Operadores Aritméticos

os operadores também seguem uma lógica de precedência, sendo assim:
operadores aritméticos
operadores relacionais
operadores lógicos

No JS, os operadores básicos são parecidos com o do Python, sendo eles:
+ = soma
- = subtração
* = multiplicação
/ = divisão normal, com vírgula
% = divisão inteira, quando chega na vírgula para a conta e o número que "sobrou" vira o resultado
** = potência
Exemplos:
5 + 2 = 7
5 - 2 = 3
5 * 2 = 10
5 / 2 = 2.5
5 % 2 = 1
5 ** 2 = 25 

e sim, eles tem uma ordem de precedência, sendo elas:
()
**
* / %
+ -

### 4.1: Atribuições

as atribuições são coisas parecidas com oq já vimos no Python, onde ao invés de fazermos aquela
conta enorme para atribuir uma variável a algum valor

Atribuição Simples:  
Var a = 5+3 : 8
Var b = a% 5 : 3
Var c = 5* b ** 2 : 45
Var d = 10 – a / 2 : 6
Var e = 6 * 2 / d : 2
Var f = b % e + 4 / e : 3

Auto atribuição:
Var n = 3
n = n + 4
n = n - 5
n = n * 4
n = n / 2
n = n ** 2
n = n % 5

Simplificando:
n += 4
n -= 5
n *= 4
n /= 2
n **= 2
n %= 5

Incremento:
Var x =5
X=x+1   x++ (simplificado)
X=x-1   x-- (simplificado)

4.2: Relacionais

ainda muito parecidos com o do Python e com a matemática da vida real, normalmente quando falamos de
operadores relacionais eles vão devolver valores boleanos, os operadores relacionais são eles:

~~~js
>
<
>=
<=
==
!=
=== (identidade)
Exemplos:
5 > 2 = true
7 < 4 = false
8 >= 8 = true
9 <= 7 = false
5 == 5 = true
4 != 4 = false
5 === '5' = false
~~~

O JS não diferencia os tipos de string e números em alguns casos, ou seja, podemos
fazer a comparação de dois int que vai retornar um true e um int e uma str que também vai
retornar um true, isso pq o JS analisa a grandeza dos valores tbm
exemplo:
5 == 5 = true
5 == '5' = true
normalmente, nestes casos usamos o === para verificarmos a identidade de algo, onde ele vai comparar
se os dados são iguais, tanto em valores tanto quanto em str, int e assim por diante.
podemos também usar o !== que serve para práticamente a msm coisa que os três sinais de igual, onde ele vai apontar se são exatamente iguais em todos os sentidos e retornar um boleano
exemplo:

~~~js
5 === '5' = false
5 === 5 = true

let x = 5
let y ='5'

x !== y = false
~~~

### 4.3: Lógicos

~~~js
! = negação
$$ = conjunção
|| = disjunção
eles também seguem uma ordem de precedência, sendo essa a msm q vc está vendo aq em cima

exemplos:
! true = false
! false = true

true $$ true = true
true $$ false = false
false $$ true = false
false $$ false = false
aq básicamente o true só vai retornar se os dois valores forem verdadeiros

true || true = true
true || false = true
false || true = true
false || false = false
aq basta que apenas um seja true para q meu resultado que vai voltar seja verdadeiro tbm
~~~

### 4.4: Ternário

? :
teste ? true : false
estes tipos de operadores ficam na msm linha de código, eles juntam 3 blocos, básicamente,
se o primeiro for false ele vai retornar algo SE NÃO ele vai retornar outra coisa, os resultados
vão depender unicamente e exclusivamente do primeiro teste lógico da linha deste código
exemplos:

var media = 5.5
media>=7.0?"Aprovado":"Reprovado" = "Reprovado"

var media = 8.0
media>=7.0?"Aprovado":"Reprovado" = "Aprovado"


-----------------------------------------------------------------


## 5: DOM

O DOM nada mais eh do que uma árvore de hierarquia, onde cada coisa fica separada, como se fosse uma árvore
genialógica, cada um tendo seu pai e filhos, ou parent e children
a sigla DOM significa: Document Object Model

podemos navegar dentro dos elementos DOM pelas seguintes maneiras:

Marca:
.getElementsByTagName('')[]
este comando fica do document
podemos pegar vários elementos, ou seja, podemos pegar vários elementos em um paragrafo do html os colchetes servem para escolhermos manualmente os elementos caso o Elements dentro do comendo
acima esteja em plural, se o Element estiver no singular ele vai pegar todos os elementos

ID:
.getElementById('')
ele serve para mudar os elementos em HTML usando a id do elemento, basicamente eh como se nós
dessemos uma identificação a elementos muito grandes, quando se falamos de familias (DOM) muito
complexos

Nome:
.getElementsByName()[]
normalmente usado para selecionarmos por nomes, quando temos muitos elementos

Classe:
.getElementsByClassName()[]

Seletor:
querySelector()
querySelectorAll()
ele serve principalmente para seleções e alterações mais precisas, quando não são muitos elementos que
vão ser alterados, basicamente modificando e selecionando elementos diretos do CSS
tenha em mente que o querySelector() eh recente, ou seja, nem todos os navegadores tem a capacidade de executar ele

### 5.1: Eventos DOM

Os eventos DOM são básicamente um conjunto de ações e eventos, ou seja, oq vai acontercer quando o usuário clicar
em um botão? vai executar uma ação

para criarmos uma função dentro do JS usamos a palavra chave "function" e depois disso damos seu nome, exemplo:

function acao() {

}

dentro dos parênteses vem os parâmetros

existem inúmeros eventos que podem acontecer dentro de um site, clique de mouse, mouse houver, touch da tela do
celular e assim por diante, dentro do HTML podemos usar os comandos pré-definidos que usamos dentro de alguma div,
exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML, CSS e JS</title>
    <link rel="shortcut icon" href="image/favicon.ico" type="image/x-icon">
    <link rel="stylesheet" href="style.css">
    
</head>

<body>

    <div id="area" onclick="clicar()" onmouseenter="entrar()" onmouseout="sair()">
        <p>Clique em mim</p>
    </div>

</body>
<script src="script.js"></script>
</html>
~~~

isso no JS ficaria assim:

~~~js
const area = document.getElementById('area')

function clicar() {
    area.innerText = 'Clicou!'
    area.style.backgroundColor = 'red'
}

function entrar() {
    area.innerText = 'Entrou!'
    area.style.backgroundColor = 'green'
}

function sair() {
    area.innerText = 'Saiu!'
    area.style.backgroundColor = 'blue'
}
~~~
nós criamos várias funções pra cada uma das possíveis coisas que podem acabar acontecendo dentro do
nosso site, agora imagina ter que fazer isso uma por uma pra cada interatividade do site?
existe um comando que facilita isso, eles são como se fossem ouvidinhos que ficam prestando
atenção sempre que algo acontece dentro site

para que isso acantoteca vamos pegar a msm div do HTML que vimos acima

usando o comando:
.addEventListenet()
nós podemos adicionar estes ouvidinhos, para isso dentro dos parênteses vamos pegar o evento do HTML e por
dentro de aspas e depois, separado por vírgula qual o comando q ele vai executar, exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML, CSS e JS</title>
    <link rel="shortcut icon" href="image/favicon.ico" type="image/x-icon">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="area">
        <p>Clique em mim</p>
    </div>
</body>
<script src="script.js"></script>
</html>
~~~

No JS:

~~~js
const area = document.getElementById('area')

area.addEventListener('click', clicar)
area.addEventListener('mouseenter', entrar)
area.addEventListener('mouseout', sair)

function clicar() {
    area.innerText = 'Clicou!'
    area.style.backgroundColor = 'red'
}

function entrar() {
    area.innerText = 'Entrou!'
    area.style.backgroundColor = 'green'
}

function sair() {
    area.innerText = 'Saiu!'
    area.style.backgroundColor = 'blue'
}
~~~
perceba como o nosso código HTML ficou menos poluido e mais claro, deixando o mesmo muito mais fácil
de dar manutenção

Podemos pegar diversas informações usando o HTML e as processando com o JS, ou seja, básicamente a interatividade
da coisa toda, exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML, CSS e JS</title>
    <link rel="shortcut icon" href="image/favicon.ico" type="image/x-icon">
    <link rel="stylesheet" href="style.css">
    
</head>

<body>

    <h1>Soma de valores</h1>
    <input type="number" name="n1" id="n1">
    <input type="number" name="n2" id="n2">
    <input type="button" value="somar" onclick="somar()">

    <div id="show-result">
        resultado
    </div>

</body>
<script src="script.js"></script>
</html>
~~~

No JS:

~~~js
function somar() {
    var n1 = document.getElementById('n1')
    var n2 = document.getElementById('n2')

    var showResult = document.getElementById('show-result')

    var result = Number(n1.value) + Number(n2.value)

    showResult.innerHTML = result
}
~~~
Aqui nós criamos uma página simples com funções simples, pegamos dois números com o INPUT do HTML,
atribuimos a eles a duas váriaveis e depois dentro da mesma function somamos os valores inseridos pelo
usuário e depois apresentamos o resultado com o .innerHTML


-----------------------------------------------------------------


## 6: Condições

Funcionam de um jeito muito parecido com o Python, seguem a mesma lógica, sendo o IF seguindo a mesma
lógica de todos os outros, entretanto, a escrita de como esse comando funciona eh diferente, isso significa que
o IF nós escrevemos assim:

if () {

}

dentro dos parentêses nós damos suas condições e situações, já dentro das chaves instruimos oq vai acontecer quando as situações
que instruimos foram atendidas

o ELSE funciona da mesma maneira que tudo mais, porém o seu posicionamento eh diferente, no JS ele fica dentro da indentação do IF,
o deixando assim:

if () {

} else {

}

Exemplo:

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprendendo HTML, CSS e JS</title>
    <link rel="shortcut icon" href="image/favicon.ico" type="image/x-icon">
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <h1>Multas</h1>
    <p>Sua velocidade</p>
    <input type="number" name="txtvel" id="speed-input">    
    <input type="button" value="checar" onclick="checkSpeed()">
    <div id="res">
        
    </div>

</body>
<script src="script.js"></script>
</html>
~~~

No JS:

~~~js
function checkSpeed() {
    var speed = document.getElementById('speed-input').value
    var div_res = document.getElementById('res')

    var vel = Number(speed)

    res.innerHTML = `<p>Velocidade atual: ${vel} </p>`

    if (vel > 60) {
        div_res.innerHTML = `<p>Voce ultrapassou o limite de velocidade permitida</p>`
    } else {
        div_res.innerHTML = `<p>Voce está dentro da velocidade permitida</p>`
    }
}
~~~
Explicação do código:
aqui temos um códdigo simples em HTML e JS, básicamente ele pergunta ao usuário seu atual velocidade, e após o
usuário inserir a velocidade, dentro do function que temos dentro do JS ela calcula se a velocidade está acima dos
60km permitido ou não 

### 6.1: Condições Aninhadas

Eh como se fosse uma condição dentro da outra, aqui neste caso nós usamos um IF e ELSE dentro de um outro IF e ELSE, isso
nos permite ter mais opções do que pode acontecer dependendo do que pedimos a tal, as consições aninhadas sercem mais para
condições de valores que não são fixos e que podem acabar variando demais, servindo para todas as situações

Exemplo:

~~~js
let agora = new Date()
let hora = agora.getHours()

console.log(`Horário atual: ${hora}`)

if (hora < 12) {
    console.log('Bom dia!')
} else if (hora <= 18) {
    console.log('Boa tarde!')
} else {
    console.log('Boa noite!')
}
~~~
Exlpicação do código:
aqui temos um simples código em JS puro que pega as horas atuais e compara elas com as pré-definições
que colocamos dentro das condições aninhadas, entregado uma mensagem de boa dia, boa tarde ou boa noite
dependendo do horário atual

### 6.2: Condições Múltiplas

Servem principalmente para situações muito pontuais e bem específicas, algo bem diferente das condições que vimos anteriormente,
essa condição eh representada pelo Switch, case, break e default, assim:

~~~js
switch (expressao) {
    case "teste":
        
        break
    case "teste2":
        
        break
    default:
        
	break
}
~~~
o uso de break se ve OBRIGATÓRIO em todos as cases, caso contrário o comando nunca irá cessar, já o
default serve para dizer oq vai ocorer se nenhuma das cases acima for atendida

Exemplo:

~~~js
var agora = new Date()
var diaSemana = agora.getDay()

switch(diaSemana) {
    case 0:
        console.log('Domingo')
        break
    case 1:
        console.log('Segunda')
        break
    case 2:
        console.log('Terça')
        break
    case 3:
        console.log('Quarta')
        break
    case 4:
        console.log('Quinta')
        break
    case 5:
        console.log('Sexta')
        break
    case 6:
        console.log('Sabado')
        break
    default:
        console.log('Dia inválido')
        break
}
~~~
Explicação do código:
aqui temos um código que pega o dia atual da semana e converte em str usando as condições switch, case, break e 
default


-----------------------------------------------------------------


## 7: Repetições

As repetições no JS funcionam de uma maneira bem parecida como qualquer outra, Java, Python e etc.
Existem duas maneiras básicas de executarmos essas repetições no JS, sendo o primeira onde ela vai fazer primeiro
o teste lógico e sendo ele verdadeiro ela vai executar o bloco, assim:
testa, executa e faz looping
para usarmos essa primira opção nós usamos somente o while(), assim:

~~~js
var n = 1

while (n <= 10) {
    console.log(`Olá, mundo! Mensagem número: ${n}` )
    n++
}
~~~
a segunda faz justamente o contrário disso tudo, onde o bloco será executado antes mesmo de fazer o 
teste lógico, assim:
executa, testa e faz o looping
já para usarmos a segunda forma de repetição, fazemos assim:
~~~js
var n = 1

do {
    console.log(`Olá, mundo! Mensagem número: ${n}`)
    n++
} while (n <= 10)
~~~

### 7.1: Repetições com estrutura de controle

Estes tipos de repetições normalmente são feitas 3 coisas dentro do parametros, sendo eles:
inicialização, teste lógico e o incremento
ele vai começar com a inicialização e o teste lógico, caso o teste lógico seja verdadeiro ele vai executar
um bloco de comandos, após isso ele vai voltar para fazer o looping e nessa volta ele faz o incremento, repetindo
o processo até o teste lógico ficar falso e o looping se encerrar, sua carcaça eh assim:

~~~js
for (inicio ; teste ; incremento) {
    bloco de comandos aqui
}

Exemplo:

for (var n=1; n<=10; n++) {
    console.log(`Olá, mundo! Mensagem número ${n}`)
}
~~~
explicação do código:
aqui nós criamos um código que escreve olá mundo 10 vezes usando a estrutura for


-----------------------------------------------------------------


## 8: Variáveis Compostas

As variáveis compostas são exatamento oq o nome diz, elas diferente das simples elas armazenam mais de um
valor, ou seja, podemos adicionar vários valores dentro de uma única variável, exemplo:
vaga a = [carro1, carro2, carro3]
ela lembra bastante as listas e dicionários do Python, não se esqueça que essa 'vaga' eh um exemplo, não um comando real.

o primeiro valor sempre vai começar com 0, ou seja, uma vaga de 10 espaços sempre vai começar de 0 até 9 e não de 1 a 10.

-a variável 'a' recebe o nome de array(vetor)
-dentro da array(vetor) temos os elemntos que ocupam o espaço da memória, o 
valor colocado dentro dele e o índice 
-temos os índices(keys) que são os números dos elementos dentro da array(sempre começando do 0)
-o conteúdo de cada elemento tem o seu valor

básicamente, uma array(vetor) eh uma várivael que tem vários elementos, cada elemento tem 
o seu valor e sua chave de identificação(key), assim:
let num = [5, 8, 4]
aqui temos um vetor de três elementos(0, 1 e 2) e que tem os valores 5, 8 e 4

nós podemos adicionar coisas dentro das listas mesmo após já termos dado seus valores, para isso
nós fazemos assim:
let num = [5, 8, 4]
num[3] = 6
aqui nós adicionamos o valor 6 no índice 3 deixando explicito que nós queriamos que esse valor
esteja inserido no índice 3, agora quando não queremos deixar isso explicito mós podemos fazer assim:
let num = [5, 8, 4]
num[3] = 6
num.push(7)
assim, nosso o quarto índice terá o número 7 como seu elemento

o metado sort() vai colocar todos os elementos em ordem crescente

quando nós queremos ver no terminal a nossa variável composta ela normalmente vem com os colchetes, para vermos
nossa variável composta com a formatação de nossa preferencia nós podemos usar o while ou o for, assim:

let num = [5, 8, 4]
num[3] = 6
num.push(7)
num.sort()

~~~js
console.log(`O vetor tem ${num.length} posições.`)

for (let pos = 0; pos<num.length; pos++) {
    console.log(`A posicão ${pos} tem o valor ${num[pos]}.`)
}
~~~
-a variável "pos" vai receber o número 0 já que o índice sempre começa no número 0
-o teste lógico faz com que enquanto o número de elementos for maior que o número de índices
ocorra o incremento a seguir
-o incremento aumenta o número do pos, quando a variável pos foi maior que o número de elementos
nosso looping fecha seu ciclo
assim nós conseguimos que várias linhas de código se transformassem em poucas linhas, isso
além de ser uma boa prática deixa o código mais limpo

### 8.1: for( in )

Podemos usar o comando for( in ) para facilitar o código, esse metado eh otimizado para fazermos a leitura
de variáveis compostas e objetos na programação, exemplo:

~~~js
let num = [5, 8, 4]
num[3] = 6
num.push(7)
num.sort()

console.log(`O vetor tem ${num.length} posições.`)

for(let pos in num) {
    console.log(num[pos])
}
~~~
-let pos serve para atribuirmos uma variável de uma maneira mais simplificada, pode ser let ou var
-o num eh nossa variável composta, eh ali onde nós devemos colocar qual a variável composta que
queremos fazer a leitura
o código pode ser lido assim:
para cada posição(for) em(in) num eu vou mostrar(console.log) o num(variável composta) pos(contagem)

Nós podemos buscar valores dentro dos nossos vetores usando o .indexOf(), exemplo:

~~~js
let num = [5, 8, 2, 9, 3]
num.push(1)
num.sort()
console.log(num)

let pos = num.indexOf(8)
console.log(`O valor 8 esta na posição ${pos}`)
~~~
assim nós perguntamos ao JS se existe o valor 8 dentro da nossa variável composta, se ele existir o JS vai
retornar o índice que ele se localiza


-----------------------------------------------------------------


## 9: Funções

Vamos supor que a sua mãe toda semana pede para vc comprar leite, ela te da um dinheiro e vc vai no mercado comprar leite, podemos
chamr isso de função, para a sua mãe não importa qual mercado vc foi, como vc foi e etc, oq importa eh q o leite precisa estar na
mão dela como ela mandou.
quando a sua mãe te chama nós podemos chamar isso de chamada, ela pode ser automática ou não.
vc não pode comprar o leite sem o dinheiro, vc precisa dele, nós chamamos isso de parâmetro, o leite também
faz parte deste parâmetro
toda a função deve ter uma ação, nesse caso seria o processo de ir na mercearia, pagar pelo leite e etc
quando vc entrega o leite para a sua mãe nós chamamos isso de retorno
lembre-se que nem toda função precisa ter parâmetros, retornos e etc

as ações são executadas assim que chamadas ou em decorrência de algum evento
uma função pode receber parâmetros e retornar um resultado, exemplo:

~~~js
function parimp(n) {
    if (n % 2 == 0) {
        return 'par'
    } else {
        return 'impar'
    }
}
console.log(parimp(11))

temos aqui uma função que diz se o número eh impar ou par, vamos explicar por partes
~~~

~~~js
let res = parimp(11)
essa parte aqui eh a nossa chamada, isso daqui que da o gatilho da nossa ação
~~~

~~~js
function parimp(n) {}
o "n" dentro dos parentêses eh o nosso parâmetro
~~~

~~~js
if (n % 2 == 0) {
        return 'par'
    } else {
        return 'impar'
    }
tudo oq está dentro das chaves da nossa função nós chamamos de ação
~~~

~~~js
return 'par'
return 'impar'
estes são os chamados retornos, onde nesse caso somente o segundo retorno foi retornado


console.log(parimp(11))
aqui ele retorna nosso resultado, se nosso número eh impar ou par, nesse caso, ele eh ímpar já
que o número 11 dentro do "parimp" eh o nosso "n"
~~~

Nós podemos também usar dois parâmetros dentro de uma única function, usando a vírgula para separar
os mesmos, exemplo:

~~~js
function soma(n1, n2) {
    return Number(n1) + Number(n2)
}
console.log(soma(5, 6))
~~~

~~~js
function soma(n1, n2) {}
essa linha eh onde nós definimos as váriaveis, onde o n1 vai receber um número que vamos declarar mais pra 
frente e com o n2 aconteçe o mesmo
~~~

~~~js
return Number(n1) + Number(n2)
essa linha eh responsavel por somar as duas váriaveis que criamos como parâmetros dentro da nossa function
~~~

~~~js
console.log(soma(5, 6))
isso daqui vai nos escrever na tela a soma dos números, além disso ele também atribui as vriveis onde estavam
o n1 e o n2, sendo o "n1 = 5" e o "n2 = 6" 
~~~

Existem casos onde pode ser que um parâmetro não seja inserido dentro dos parâmetros da nossa function, usando o exemplo
acima, caso o n2 esteja vazio o JS iria entender essa variável como undefined e retornando a mensagem NaN.
para impedir que isso aconteça nós devemos definir parâmetros opcionais que só vão ser usados caso eles não sejam
declarados pelo usuário, para defini-los podemos fazer assim:

~~~js
function soma(n1=0, n2=0) {
    return Number(n1) + Number(n2)
}
console.log(soma(5))
assim deste jeito caso o n1 ou o n2 não sejam passados pelo usuário eles terão o valor de 0
~~~

Podemos definir as funções em váriaveis, ou seja, uma variável vai receber uma function, assim:

~~~js
let m = function(x) {
    return x * 2
}
console.log(m(5))
assim, usando o m para armazenar uma function nós damos o parâmetro de "x", que foi o número 5 e calculamos
o dobre dele, oq nos retornou 10
~~~

Podemos fazer uma função que calcula fatoriais, assim:

~~~js
function fatorial(num) {
    let fat = 1
    for(let c = num; c > 1; c--){
        fat *= c
    }
    return fat
}
console.log(fatorial(5))
~~~

indo por partes temos assim:

~~~js
function fatorial(num) {}
aqui nós criamos a função e demos seu nome, o seu parâmetro eh o "num"
~~~

~~~js
let fat = 1
    for(let c = num; c > 1; c--){
        fat *= c
    }
-criamos uma váriavel que recebe um contador, sendo ele o número 1, ela eh responsável por
parar o nosso for quando o número escolhido chegar no fatorial máximo(sendo ele o número 1)

-a váriavel c eh um contador que vai começar no número escolhido pelo usuário, ele que vai ser responsável
por permitir que o loop aconteça até chegar no 1

-"c--" significa que a cada volta no loop o c, que eh nosso contador, ele perde um a menos, isso vai se
repetir até que ele chegue no limite, sendo o número 1

-"fat *= c" eh a conta em si, ele faz a conta toda de multiplicação beseado no atual número do contador
~~~


-----------------------------------------------------------------


## 10: Objetos

O JS eh uma linguagem de programação orientada a objetos, como o Java por exemplo, de uma maneira parecida as variáveis
compostas nós podemos criar objetos com índices própios, ou seja, nós decidomos os nomes do índices ao invés dele serem
separados somente por números crescentes, assim:

~~~js
let pessoa = {nome:'josé', sexo:'M', idade:22, envelhecer(i){}}
~~~

os objetos podem guardar funções para que possam trabalhar de forma conjunta a outras, assim:

~~~js
let pessoa = {nome:'igor', 
    Idade:'18', 
    sexo:'M',
    peso:60,
    engordar(p=0) {
        console.log(`${this.nome} esta crescendo`)
        this.peso += p 
    }}
pessoa.engordar(2)
console.log(`${pessoa.nome} tem ${pessoa.peso}kg`)

Assim nós criamos um código que tem um objeto chamado pessoa onde ela recebe os índices:
nome;
idade;
sexo;
peso.
e uma função que tem seu objetivo modificar um item dentro do nosso objeto sempre que essa função for chamada e
seu parâmetro "p" for modificado de maneira externa, mostramos que essa função foi chamada com o console.log que
eh executado sempre junto da função
~~~


-----------------------------------------------------------------


## 11:  


-----------------------------------------------------------------








-----------------------------------------------------------------





-----------------------------------------------------------------










-----------------------------------------------------------------













-----------------------------------------------------------------













-----------------------------------------------------------------













-----------------------------------------------------------------

Dentro do JS podemos escrever coisas diretamente em nosso site, geralmente para mostrar resultados imediatos
dependendo de come se usa, para isso devemos usar o comando .innerHTML  e depois usado o = apresentar o
valor que o mesmo vai escrever para nós

Criar uma variável com let eh melhor do que var, pois uma variável "var" tem o escopo global e pode ser acessada de qualquer lugar, ou seja:
let = tem o escopo local, só pode ser usado no bloco de notas presente
var = recebe o escopo global, pode ser acessado de qualquer lugar

-----------------------------------------------------------------