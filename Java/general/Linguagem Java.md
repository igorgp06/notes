## 1: HotSpot e JIT

O HotSpot/JVM e o são como se fossem irmão, eles são básicamente dominíos, eles foream criados pela Oracle, um exemplo muito bom do
hotspot eh a "GraalVM", muitas empresas famosas usam ela, a própria Oracle usa ela

Já o "JIT"(Just-in-Time) eke otimiza a execução do HotSpot, ele compila o bytecode, isso faz com que o código seja otimizado para o ambiente
que ele está sendo executado, melhorando a performace e o desempenho do código

O Java roda em todo lugar gracas a sua funcionalizade, onde ele gera bytecodes em linguagem de máquinas, ai que entra as JVM e o JIT, seguindo
esse exemplo:

Código Java -> Compilador -> Bytecode -> (dentro da JVM) Class Loader -> Bytecode Verifier -> Interpretador -> JIT -> (fora da JVM) Máquina

o JIT atua nessa área, ele fica dentro da JVM ao lado do interpretador, digamos que temso um código enorme cheio de repetições, para
o interpretador mandar isso várias vezes, gerando várias linhas de códigos binários, nesse momento o JIT entra, ele faz com que o
interpretador corte esse trabalho desnecessário e sem precisar gerar inumeras linhas de repetições, ele diz se o código deve se repetir, se
ele deve ser ignorado, excluido e etc 


-----------------------------------------------------------------


## 2: JVM, JRE e JDK

Se você tem uma JRE, ele obrigatoriamente inclui uma JVM, o JDK instala todos os outros (JRE e a JVM), ele também incluí 
várias bibliotecas úteis para nos ajudar nos códigos, veja o signifcado de cada um desses termos:
JDK = Java Development Kit
JRE = Java Runtime Enviroment
JVM = Máquina Virtual do Java


-----------------------------------------------------------------


## 3: Uso do -version e suas variações

Para nós vermos qual a versão atual do Java, nós devemos abrir o GIT BASH e escrever "java -version"

Para começarmos com uma vm, usamos o "javac -version", assim nós vemos o pacote de versão do JDK, sendo ele o responsável por compilar
os códios em Java

Para verificarmos nossas variaveis de ambiente usamos

Após criamos um código em Java usando o "nano", ele gera um bytecode (se o código estiver semanticamente correto), depois, após o código ter sido
compilado, nós devemos mandar o bytecode para a nossa máquina e assim ele será executado atraves do terminal BASH

Veja um exemplo de como dar um HelloWord em Java:

~~~Java
public class HelloWord {
    public static void main(String[] args) {
        System.out.println("Hello World!");
        }   
}
~~~


-----------------------------------------------------------------


## 4: intelliJ e comentários

Uma das melhores IDLES para programar em Java eh o intelliJ, ele vem vom várias funções exclusivas e que já facilitam nossas vidas
quando codamos em Java, igual o PYCharm para o Python

Para comentarmos em Java ele eh igual ao JavaScript, para comentarmos em uma única linha usamos o "//" e para multiplas linhas usamos o
/* no começo da linha e */ no final da linha onde acaba o comentário

Os nossos cógigos pricipais sempre estarão dentro de src, as outras pastas normalmente são dependências, como informações de bibliotecas, git,
git ignore e etc

Dentro do intelliJ existe uma funcionalidade chamada de TODO, ela eh como se fosse uma lista de afazeres dentro da nossa IDE, para usarmos
nós devemos usar o comando de comentário "//" e escrever logo após "todo", assim ficará marcado como uma tarefa a ser feita


-----------------------------------------------------------------


## 5: Variável e Constante

De uma maneira muito parecida com o JS, o Java tem variáveis e Constantes, elas significam exatamente oq seu nome quer dizer, uma variável pode
mudar várias vezes com o decorrer do programa, já a constante uma vez declarada não pode ser mais alterada

O Java eh uma linguagem extremamente verbosa e tipada, isso significa que sempre devemos declarar o tipo de dado que uma variável que vai
receber, veja um exemplo:

~~~Java
public class Main {
    public static void main(String[] args) {
        String txt = "Olá, mundo!";
        System.out.println(txt);
    }
}
Declaramos uma variável que recebe uma String com o nome de "txt" e seu valor eh "Olá, mundo!"
\\\\\\\\\\\\\\\\

nós podemos livremente alterar o valor dessa variável ao decorrer do programa desde que seja uma o tipo primitivo
String

Para as constantes basta adicionar o termo "final" antes ou depois de declarar o tipo primitivo do dado que queremos, veja um exemplo abaixo:

////////////////
public class Main {
    public static void main(String[] args) {
        final String txt2 = "Olá, mundo!";
        System.out.println(txt2);
    }
}
~~~

-----------------------------------------------------------------


## 6: Tipos Primitivos

Tipos de dados que envolvem textos e caracteres não naturais:
String = linha de texto

Tipos de dados que envolvem números naturais e decimais:
int = número natural inteiro
double = número natural com casa decimal

Tipos de dados que envolvem operadores lógicos:
boolean = true ou false

Veja os exemplos de cada um dos tipos primitivos no Java:

~~~Java
public class Main {
    public static void main(String[] args) {
        // tipo de texto
        String txt = "Olá, mundo!";
        System.out.println(txt);

        // número inteiro
        int NumInt = 18;
        System.out.println(NumInt);

        // número decimal
        double NumDouble = 3.14;
        System.out.println(NumDouble);

        // tipos boleanos
        boolean BoolTrue = true;
        boolean BoolFalse = false;
        System.out.println(BoolTrue);
        System.out.println(BoolFalse);
    }
}
~~~


-----------------------------------------------------------------


## 7: Estrutura de Condição IF

Abaixo temos os tipos padrões de operadores lógicos, sendo eles os mais padrões que já conhecemos, com o igual, diferente, maior que, 
menor que e assim por diante. Veja eles abaixo:


- == = igual
- >= = maior ou igual
- <= = menor ou igual
- != = diferente de
- ! = negação
- > = maior
- < = menor
- && = e (X tem que ser igual a Y para que o movimento Z aconteça)
- || = algum dos (X ou Y tem que ser igual a algo para que o movimento Z aconteça)

A estrutura de condição IF eh muito parecida com o JS, tem a mesma lógica e seguem preceitos muito parecidos, tanto logicamente tanto
quanto visualmente, veja um exemplo abaixo:

~~~Java
public class Main {
    public static void main(String[] args) {
        int n1 = 10;
        int n2 = 5;

        if (n1 > n2) {
            System.out.println("O número 1 é maior");
        } else {
            System.out.println("O número 2 é maior");
        }
    }
}
Código simples que analisa se o "n1" é maior que o "n2" e retorna uma mensagem para cada uma das situações 
~~~

digamos que o "n1" seja igual ao "n2", neste caso nosso programa não iria rodar já que dentro da nossa estrutura IF essa possibidade não foi
informada, neste caso nós podemos utilizar p "else if {}", básicamente a mesma coisa do JS, veja um exemplo abaixo:

~~~Java
public class Main {
    public static void main(String[] args) {
        int n1 = 10;
        int n2 = 10;

        if (n1 > n2) {
            System.out.println("O número 1 é maior que o número 2");
        } else if (n1 == n2) {
            System.out.println("O número 1 é igual ao número 2");
        } else {
            System.out.println("O número 2 é maior que o número 1");
        }
    }
}
neste código nós verificamos todas as possibilidades que podem acontecer se o número 1 foi maior ou menor que o número 2 ou
se os dois números são iguais
~~~

dessa forma nós conseguimos fazer quanats estruturas aninhadas nós quisermos, podemos colocar quantos "else if" quisermos e não
se esqueca que nós podemos usar livremente somente um IF caso seja necessário


-----------------------------------------------------------------


## 8: Estrutura de Condição SWITCH

A estrutura SWITCH funciona de uma maneija parecida com o JS, extremamente útil para códigos e funções extremamentes
específicas e com valores fechados, procure extender o minino possível estas extruturas. Veja um exemplo abaixo:

~~~Java
public class Main {
    public static void main(String[] args) {
        int n1 = 2;

        switch (n1) {
            case 1:
                System.out.println("Valor 1");
                break;
            case 2:
                System.out.println("Valor 2");
                break;
            case 3:
                System.out.println("Valor 3");
                break;
            default:
                System.out.println("Valor acima do permitido");
                break;
        }
    }
}
um código que verifica o valor de n1 e caso ele seja compativel com algumas das cases ele retorna uma mensagem
~~~

nunca se esqueça que após terminar de declarar oq aquela case vai fazer inserir um break, já que ele eh responsável por barrar o
código para que ele não fique num loop repetindo sem parar

o default serve de uma maneira parecida com o else, ele básicamente diz oq acontece caso nenhuma das cases acima seja atendida, neste caso
ele escreve vê se o valor de n1 foi maior que 3 ele escreve algo no terminal


-----------------------------------------------------------------


## 9: Estrutura de Condição TERNÁRIA

A estrurua de condição Ternária é bem parecida com a estrura de IF e ELSE, quando soó se tem dois caminhos a serem seguidos, sempre que situações
assim aparecerem recomnda-se usar a condição ternária, porém quando eh mais de dois caminhos usamos o IF, IF ELSE e ELSE

o perador ternário eh representado por dois sinais, sendo eles "?" e ":", pense nisso como um if e else, sendo:
? = IF
: = ELSE
os parâmetros são passados antes do "?" que funciona como um IF, e depois passamos oq acontece após o ":" como se ele fosse um ELSE, exemplo:

~~~Java
public class Main {
    public static void main(String[] args) {
        int n1 = 20;

        String res = (n1 <= 17) ? "Menor de idade" : "Maior de idade";
	System.out.println(res)
    }
}
Código que pega o "n1" e o analisa, caso ele seja menor ou igual a 17 o "?"(que tem função a função de um IF) vai entrar em
ação, caso contrário o ":"(que tem função de ELSE) vai ser executado
~~~

as condições ternárias precisam obrigatoriamente estarem armazenadas dentro de uma váriavel ou constante, caso contrário ela não vai funcionar. É
importante lembrar que dependendo do que nós queremos que retorne a nós, precisamos especificar isso na variável/constante que armazena a
condição ternária, neste caso ela armazena uma String e seu retorno deverá ser uma string


-----------------------------------------------------------------


## 10: Manipulação de Strings com valueOf e chartAt

O comando String eh próprio do Java, isso justifica o pq ele se escreve diferente dos outros tipos primitivos. Ele por trazer inumeras
funcionalidades consigo mesmo eh recomendado visitar o site:
https://www.javatpoint.com
já que ele traz inumeras informações úteis dessas Strings

Vejamos algumas funcionalidades das mesmas a seguir

O método "valueOf()" converte qualquer tipo de dado em uma String, seja ele numeros inteiros, decimais e etc

com a conversão de dados para String isso nos permite manipular diversos tipos de dados livremente, usando diversas
fncionalidades, um exemplo de funcionalidade eh o "charAt()", ele serve para nós retornarmos qual o caractere que tem naquele
índice, lembre-se que o índice sempre começa no 0 em ordem crescente. Os retornos que esse método develve sempre será uma String, independente
do que ele esteja apresentando no momento, exemplo:

~~~Java
public class StrManopulation {
    public static void main(String[] args) {
        double n1 = 21.131;
        String ConVar = String.valueOf(n1);
        System.out.println(ConVar.charAt(2));
    }
}
aqui nós temos um código que recebe um double na variável "n1", depois ele eh convertido para uma "String" e armazenada numa
variável, após isso usando o "pritnln" nós passamos a variável ja convertida em uma "String" e usando o método ".charAt()" ele
retorna qual o caractere na terceira posição, neste caso seria o "."
~~~

## 10.1: Manipulação de Strings - startsWith e endsWith

Ainda na manipulação de Strings existem dois métodos dentro do Java, sendo eles:
startsWith() = começa com
endsWith() =  termina com
eles são métados extremamente parecidos, possuindo algumas poucas diferenças, onde no "startsWith()" nós passamos um
préfixo que verifica se na String que estamos manipulando ele tem esse préfixo que passamos, retornando um valor boleano 
que deve estar armazenado dentro de uma váriavel com o tipo primitivo do mesmo (boolean), lembre-se que o Java é CaseSensitive. 
Podemos passar também uma "offset" dentro do "startsWith()" após já termos declarado o métado anterior, ele é responsável por dizer
em qual índice ele deve começar a verificar a String que está sendo manipulada

Exemplo de um "startsWith()" com um "offset":

~~~Java
public class StrManopulation {
    public static void main(String[] args) {
        String str1 = "Olá, mundo";
        boolean start_offset = (str1.startsWith("O", 1));
        System.out.println(start_offset);
    }
}
Aqui temos um código que recebe uma String com o valor de "Olá, mundo", logo após isso nós jogamos para dentro uma variável boleana, o
primeiro termo dentro do "startsWith()" ve qual o(s) caractere(s) que queremos q ele procure, o segundo argumento (que eh o offset) diz
de qual índice ele deve começar
~~~

O "endsWith()" funciona da mesma forma que o "startsWith()", sua única diferença eh que ele ao invés de começar da esquerda para a direita
ele faz a análise da direita para a esquerda, veja um exemplo a seguir:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        String str2 = "Eu amo programar em Java";
        boolean end = str2.endsWith("a");
        System.out.println(end);
    }
}
Fizemos a mesma coisa que antes porém agora usando o métado "endsWith()", criamos uma variável String que recebe o nome de "str2", depois
criamos uma variável boleana que análisa a variável "str2", ela 'pergunta' se o texto detro da variável termina com a letra "a", neste caso
como ela termina o nosso código vai retornar o valor boleano "true"
~~~

## 10.2: Manipulação de Strings - trim, length e strip

O método "length()" funciona de uma maneira identica a várias outras linguagens de programação, isso sigifica que ele lê nossa
String e retorna quantos caracteres tem dentro da String, não se esqueça que como em qualquer linguagem de programação, o "length()" também
lê os espaços pois eles contam como caracteres, isto inclui os espaços antes ou no final da String

Para removermos estes espaços no final das Strings existem algumas formas, sendo elas o método "strip()" ou o método "trim()", os dois
possuem diferentes jeitos de se usar, porém entregam resultados parecidos, veja os exemplos daqui a pouco

Tenha sempre em mente que o método "length()" conta quantos caracteres existem dentro da variável (seja ele ponto, letra, espaço e etc), 
"trim()" e "strip()" removem estes espaços no começo e no final da frase. Fique agora com os exemplos:

Usando o "strip()":

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        String str3 = "Minecraft foi escrito em Java!     ".strip();
        System.out.println(str3.length());
    }
}
Note que após a String variável "str3", existem vários espaços no final da frase, logo após ela existe o método ".strip()", ele eh
o responsável por eliminar estes espaços na frase. O método ".length()" está dentro dos parentêses do "println", ele foi o responsável
por mostrar quantos caracteres existem dentro da variável "str3", sendo que sem o método ".strip()" existiriam 35 caracteres, já com o método
ali existem apenas 30 já que os espaços foram cortados 
~~~

Usando o "trim()":

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        String str4 = "   Minecraft foi escrito em Java!";
        String str_sem_espacos = str4.trim();
        System.out.println(str_sem_espacos.length());
    }
}
Agora os espaços estão no começo da variável "str4", o problema de usar o "trim()" eh que nós precisamos criar uma variável só para ele, isso
faz que com que precisemos escrever mais para algo que pode ser resolvido com um simples ".strip()", lógico que são casos e casos, porém sempre que
possivel tenha preferência pelo método ".strip()"
~~~

## 10.3: Manipulação de Strings - toLowerCase e toUpperCase

São bem tranquilos de compreender, os nomes sãp totalmente sugestivos, muito conhecidos e utilizados no Python também, estamos falando
do método "toLowerCase()" e do "toUpperCase()", veja oq eles fazem:
toLowerCase() = coloca todos os argumentos de uma String na forma minúscula
toUpperCase() = coloca todos os argumentos de uma String na forma maiúscula

Veja um simples exemplo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        String str5 = "Eu amo usar a IDE intelliJ";
        System.out.println(str5.toLowerCase());
        String str6 = "Olá, mundo! Estou totalmente na forma maiúscula!";
        System.out.println(str6.toUpperCase());
    }
}
Um simples código que pega os argumentos de suas respectivas variáveis e as põe 
na forma sugerida, "toLowerCase()" e "toUpperCase()"
~~~

Lembre-se que existem várias formas de usarmos estes métodos, não se limite ao jeitos usados nestes exemplos

10.4: Manipulação de Strings - indexOf e lastIndexOf

O método "indexOf()" retorna o primeiro índice que ele encontrou baseado no que nós passamos como argumento para ele, ou seja, ele vai entregar
a posição de itens específicos conforme foi solicitado para ele, já o "lastIndexOf()" retorna o último índice que lhe foi passado, entregando
qual foi a última posição que o argumento passado apareçeu, veja abaixo:
indexOf() = entrega o índice de onde apareceu pela primeira vez o argumento passado a ele
lastIndexOf() = entrega ao índice do de onde apareceu o pela última vez o argumento passado a ele 

Saiba que o "indexOf()" quando não encontra o argumento passado a ele, seu retorno será de "-1"

Tanto o "indexOf()" quanto o "lastIndexOf()" podem receber uma "fromindex", isso significa que podemos escolher a partir de qual índice ele 
vai começar a fazer sua análise, básicamente uma offset

O método "lastIndexOf()" fuhciona de uma maneira parecida, ele faz o contrário do "indexOf()" porém seguindo a mesma lógica, nele podemos
adicionar um "fromindex" também, a diferença aqui eh que ao invés dele começar no índice zero (sem nenhuma offset) ele vai começar do último
índex dessa variável que contém uma String

entenda que o "fromindex/offset" de cada um segue seu respectivo caminho e direção, ou seja, se o "indexOf()" começa da esquerda para a direita seu
"fromindex/offset" vai seguir esse mesmo camiho e o mesmo vale para o "lastIndexOf()", já que ele começa da direita para a esquerda seu "fromindex/offset"
vai seguir essa mesma lógica

Exemplo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        String str7 = "Banana";
        System.out.println(str7.indexOf("ma", 2));
        String str8 = "Laranja";
        System.out.println(str8.lastIndexOf("a"));
    }
}
Neste exemplo aqui temos duas variáveis com uma String e um texto dentro da mesma, analisando a primeira variável(str7), podemos ver que o
"indexOf()" pede uma coisa que não existe dentro dessa variável, portanto ele tera o retorno "-1", já na segunda variável(str8) vemos que
ele pode o índice de onde foi a última vez que usamos a letra "a", como não passamos nenhum "fromindex/offset" seu valor retornado será igual a "6"
~~~

## 10.5: Manipulação de Strings - replace e substring

O método "replace()" faz exatamente oq seu nome quer dizer, com ele nós podemos substituir ocorrências, se pedirmos para trocarmos todas as
letras "x" pela letra "y" ele vai faze-lô

primeiro passamos os argumentos que queremos subsituir (target) dentro das aspas, após isso separado por uma vírgula nós colocamos o
argumento que será inserido no lugar do que virá a ser substituido (replacement), veja o exemplo abaixo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        String str9 = "Banana";
        System.out.println(str9.replace("a", "e"));
    }
}
neste código temos uma variável String (str9) que recebeu um texto, após isso dentro do "println" nós mandamos o método ".replace()" substituir
todas as letras "a" presentes na variável pela letra "e". Lembre-se que os argumentos passados podem ser qualquer coisa, não se limite a apenas
um único caractere
~~~

Já o método "substring()" nós podemos extrair coisas das Strings com base no seu índice, ou seja, baseado no índice onde uma palavra começa e 
termina, com este método nós podemos extrair ela e assim teremos o retorno da parte que extraímos, exemplo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        String str10 = "Diga olá a todos, Java!";
        System.out.println(str10.substring(0, 16));
    }
}
neste código temos uma variável String (str10), perceba que dentro do "println" temos o método "substring()", ela vai ser a responsável por
extrair oq pedimos com base nos índices, neste caso colocamos os índices "0" e "16", isto significa que ela vai pegar tudo o índice "0" até
o índice "16" e depois escrever no nosso terminal
~~~


-----------------------------------------------------------------


## 11: Arrays Simples

O Conceito de "array" eh simples, são básicamente listas de dados onde podemos armazenar informações de algo especifico e atráves de diferentes
formas podemos acessar seus dados, cada dado dessa array recebe seu índice, funciona de uma maneira bem parecida com oq vimos antes em relação a
manipulação de string, ou seja, igual numa String cada elemento vai receber um índice (começando a partir do zero)

Antes de declararmos uma array, devemos usar os colchetes após declararmos de qual tipo vai ser nossa array, se ela vai ser de números ineiros, Strings
e etc, após isso damos o nome a array e usando as chaves{} colocamos seus argumentos separados por vírgulas 

Nós podemos acessar os objetos de uma array a usando os colchetes[], veja um exemplo abaixo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        int[] array1 = {1, 41, 141, 151, 6};
        System.out.println(array1[1]);
    }
}
aqui temos uma array que recebe diversos números inteiros devido ao tipo primitivo que foi passada a ela, após isso no "println" nós
chamamos a nossa array e dentro dos colchetes[] colocamos o índice que contém o argumento que queremos acessar, neste caso a valor "41" vai ser
retornado no terminal
~~~

Quando nós tentamos acessar um índice que não existe na nossa array o código vai deixar de funcionar, porém existe um jeito de fazermos isso sem
dar erro, para isso nós devemos usar o método "new (tipo primitivo do que var ser adicionado aqui)"[novo argumento aqui], preste atenção, ao usar
esse método nós estamos criando uma array vazia porém que tem capacidade para ser // corrigir essa parte aqui \\ preenchida por até argumentos, 
no caso 4 índices, após isso
podemos escolher qual argumento var ser atribuido a qual índice da array, exemplo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        int[] array2 = new int[4];
        array2[3] = 69;
        System.out.println(array2[3]);
    }
}
análise bem esse código, aqui criamos uma array vazia porém que tem capacidade máxima de até 4 índices para ser preenchida, após isso
chamamos essa array e dentro dos colchetes[] nós informamos qual índice queremos acessar e usando o "=" adicionamos o valor
"69" ao índice 3
~~~

Resumindo, existem duas forma de criar uma array no Java, vc pode declarar a array e já atribui todos os itens que ele vai ter ou você cria
um array dizendo o tamanho máximo dele para posteriormente ir adicionado seus valores

## 11.1: Arrays multidimensionais

As arrays multidimensionais/matrizes são objetos que podem ter várias dimensões, como se fosse um conjunto de arrays, para montar uma array 
multidimensional nós devemos declarar seu tipo primiivo e após isso usar dois colchetes [][] ao invés de um só como nas listas simples, após 
isso podemos declarar seu nome e passar seus dados, assim podemos usar várias chaves dentro dessa array como se fosse um conjunto

Dentro de uma array multidimensional cada conjunto de chave se torna um índice, ou seja, a chave dentro dessa array ganha um indentificador
numeral que começa a partir do zero e o mesmo vale para os valores dentro dessas arrays

Para acessarmos as valores de uma array multidimensional primeiros precisamos passar (dentro dos colchetes[]) o índice de qual array 
dentro do principal queremos acessar e depois logo ao lado abrimos outro colchete[] e escrevemos qual o índice dessa array que nós
queremos ver, veja o exemplo abaixo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        String[][] MultiArray1 = {{"Olá, mundo!", "Thanos"}, {"Java", "Spring Boot"}};
        System.out.println(MultiArray1[0][1]);
    }
}
temos um código que começa declarando uma String e logo após temos dois colchetes[][] sendo isso que informa que essa array eh multidimensional, após
isso passamos seu nome "MultiArray1", note que temos uma chave{} que engloba tudo, essa eh a chave principal e depois ainda dentro dessa chave temos
outras duas chaves, cada chave dessa recebe um índice que começa do zero, dentro de cada uma dessas chaves menores temos duas Strings em cada
que também recebem um índice que começa do zero, após isso dentro do "println" nós chamamos nossa array multidimensional com o colchte[] indicando
que estamos chamando a primeira chave pelo índice 0 e o segundo colchete[] indicando que estamos chamando o índice 1, assim nosso "println" vai
retornar a String "Thanos"
~~~

Lembrese que cada colchete[] quando nós declaremos nossa String que contém os arrays multidimensionais deve conter todos os colchetes[] para dizer
quantas dimensões contém esse array, no caso acima nós temos duas dimensões, se caso precisar de uma terceira dimensão devemos adicionar mais um colchete
após o String, assim:
String[][] MultiArray1 -> duas dimensões
String[][][] MultiArray1 -> três dimensões
nestes casos os índices sempre vão começar do zero sem excessões

Nós podemos fazer com as Arrays Multidimensionais a mesma coisa do que com as Arrays Simples, podemos dizer qual o tamanho vai ter o array sem precisar
adicionar os argumentos de imediato e podendo adicionalos posteriormente, assim:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        int[][] MultiArray2 = new int[2][2];
        MultiArray2[0][0] = 1;
        MultiArray2[0][1] = 2;
        MultiArray2[1][0] = 3;
        System.out.println(MultiArray2[0][0]);
    }
}
repare que nós criamos um Array Multidimensional com duas dimensões devido aos dois colchetes[][], após isso usando o mesmo argumento de um Array Simples
nós, o "new int", foi passado a ele também duas dimensões com os dois colchetes[][], isso significa que ele vai ter duas dimensões e dentro de cada
dimensão ele vai guardar dois argumentos, após isso passamos os argumentos que cada um vai armazenar dentro de si
~~~

podemos ver o código acima da seguinte maneira:
{{1, 2}, {3}}


-----------------------------------------------------------------


## 12: Loops - For

O conceito de Loops existe também no Java, isso significa que coisa X vai acontecer até que alguma condição seja atendida, podemos misurar Loops
com Arrays, fazendo interações com os itens da lista até que todas as condições sejam atendidas, esta condição usa da mesma lógica do JavaScript, ou seja,
começamos criando uma váriavel de controle do loop, após isso fazemos o teste lógico responsavel por verificar se a condição do loop já foi atendida ou não,
e por último criamos o incremento que só será executado se o teste lógico der a devida permissão (que nesse caso seria a mesma coisa que dizer que a 
condição necessároa não foi atendida e o loop deverá se repetir)

O Java exige que dentro da condição dentro do for() seja separada por um ponto e vírgula(;)

exemplo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        int[] SimpArray1 = {1, 2, 3, 4};
        for(int i = 0; i < SimpArray1.length; i++) {
            System.out.println(SimpArray1[i]);
        }
    }
}
aqui nós temos um exemplo de código que faz o aumento de um número até que ele seja atendido como pedido, vejamos:
-temos uma Array com 4 valores dentro dela, sendo eles os números: 1, 2, 3 e 4
-no primeiro parâmetro do for criamos uma variável "i" que recebe o número 0, ele será o nosso contador
-no segundo parâmetro temos nosso teste lógico, ele eh responsavel por validar se o loop deverá continuar acontecendo ou não, neste caso ele
pergunta se o contador "i" é menor que o número de valores que temos dentro da nossa Array
-depois disso temos o incremento, ele só vai acontecer enquando o teste lógico não for atendido neste caso ele vai aumentar o valor do contador
"i" em mais 1 (i + 1)
-o "println" eh o responsável por mostrar o valor de "i", isso vai se repetir 4 vezes, ou seja nosso loop se repetirá 4 vezes até que o valor de
"i" seja igual ao valor de valores dentro da nossa Array
~~~

### 12.1: Loops - Foreach

Funcionando de uma muito parecida do "For", porém ele não necessita que especifique quantas vezes ele precisa se repetir, ele mesmo para por
conta prórpia básicamente, pegando o último exemplo de código do "for", vimos que criamos um contador, um teste lógico e por fim criamos o
incremento do contador, o "Foreach" anula essas necessidades, pois ele exige que criamos somente uma váriavel prórpia, veja o exemplo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        int[] SimpArray2 = {1, 2, 3, 4};
        for(int num : SimpArray2) {
            System.out.println(num);
        }
    }
}
note que os dois códigos cumprem o mesmo propósito, eles tem a mesma saída porém com a escrita diferente, temos nossa Array com seus 4
valores, após isso temos o "for" e dentro deles criamos uma váriavel chamada "num", podemos interpretar o ":" como um "length", ele é o
responsavel por atribuir a Array "SimpArray2" ao método "length" mesmo esse método não estando explicitamente escrito
~~~
  

Devemos ter em mente que os dois tipos de for tem usos diferentes para ocasiões diferentes dependendo da exigência ou situação, básicamente
o primeiro "for" deverá ser preferencialmente usado quando nós sabemos exatamente o valor que quermos validar/varificar e etc, já o "Foreach" eh
para quando nós não sabemos quantos índices/valores e etc nós temos, básicamente o "for" eh mais direto a exatamente oq queremose e quando temos
certezam diferente do "Foreach"

### 12.2: Loops - While

O termo "while" eh bem conhecido no mundo da programação, ele quer dizer "enquanto", isso significa que enquanto a condição X não foi atendida
a função Z vai ser executada até a função X for atendida, exemplo

Diferente do "for" e do "foreach" que tinham seus contadores dentro do seus parâmetros, o "while" precisa ter o contador fora so escopo dele, ou seja,
eh como seu o teste lógico dele ficasse fora de seu escopo e o incremento dentro da sua indentação

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        int[] SimpArray3 = {1, 2, 3, 4};
        int cont = 0;
        while (cont < SimpArray3.length) {
            cont++;
            System.out.println(cont);
        }
    }
}
aqui temos um código bem simples, vejamos os detalhes:
-começamos com uma Array que contém 4 valores
-depois temos uma variável que contém o número 0 sendo ela responsável por fazer parte do teste lógico "while"
-no "while" temos os parâmetros que diz fala: enquanto o "count" for menor que o "length"(tamanho) da Array adicione mais 1 (cont + 1)
no meu "count" até que o count seja maior que o tamanho da minha Array 
~~~

### 12.3: Loops - Do While

Os loops "do While" são muito parecidos com o "while", ele pode ser lido assim: faça(do) enquanto(while), ou seja, ele manda algo acontecer
enquanto o while for true, a função X vai ser executada enquanto o contador Z for menor que o número Y

"while" e "do while" tem uma pequena diferença, o "do while" primeiro executa sua condição (no caso, o "do") e depois faz o teste lógico, básicamente
no "while" o loop só acontece se a condição exigida for atendida e caso ela seja false o loop nunca chegará a acontecer, já o "do while" faz justamente o
contrário, ela primeiro vai executar oq foi passado pra ela pra só depois disso disso o teste lógico ser executado dentro do "while"

Exemplo:

~~~Java
public class StrManipulation {
    public static void main(String[] args) {
        int[] SimpArray4 = {1, 2, 3, 4};
        int num = 0;
        do {
            System.out.println(SimpArray4[num]);
            num++;
        } while (num < SimpArray4.length);
    }
}
temos um código usando o "do while", ele faz a mesma coisa do que o "while" porém com a escrita diferente, indo por partes temos:
-uma Array simples com 4 valores
-um contador que começa do número 0
-o "do" vai imediatamente escrever na tela o valor do "num" em relação a Array e logo em sequencia adiciona mais um número ao contador "num"
-no while acontece o teste lógico, dizendo que enquanto "num" for menor que o tamanho da Array o "do" vai ser executado novamente até
o fim do loop
~~~


-----------------------------------------------------------------


## 13: Programação Orientada a Objetos (POO)

O termo "Programação Orientada a Objetos" tem como seu pricipal objetivo tentar representar ao máximo possível algo que chegue próximo a alguma
representação do mundo real, eh dai de onde vem s silga "POO"

A "Programação Orientada a Objetos" tem 4 pilares, sendo eles:
-Abstração;
-Escapsulamento;
-Herança;
-Polimorfismo.

Vamos seguir a analogia, vamos imaginar um carro, ele tem suas características, nós conseguimos saber elas, como sua cor, potência do motor, marca, modelo,
ano e etc, essas características no mundo da programação são chamadas de "Atributos". Além das características do carro ele também possui funções, como a
função de ligar, acelerar, freiar, trocar de marcha e etc, nós chamamos estas funções de "Métodos"

Ainda dentro da "Programação Orientada a Objetos" eixstem dois termos muito famosos, sendo eles a "classe" e o "objeto"
classe = modelo que vai ser seguindo para que um objeto seja criado
objeto = resultado(s) da classe

vamos imaginar que temos um molde e dentro desse molde nós temos um carro, dentro da "Programação Orientada a Objetos" o molde eh a "classe" e o resultado
desse molde nós temos o "objeto", onde um molde pode criar vários objetos diferentes que podem interagir entre si

### 13.1: Criação de objetos com classe

Note que TODOS os códigos que vimos até agr tinham sua primeira palavra como "public", ele eh o modificador de acesso da classe. Logo após ele
vinha a palavra "class", ele indica que oq está sendo contruido eh uma classe e seguido depois do nome da classe, sempre opte por colocar o nome da classe
com o(s) nome(s) maíusculos e depois abrimos e fechamos o escopo dessa classe

Quando nós criamos uma nova classe dentro do diretório "src" o intelliJ sugere alguns nomes para nós, use-os, eles são muito importantes para a contruções de
várias aplicações diferentes

Na segunda linha dentro do escopo da classe nós devemos passar o modificador de acesso do atributo, ele pode ser público, privado e etc, apos isso nós
devemos passar qual o tipo primitivo(String, int, double e etc) esse modificador vai ser, dá também para passarmos valores padrões para a classe, isso
significa que podemos após darmos o nome da classe usamos o "=" para darmos seu valor "default"

lembre-se que todos os dados inseridos dentro do escopo da classe principal são os atríbutos dela mesma, elas são suas características para cada objeto
construido dentro da nossa aplicação (que nesse nosso exemplo seria o carro)

eh importante que quando nós criamos uma classe, somente oq se relaciona e ela mesma esteja dentro do arquivo, ou seja, quando nós criamos uma
classe com todos seus atríbutos e características somente isso esteja lá dentro, nada mais nem nada a menos, pois o sistema, a lógica, e a estrutura
do código deve estar principalmente dentro do "Main", e a classe separada desse arquivo

Agora dentro do "Main", após já termos construido a classe em um arquivo separado nós podemos começar a criar nossos objetos, dentro do escopo
da "static void" nós começamos chamando nossa classe e passando o nome do objeto (chame e variável para melhor entendimento qm sabe), após isso
usando a palavra reservada "new" nós chamamos novamente a classe com os parentêses no final da classe onde nós podemos passar seus parâmetros

depois de já termos criado o objeto nós podemos começar a chamar o mesmo e usando o "." e passarmos as características desse objeto, lembre-se
que as características são os atríbutos que criamos no arquivo da classe deste objeto que acabamos de criar

Vejamos um exemplo: 

~~~Java 
AQUIVO DA CLASSE

public class Carro {
    public String marca;
    public String modelo;
    public String cor;
    public int ano;
}
temos uma classe pública que recebe o nome de Carro, abrindo as chaves{} e dentro do seu escopo temos as atríbutos/características dessa mesma
classe, observe que o tipo primitivo de cada um dos atríbutos deve sempre estar presente
~~~

~~~Java
ARQUIVO MAIN

public class Main {
    public static void main(String[] args) {
        Carro fusca = new Carro();
        fusca.marca = "VOLKSWAGEN";
        fusca.modelo = "Fusca";
        fusca.cor = "Preto";
        fusca.ano = 1990;
        System.out.println(fusca.cor);
    }
}
veja bem, note que nós chamamos nossa classe "Carro" como se ela fosse um tipo primitivo já que ela virou uma classe do próprio java para essa
nossa aplicação, eh como se nós estivessemos criando uma variável. Após o "=" temos a palavra reservada "new" e chamamos novamente a classe "Carro()", isso
quer dizer que criamos(new) um novo objeto da classe "Carro", também chamado de onstanciar um objeto no mundo da programação. Finalmente depois de tudo
isso nós começamos a passar as características de cada um do atríbutos que criamos lá dentro do arquivo da classe, eh como se a classe 
fosse as instruções do que precisamos para montar um carro e o arquivo "Main" fosse a montadora desse carro. 
Por fim o "println" escreve no terminal qual a característica salva na cor de fusca
~~~

### 13.2: Método construtor de uma classe

Os métodos construtores são as ações (também chamados de funções) que nosso objeto pode fazer, isso significa que dentro de alguma classe nós podemos
fazer com que ela execute ações, como no exemplo da classe "Carro", nós podemos criar uma método para que ele ligue por exemplo

A primeira funcionalidade que estamos vendo são os métodos construtores, os métodos construtores devem estar dentro do arquivo da própria classe, já que
eles ficam dentro dos parentêses no aquivo "Main", observe o exemplo que vimos anteriormente, perceba que nessa linha aqui:
Carro fusca = new Carro();
que foi onde nós criamos o objeto "Carro", olhe como os parentêses estão vazios, isso aconteçe pq não foi passado nenhum método construtor a este objeto

Exeemplo:

~~~Java
ARQUIVO DA CLASSE

public class Carro {
    public String marca;
    public String modelo;
    public String cor;
    public int ano;

    public Carro(String marca, String modelo, String cor, int ano) {
        this.marca = marca;
        this.modelo = modelo;
        this.cor = cor;
        this.ano = ano;
    }
}
olhe como nós criamos um método público com a classe do objeto "Carro", lembre-se que eh muito importante sempre dizermos o tipo primitivo do método
construtor antes mesmo de definir ele, eh como se colocassemos todas as informações do carro dentro de um único método. O nome "this" serve (neste caso) 
para acessarmos os dados dentro da classe, isso signfica que estamos pegando alguma característica da nossa classe e a passando dentro do método
construtor usando o "this."
~~~

~~~ Java
ARQUIVO MAIN

public class Main {
    public static void main(String[] args) {
        Carro gol = new Carro("Gol", "VOLKSWAGEN", "Branco", 2004);
        gol.cor = "Cinza";
        System.out.println(gol.cor);
    }
}
observe que aqui que nós chamamos a classe "Carro" e depois criamos um objeto chamado "gol", dentro do seus parentêses estão todas as suas características,
tudo oq fizemos no código do exemplo "13.1" foi feito em uma única linha dentro do "Main", nós passamos os métodos dentro do arquivo da classe do "Carro" e
no "Main" nós abordamos ele, passando todos eles dentro do método construtor do objeto da classe "Carro". Veja também que esses mesmos métodos podem ser
alterados mesmo depois de declarados, onde nesse caso nós alteramos a cor do objeto "gol" que antes era uma e depois passou a ser outra 
~~~

### 13.3: Métodos (funcionalidades) de uma classe

Os métodos/funcionalidades são as ações de um objeto, oq ele pode fazer, executar e etc. As funcionalidades são construídas de uma maneira muito parecida
com os métodos construtores, a excessão eh que para construirmos a funcionalidade nós não usamos o nome da classe, nós usamos o nome do método em específico
que queremos pra ele e qual vai ser o seu retorno

lembre-se que nós consguimos deixar o atríbutos da classe com alhum valor padrão e o mesmo vale para as funcionalidades, porém, não eh recomendado fazer
isso dentro da classe, normalmente tudo em relação as características devem ser específicados dentro do método construtor e dependendo do situação quando
o objeto vai sempre começar com o mesmo valor nós podemos específicar este estado dentro da classe construtora do arquivo "class", sem precisar específicar o
mesmo dentro do "Main"

Para criamos uma funcionalidade devemos começar dizendo sua visilidade (pública, privada e etc), após isso devemos informar quando o seu retorno, podendo
ser uma "String", "bolean", "int" e assim por diante, porém quando nós não queremos um retorno e queremos que apenas alguma alteração seja feita nós usamos
o método "void", ele quer dizer que nós não vamos ter retorno porém nossa acçao vai ser executada e normalmente alterando algum valor

Exemplo de um código que trabaha com funcionalidades:

~~~Java
ARQUIVO DA CLASSE

public class Carro {
    public String marca;
    public String modelo;
    public String cor;
    public int ano;
    public boolean ligado;
    public int velocidade;

    public Carro(String marca, String modelo, String cor, int ano) {
        this.marca = marca;
        this.modelo = modelo;
        this.cor = cor;
        this.ano = ano;
        this.ligado = false;
        this.velocidade = 0;
    }

    public void ligar() {
        if (this.ligado) {
            return;
        } else {
            this.ligado = true;
        }
    }

    public void desligar() {
        if (!this.ligado) {
            return;
        } else {
            this.velocidade = 0;
            this.ligado = false;
        }
    }

    public void acelerar(String SpeedType) {
        switch (SpeedType) {
            case "forte":
                this.velocidade += 1000;
                break;
            case "fraco":
                this.velocidade += 500;
        }
    }

    public void acelerar() {
        this.velocidade += 750;
    }
}
nessa parte da classe nós criamos duas características a mais para a nossa classe, temos uma boleana que serve como o liga e desliga do carro e a outra
guarda a velocidade do carro (nesse caso, o RPM do motor), após isso na classe construtora as duas características vem com um valor padrão, que vai ser
o carro estar por padrão desligado e isso automaticamente faz a velocidade/RPM ser igual a zero. 
Temos uma funcionalidade chamada de "ligar()", ela básicamente eh a responsável por ligar o carro, o if serve para verificar se o carro já está ligado, 
caso já esteja ela vai retornar, porém caso o carro não esteja ligado o valor de "ligado" vai passar a ser "true". 
Depois disso temos outra funcionalidade que eh a responsável por desligar o carro, fazendo a mesma coisa que a função ligar, porém verificando 
se o carro já está desligado.
Após isso entra a funcionalidade de acelerar o carro, note que ela recebe o "void" pq ela não escreve nenhum valor, ela apenas muda eles por
debaixo dos panos, veja como dentro dos parentêses existe o "(String SpeedType)", ele eh o responsável por ser a ponte entre o arquivo "Main" e o código
do arquivo da classe, ou seja, isso faz com que dentro do arquivo "Main" quando nós chamarmos a funcão "Acelerar()" ela dentro do seus parentêses vai pedir um parâmetro, onde neste caso ele vai ser uma String 
Ai onde entra o método switch, ela é a responsável por fazer a verificação do que foi inserido do que foi inserido no método "acelerar()" e assim retornar o "RPM" do motor baseado no que o usuário escreveu, a última função ali embaixo serve para dizer que mesmo que o usuário não passe nenhum valor o código vai funcionar, quando fazemos isso o nome dessa função deve ser o mesmo da função principal, podemos usar o if para fazer a validação completa desses dados já que nesse caso ele se encaixaria melhor
}
~~~


-----------------------------------------------------------------


## 14: Conceito de Abstração

Abstração nada mais é, dentro do **POO**, é a concretização de objetos do mundo real e tomando o tópico anterior, nós fizemos exatamente isso, nós abstraímos um objeto da vida real e criamos um objeto dentro da programação, ele contém características, funcionalidades, condições de funcionalidades e etc. Isso significa abstração, pegar algo do mundo real e transformá-lo em código


-----------------------------------------------------------------


## 15:  Conceito de Encapsulamento - Getters e Setters

O encapsulamento nada mais é que o resguarde de informações, elas precisam serem guardadas em algum lugar preservado, a necessidade de preservação dessas informações para que elas não sejam alteradas aborda diretamente o conceito de encapsulamento, basicamente eh o trabalho de acesso das informações de uma classe.

No exemplo anterior temos as características do nosso carro, como o ano, modelo e marca, essas são informações inalteráveis, por exemplo, todo carro tem um número único de chassi, esse número não pode ser alterado pois isso viola uma lei, certo? O encapsulamento aborda isso, onde nós temos informações que não podem ser alteradas, elas não podem ficar soltas de qualquer forma e para isso nós devemos tratar estes dados para se prevenir de alterações que podem e não podem acontecer

Um dois jeitos de deixar essas informações encapsuladas eh usando o método "private", ele bloqueia as coisas para o uso único e exclusivo dentro do arquivo da classe que ele mesmo foi criado, por isso existem dois métodos para que criam excessões para que nós consigamos acessar essas informações passando por algum tipo de tratamento, sendo eles:
Getters = usado para acessar um propriedade
Setters = usado para manipular uma propriedade
lembre-se, eles não devem ser usados para coisas fúteis. Ainda usando o exemplo do carro que nós temos a marca, modelo, cor, ano e as suas funções, certo? Nós não podemos mudar a marca de um carro porém podemos acessar ela, nós podemos visualizar qual a sua marca, já isso não vale para a cor do carro, oq nos impede de pintar o carro de outra cor? Por isso nós temos esses dois métodos

O próprio intelliJ quando nós temos uma classe privada permite criar automaticamente um "getter", "setter" ou os dois ao mesmo tempo, dentro do Java todos os modelos "getter" sempre vão começar com a palavra "get", exemplo do "getter":

~~~Java
public String getMarca() {  
    return this.marca;  
}
usando o mesmo exemplo do código do carro nós privamos nossa característica "marca" e como a marca de um carro não pode ser alterada nós usamos o "getter" para fazer com que essa característica só possa ser visualizada e não alterada
~~~

porém a história muda quando falamos do "setter", pois como vimos anteriormente ele permite que a característica seja alterada (lembre-se, não eh pq ela pode ser alterada que necessariamente signifique ela possa ser vista), vejamos o exemplo do "setter":

~~~Java
public void setCor(String cor) {  
    this.cor = cor;  
}
assim desse jeito nós informamos que a característica pode ser alterada, o método "setter" usa o "set" para dizer que a característica pode ser alterada mesmo ela sendo privada
~~~

porém e quando queremos que uma característica possa ser alterada e visualizada? Não faz sentido alterarmos a cor do carro porém não conseguirmos vela, certo? Agora veja o exemplo de como o "getter" e o "setter" trabalham juntos:

~~~Java
public String getCor() {  
    return cor;  
}  
  
public void setCor(String cor) {  
    this.cor = cor;  
}
assim mesmo, para dizermos que uma característica pode ser alterada e visualizada nós usamos os dois blocos de código que faz com que ela seja uma "getter" ou uma "setter", assim desse jeito ela pode ser visualizada e alterada
~~~

Agora vejamos um exemplo mais complexo ainda com o objeto Carro:

~~~Java
ARQUIVO DA CLASSE

public class Carro {  
    private String marca;  
    private String modelo;  
    private String cor;  
    private int ano;  
    private boolean ligado;  
    private int velocidade;  
  
    public Carro(String marca, String modelo, String cor, int ano) {  
        this.marca = marca;  
        this.modelo = modelo;  
        this.cor = cor;  
        this.ano = ano;  
        this.ligado = false;  
        this.velocidade = 0;  
    }  
  
    public void ligar() {  
        if (this.ligado) {  
            return;  
        } else {  
            this.ligado = true;  
        }  
    }  
  
    public void desligar() {  
        if (!this.ligado) {  
            return;  
        } else {  
            this.velocidade = 0;  
            this.ligado = false;  
        }  
    }  
  
    public void acelerar(String SpeedType) {  
        switch (SpeedType) {  
            case "forte":  
                this.velocidade += 1000;  
                break;  
            case "fraco":  
                this.velocidade += 500;  
        }  
    }  
  
    public void acelerar() {  
        this.velocidade += 750;  
    }  
  
    public String getMarca() {  
        return marca;  
    }  
  
    public String getModelo() {  
        return modelo;  
    }  
  
    public String getCor() {  
        return cor;  
    }  
  
    public void setCor(String cor) {  
        this.cor = cor;  
    }  
  
    public int getAno() {  
        return ano;  
    }  
  
    public boolean getLigado() {  
        return ligado;  
    }  
  
    public int getVelocidade() {  
        return velocidade;  
    }  
}
veja como o arquivo da classe cresceu, perceba que todas as características dele estão marcada como privadas, isso quer dizer que estamos controlando as características do nosso objeto.
Nas últimas linhas do código nós fizemos com que todas as características (com excessão da "cor") fossem dados que só possam ser visualizados, todos eles são imutaveis, porém a a característica "cor" recebeu um "getColor()" e um "setCor()" e isso significa que além de poder ser olhada a característica também pode ser alterada dentro de um "void" já que nós queremos apenas que ela seja alterada sem necessariamente retornar algum valor
~~~

~~~Java
ARQUIVO MAIN

public class Main {  
    public static void main(String[] args) {  
        Carro gol = new Carro("Gol", "VOLKSWAGEN", "Branco", 2004);  
        gol.ligar();  
        gol.acelerar("forte");  
        gol.acelerar("fraco");  
        gol.acelerar("");  
        gol.setCor("Vermelha");  
  
        System.out.println("O carro está ligado? " + gol.getLigado());  
        System.out.println("O RPM do carro é de: " + gol.getVelocidade());  
        System.out.println("A cor do carro agora é: " + gol.getCor());  
    }  
}
como nós alteramos a visilidade das características do nosso objeto lá no arquivo da classe, isso significa que ao chamarmos por ele dependendo do que queremos fazer com a característica.
Tendo em mente que apenas a característica "cor" pode ser alterada eh importante percebermos como isso foi executado, veja que o jeito de chamar as funcionalidades e passar seus parametros não foi alterada.
Como a cor recebe um "getter" e o "setter" ela pode ser alterada e acontece exatamente isso no código, onde o método "setCor("")" faz esse papel de mudar a mesma.
Após isso temos os métodos "getLigado()" e "getVelocidade()", eles são os responsaveis por apenas mostrar se o carro está ligado e quantos RPM está fazendo atualmente, isso aconteçe pq os dois receberam o método "getter" que permite q eles sejam visualizados e não alterados
~~~

Quando nós queremos um método controlado somente dentro da classe e que não pode ser visualizado em outros lugares, basta que seja adicionado a ele somente o método "setter", isso faz com que ele possa ser alterado porém não possa ser acessado fora do arquivo da classe e só possa ser alterado dentro dela, exemplo:

~~~Java
public class Carro {  
    private String marca;  
    private String modelo;  
    private String cor;  
    private int ano;  
    private int idade;  
    private boolean ligado;  
    private int velocidade;  
  
    public Carro(String marca, String modelo, String cor, int ano) {  
        this.marca = marca;  
        this.modelo = modelo;  
        this.cor = cor;  
        this.ano = ano;  
        this.setIdade();  
        this.ligado = false;  
        this.velocidade = 0;  
    }  
  
    public void ligar() {  
        if (this.ligado) {  
            return;  
        } else {  
            this.ligado = true;  
        }  
    }  
  
    public void desligar() {  
        if (!this.ligado) {  
            return;  
        } else {  
            this.velocidade = 0;  
            this.ligado = false;  
        }  
    }  
  
    public void acelerar(String SpeedType) {  
        switch (SpeedType) {  
            case "forte":  
                this.velocidade += 1000;  
                break;  
            case "fraco":  
                this.velocidade += 500;  
        }  
    }  
  
    public void acelerar() {  
        this.velocidade += 750;  
    }  
  
    public String getMarca() {  
        return marca;  
    }  
  
    public String getModelo() {  
        return modelo;  
    }  
  
    public String getCor() {  
        return cor;  
    }  
  
    public void setCor(String cor) {  
        this.cor = cor;  
    }  
  
    public int getAno() {  
        return ano;  
    }  
  
    private void setIdade() {  
        this.idade = 2024 - this.ano;  
    }  
  
    public int getIdade() {  
        return idade;  
    }  
  
    public boolean getLigado() {  
        return ligado;  
    }  
  
    public int getVelocidade() {  
        return velocidade;  
    }  
}
foram adicionados uma característica da classe, um novo método construtor, um "setter" e um "getter" para ver o resultado do "setter". Vamos indo passo a passo para enteneder tudo.
-a característica da classe adicionada foi:
private int idade;
isso quer dizer que agora nossa classe do carro passa a dar uma nova característica ao nosso objeto "Carro".

-nova parte do método construtor:
this.setIdade();
este método faz com que seja adicionado de vez a característica ao ao objeto "Carro", básicamente isso eh a atribuição da característica que criamos para o objeto "Carro".

-calculo da idade do carro com o ano atual:
    private void setIdade() {  
        this.idade = 2024 - this.ano;  
    }
isso básicamente eh um calculo que ocorre dentro do arquivo da própria classe, como ninguem precisa saber e nem visualizar como esse cálculo eh feito nós o deixamos privado e como esse métotodo não vai ser chamado fora do arquivo classe nós podemos passar o "void" para ele.

-chamando o resultado da conta do ano de fabricação com o ano atual:
public int getIdade() {  
    return idade;  
}
anteriormente criamos um bloco privado que calcilava a idade do carro com o ano atual e o privamos para que ele possa ser apenas alterado, esse "getter" faz com que nós pegamos o resultado dessa conta e o deixamos público para que posso ser visualizado em qualquer lugar, eh como se criassemos uma variável privada que faz o backend da conta e uma outra que faz o frontend em apresentar para nós esse resultado
~~~ 


-----------------------------------------------------------------


## 16:  Conceito de Herança

O conceito de herança eh quando uma classe herda características e comportamentos de uma outra classe, estas classes que passam a herança a outras classes são conhecidas por diferentes nome,  "super classes", "classe pai" e "classe mãe" são alguns dos nomes mais conhecidos e usados, pois elas são, hierarquicamente falando, superiores a outras classes normais, basicamente quando uma classe menor herda características e comportamentos de uma outra classe isso eh chamado de herança.

Para fazermos uma classe herdar as características e os comportamentos de uma super classe nós usamos a palavra reservada "extends", ela vai logo na primeira linha quando nós definimos a classe. Dentro dos parênteses do objeto criado devemos passar os métodos que eles vão possuir e herdar, e após isso passamos a palavra reservado "super()" para que essas informações coletadas sejam redirecionadas e tratadas na super classe.

tenhamos em mente que quando nós criamos uma super classe e queremos que as outras classes filho herdem as características e os comportamentos da super classe eh pq não queremos repetir coisas padrões, digamos que você está criando um sistema para uma escola que registra alunos, professores, serventes e etc, todos eles são pessoas, todos eles tem um CPF certo? Agora um aluno não recebo o salário de um professor, um servente não tem notas de uma prova que ele nem fez certo? As super classes eh como se fosse uma central para as informações que todos eles possuem, como o nome e CPF nesse exemplo, e as classes filho recebem suas próprias características e funcionalidades exclusivas, vejamos os exemplos:

~~~Java
ARQUIVO DA SUPER CLASSE

public class Pessoa {  
    private String nome;  
    private String cpf;  
  
    public Pessoa(String nome, String cpf) {  
        this.nome = nome;  
        this.cpf = cpf;  
    }  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public String getCpf() {  
        return cpf;  
    }  
}
aqui nós temos a nossa super classe, note que ela contém as características base de uma
pessoa, como nome e CPF, aqui nós também usamos um "getter" e o "setter" para o nome da pessoa, para que ele possa ser visualizado e editado, já para o CPF nós usamos somente o "getter" para que ele possa apenas ser visualizado.
~~~

~~~Java
ARQUIVO CLASSE FILHO, CHAMADO DE "ALUNO"

public class Aluno extends Pessoa {  
    public Aluno(String nome, String cpf) {  
        super(nome, cpf);  
    }  
}
aqui a história eh um pouco diferente, como aqui se trata de uma classe filho podemos notar o termo "extends", isso quer dizer que ela eh uma extansão da super classe que recebe suas características e funcionalidades.
Ceclaramos também o nome do objeto e quais os métodos que ele vai herdar/receber e depois usando a palavra reservada "super", nós informamos que estes argumentos recebidos devem ser tratados dentro da super classe.

Podemos visualizar isso assim:
public class Aluno extends Pessoa
essa linha eh reponsável por dizer que a classe "Aluno" eh filho da super classe "Pessoa"

public Aluno(String nome, String cpf) {  
Essa linha eh responsável por dizer quais as características o objeto "Aluno" tem, lembre-se que nesse caso os argumentos passados podem ser os da super classe e mais e os
atríbutos da classe filho, eles não precisam ser exclusivamente da classe super

super(nome, cpf); 
e essa última linha eh quem vai dizer para onde vai as estes dados, no arquivo da super classe nós tratamos estes dados lá por eles serem características comuns, porém caso nós tenhamos outras características dentro da classe filho nós poderiamos tratar elas dentro do método construtor da mesma, já que o "super()" serve para dizer para onde estes dois métodos vão
~~~

~~~Java
ARQUIVO CLASSE FILHO, CHAMADO DE PROFESSOR

public class Professor extends Pessoa{  
    private int salario;  
    public Professor(String nome, String cpf, int salario){  
        super(nome, cpf);  
        this.salario = salario;  
    }  
  
    public int getSalario(){  
        return salario;  
    }  
  
    public void setSalario(int salario){  
        this.salario = salario;  
    }  
}
temos aqui o código de uma classe que também herda as características e funcionalidades da super classe "Pessoa", porém essa classe tem uma característica que eh só dela, pertencendo somente a ela em que ela não herda de ninguém e nenhuma outra super classe trata as informações que ela exige (nesse caso, o sálario do professor). Essa característica fica dentro de seus parámetros como qualuer outra, ela pode seralterada e visualizada com o "getter" e o "setter" respectivamente
~~~

~~~Java
ARQUIVO MAIN

public class Main {  
    public static void main(String[] args) {  
  
        Aluno igor = new Aluno("Igor", "123456789-10");  
        Professor flavio = new Professor("Flávio", "987654321-01", 30000);  
    }  
}
e por fim temos o arquivo "Main" e como sempre ele eh o responsável por passar as informações que as classes exigem de seus objetos, perceba que o aluno recebe somente o "nome" e "CPF" enquanto o professor recebo o "nome", "CPF" e o "sálario" sendo o salário um método construtor da classe "Professor"
~~~


---


## 17: Classe Abstrata

Vamos trabalhar novamente com e exemplo da escola, digamos que nós estejamos criando um software para uma escola, como nós temos a super classe "Pessoa()" nós podemos instanciar novos objetos seguindo as regras dessa classe, certo? Porém isso eh muito genérico e não pode acontecer pois o certo eh não poder instanciar novos objetos usando a super classe. Existem várias pessoas trabalhando dentro dessa escola, pode ser qualquer um, por isso nós temos as classes filho que servem para atender as características de cada uma dessas pessoas como falamos no tópico anterior e eh ai onde entra a classe abstrata, elas são classes literalmente abstratas, elas existem para que objetos não possam ser instanciados pois isso eh a concretização de um objeto a partir de uma classe, fugindo totalmente da ideia de abstração. Uma classe abstrata não pode criar novos objetos com o "new", ela só pode ser herdade por outras classes de concretização, entenda isso:
classe abstrata = serve apenas para ditar características, funcionalidades e regras para as classes concretas
classe concreta = serve para a construção de novos objetos

para declararmos uma classe abstrata, basta, antes de declararmos o nome da classe na primeira linha código usarmos a palavra reservada "abstract", assim:

~~~Java
ARQUIVO DA SUPER CLASSE AGR ABSTRATA

public abstract class Classe_Abstrata {  
    
}
deste jeito nós agora nós temos uma classe abstrata que não pode criar objetos a partir dela, agora ela só pode regrar as classes filho(concretizantes) para que elas possam criar os objetos 
~~~

Uma classe abstrata pode conter métodos que podem serem herdados e também podemos ter métodos abstratos, eles são métodos que não são implementados na classe abstrata, quem implementa estes métodos são as classes que herdam essa classe abstrata e para que um método seja abstrato ele precisa obrigatoriamente estar dentro de uma outras classe abstrata. Para dizermos que um método eh abstrato nós também usamos o termo "abstract" antes de dizermos o tipo primitivo da função(int, void, double e etc), o bloco da função também não pode estar dentro de seu escopo, ele neste momento que a criamos basicamente não existe, assim: 

~~~Java
public abstract class Classe_Abstrata {   
    private int método_construtor_usado_para_dar_funcionalidade_a_função_abaixo;  
  
    public abstract void Point_Counter(int minutos);  
}
perfeito, agora nós temos um método abstrato dentro de uma super classe também abstrata, o bloco/funcionalidades do método abstrato devem ser passadas dentro da classe que vai herdar esse método, podendo variar dependendo das necessidades de uso da mesma
~~~

Para que uma funcionalidade abstrata seja herdada(pelo menos nesse caso em qual estamos trabalhando) nós devemos passar uma regra que sobrepõe uma outra para aquela funcionalidade específica, onde no nosso caso que veremos em seguida nós tivemos que usar ela

Vejamos um exemplo de código usando uma classe e uma funcionalidade específica com resultados diferentes para cada classe filho construtora:

~~~Java
ARQUIVO DA SUPER CLASSE ABSTRATA

public abstract class Pessoa {  
    private String nome;  
    private String cpf;  
    private int points;  
  
    public Pessoa(String nome, String cpf) {  
        this.nome = nome;  
        this.cpf = cpf;  
        this.points = 0;  
    }  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public String getCpf() {  
        return cpf;  
    }  
  
    public int getPoints() {  
        return points;  
    }  
  
    public void setPoints(int points) {  
        this.points += points;  
    }  
  
    public abstract void Point_Counter(int minutos);  
}
Dentro das características da classe nós temos um parâmetro privado chamado "points", ele eh o método construtor da nossa função, ele eh oq solicitamos ao usuário no arquivo Main que veremos depois, veja a linha:
	private int points;

Dentro do método construtor nós informamos uma refra default aos "points", dizendo que eles sempre vão começar no número 0, aqui:
        this.points = 0;  

Temos o "getter" e um "setter" para a nossa característica "points", já que ele pode ser livremente alterado e visualizado pelo usuário. O "setPoint" eh o responsável por fazer acumular os pontos para que não sejam resetados após seu uso, veja:
    public int getPoints() {  
        return points;  
    }  
  
    public void setPoints(int points) {  
        this.points += points;  
    }  

Por fim na última linha nós temos a nossa funcionalidade abstrata, ela se chama "Point_Counter", veja que ela própria recebe um parâmetro, esse parâmetro vai ser futuramente usado para calcular os minutos e a quantidade de pontos que vai ser retornado ao usuário, observe:
    public abstract void Point_Counter(int min);
~~~

~~~Java
ARQUIVO CONSTRUTOR "ALUNO"

public class Aluno extends Pessoa {  
    public Aluno(String nome, String cpf) {  
        super(nome, cpf);  
    }  
  
    @Override  
    public void Point_Counter(int minutos) {  
        int pontos = minutos * 2;  
        this.setPoints(pontos);  
    }  
}
perceba que nas últimas linhas desse código existe o "@Override", vamos ignoralo por enquanto e falar somente da função que vem abaixo dele, notamos que temos uma função publica, ela foi herdada lá da nossa super classe abstrata, perceba que ela continua sendo um "void", portanto não vai retornar nenhum valor e irá apenas executar o cálculo que solicitamos para a mesma. 
O parâmetro "int minutos" tem a mesma função de quanto o criamos na classe abstrata, podemos imaginar que esse parâmetro funciona como o "input" do Python, eh como se tivessemos uma váriavel chamada "minutos" que recebe um input do que o usuário escrever.
Estes minutos são como se fossem uma váriavel que recebe um "input", sabendo disso nós pegamos esses minutos que o usuário escreveu e o fazemos vezes(x) dois, isso significa que o input do usuário dos minutos que ele escreveu são feitos vezes dois, digamos que o usuário escreveu 20, vai ser 20 x 2 e esse resultado eh salvo na váriavel "pontos".
Por último aquela última linha de código quer dizer que o "setter" "setPoints" que criamos lá dentro da classe abstrata vai receber um parâmetro e esse parâmetro eh o resultado da conta que nós fizemos anteriormente
~~~

~~~Java
ARQUIVO DA CLASSE PROFESSOR

public class Professor extends Pessoa{  
    private int salario;  
    public Professor(String nome, String cpf, int salario){  
        super(nome, cpf);  
        this.salario = salario;  
    }  
  
    public int getSalario(){  
        return salario;  
    }  
  
    public void setSalario(int salario){  
        this.salario = salario;  
    }  
   
    @Override  
    public void Point_Counter(int minutos) {  
        int pontos = minutos * 3;  
        this.setPoints(pontos);  
    }  
}
Temos aqui a classe professor, podemos notar que ela recebe o básico de uma classe construtora filho.
Note que ela também possui uma função com o "@Override" que vamos deixar de lado por enquanto.
Ela segue a mesma lógica da classe "Aluno", continua sendo um "void" que recebe em seu parâmetro um número inteiro, como se fosse um input do Python, entretanto a lógica aqui eh um pouquinho diferente, percebemos que os alunos a conta eh feita o número de minutos passados pelo usuário vezes(x) três (minutos * 2), já os professores seguem a mesma lógica porém com a diferenca que o número de minutos deles eh feita vezes 3 (minutos * 3)
~~~


~~~Java
ARQUIVO MAIN

public class Main {  
    public static void main(String[] args) {  
  
        Aluno igor = new Aluno("Igor", "123456789-10");  
        Professor flavio = new Professor("Flávio", "987654321-01", 30000);  
        igor.Point_Counter(10);  
        flavio.Point_Counter(30);  
        System.out.println(igor.getPoints());  
        System.out.println(flavio.getPoints());  
    }  
}
E por fim temos o arquivo "Main", podemos notar que temos dois objetos diferentes aqui, um aluno e um professor.
Lembra quando foi dado o exemplo onde nós podiamos dizer que o parâmetro passado para a função era tipo o "input" do Python, aqui podemos ver isso na prática, podemos ver que passamos 10 para o aluno "igor" e 30 para o professor "flavio", indicarmos para quem aquela função vai ser direcionada eh fundamental para o funcionamente, o Java vai identificar a classe que o objeto pertençe e vai fazer tudo nos conformes das caracteríticas e regras da classe construtora daquele objeto, como o "igor" pertence o classe "Aluno", ele vai seguir as regras e normas daquela classe e isso vale também para as funções já que uma função da certa classe destinta tem regras diferentes, a classe "Aluno" tem regras diferentes da classe "Professor" e por isso os resultados no "pritln" vão ser diferentes para cada um deles. 
~~~


-----------------


## 18: Conceito de Polimorfismo

Um dos pilares da programação orientada a objetos(POO), onde "Poli" vem de muitos e "Morfismo" vem formas, isso na POO quer dizer que uma classe pode ter várias formas dependendo da classe que vai herdar essa funcionalidade. Anteriormente nós criamos um sistema simples que pega o "input" do quantos minutos o objeto leu, ou seja, se o objeto for um aluno o conta vai ser feita de um jeito e caso o objeto seja um professor a conta vai ser executada de outra jeito (lembre-se, estamos falando de objetos dentro do mundo da programação, não leve isso no sentido literal!!), isso já eh o Polimorfismo aplicado, onde um método abstrato tinha uma forma padrão e essa única forma padrão deu origem a outras funcionalidades de duas classes construtoras distintas e acessando elas dependendo do objeto ao qual estamos nos referindo.

Vejamos:

~~~Java
ARQUIVO DA SUPER CLASSE ABSTRATA

public abstract class Pessoa {  
    private String nome;  
    private String cpf;  
    private int points;  
  
    public Pessoa(String nome, String cpf) {  
        this.nome = nome;  
        this.cpf = cpf;  
        this.points = 0;  
    }  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public String getCpf() {  
        return cpf;  
    }  
  
    public int getPoints() {  
        return points;  
    }  
  
    public void setPoints(int points) {  
        this.points += points;  
    }  
  
    public abstract void Point_Counter(int minutos);  
  
    public String greeting_message() {  
        return "Olá " + this.nome + "!";  
    }  
}
Note que na última linha do nosso código nós temos um método não abstrato porém ele está dentro da super classe abstrata, neste caso aqui esse método não vai nos retornar nada nunca justamente por que essa classe eh abstrata e não uma construtora.
~~~

~~~Java
ARQUIVO DA CLASSE ALUNO

public class Aluno extends Pessoa {  
    public Aluno(String nome, String cpf) {  
        super(nome, cpf);  
    }  
  
    @Override  
    public void Point_Counter(int minutos) {  
        int pontos = minutos * 2;  
        this.setPoints(pontos);  
    }  
  
    public String greeting_message() {  
        return "Olá aluno(a) " + this.getNome() + "!";  
    }  
}
Também na última linha nós podemos ver o código que escrevemos nas super classe abstrata, porém aqui nós temos um diferencial pq essa classe por se tratar de uma construtora vai retornar algo para nós, ela sobscreve o que foi inicialmente escrito na super classe abstrata.
~~~

~~~Java
ARQUIVO DA CLASSE PROFESSOR

public class Professor extends Pessoa{  
    private int salario;  
    public Professor(String nome, String cpf, int salario){  
        super(nome, cpf);  
        this.salario = salario;  
    }  
  
    public int getSalario(){  
        return salario;  
    }  
  
    public void setSalario(int salario){  
        this.salario = salario;  
    }  
  
  
    @Override  
    public void Point_Counter(int minutos) {  
        int pontos = minutos * 3;  
        this.setPoints(pontos);  
    }  
  
    public String greeting_message() {  
        return "Olá professor(a) " + this.getNome() + "!";  
    }  
}
E seguindo a mesma lógica da classe do aluno nós temos a mesma função da super classe abstrata que sobscreve o que foi passado anteriormente na mesma
~~~

~~~Java
ARQUIVO MAIN

import javax.xml.transform.Source;  
  
public class Main {  
    public static void main(String[] args) {  
  
        Aluno igor = new Aluno("Igor", "123456789-10");  
        Professor flavio = new Professor("Flávio", "987654321-01", 30000);  
        System.out.println(igor.greeting_message());  
        System.out.println(flavio.greeting_message());  
    }  
}
Por fim temos o arquivo "Main" que chama essa a função que acabamos de ver, utilizando a mesma lógica que no último tópico que vimos antes quando um objeto eh chamado automáticamente todas as instâncias atribuidas a classe de origem daquele objeto vão aparecer e se adaptar conforme a mesma pede, seguindo a regras que foram passadas em sua classe de origem.
Como aqui nós temos a classe "Aluno" que está chamando a função "greeting_message()" na mesma hora o Java vai saber que esse comando faz referência ao que está dentro do classe de origem do objeto "igor", o mesmo vale para o professor também.
~~~


------------------


## 19: Interfaces

Um outro conceito da POO são as interfaces, elas são muito confundidas com o que vemos na herança de classes. Digamos que nós temos uma classe abstrata, nós já sabemos ela não pode criar objetos justamente por ser uma classe abstrata e somente classes que herdam essas classes podem criar os objetos, os métodos também não fogem disso, onde dependendo de sua classe pode ser subscrita para atender as necessidades daquela classe.

O conceito de Interface eh um contrato criado para que a classe que utiliza deste contrato ela tenha que implementar esse contrato, como se fosse na vida real literalmente (aqui podemos ver novamente um dos principais conceitos da Programação Orientada a Objetos).

Assim que uma Interface eh criada podemos ver sua estrutura básica, sendo ela assim:

~~~Java
ARQUIVO DE INTERFACE "User"

public interface User {  

}
Essa eh a estrtura base de uma Interface, muito parecida com o classe.
~~~

Como dito antes uma interface eh como se fosse um contrato e para que seja implementado os   termos desse contrato nós precisamos adicionar assinaturas de métodos e atributos, este métodos e atributos NÃO vão ser implementados e NÃO vão receber nenhum tipo de valor dentro do arquivo da interface já que as interfaces são SOMENTE para assinaturas, para que tenhamos modelos/formatos a serem implementados dentro de uma classe. Essa é a diferença de uma classe abstrata que pode ter atributos, métodos, valores(...) implementados dentro dela e isso não acontece nas interfaces.

Para implementarmos interfaces nos arquivos nós usamos o termo "implement" logo após o nome da classe bem na primeira linha, assim:

~~~Java
ARQUIVO DE EXEMPLO INEXISTENTE

public class Classe_Construtora extends Classe_Abstrata implements Interface {

}
Assim desse jeito nós acabamos de dizer que uma classe construtora herda de uma super classe abstrata e ela implementa o "contrato" de uma interface, eh como se nós mandassemos uma classe construtora construir algo usando esses materiais (da classe abstrata) e essas ferramentas tendo que seguir essa norma prevista no contrato da empresa (usando a interface que ela implementa).
~~~

Vejamos um exemplo mais completo agora:

~~~Java
ARQUIVO DA SUPER CLASSE ABSTRATA

public abstract class Pessoa {  
    private String nome;  
    private String cpf;  
    private int points;  
  
    public Pessoa(String nome, String cpf) {  
        this.nome = nome;  
        this.cpf = cpf;  
        this.points = 0;  
    }  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public String getCpf() {  
        return cpf;  
    }  
  
    public int getPoints() {  
        return points;  
    }  
  
    public void setPoints(int points) {  
        this.points += points;  
    }  
  
    public abstract void Point_Counter(int minutos);  
}
Compare esse código com o último que vimos antes no tópico anterior, perceba que aquela função não existe mais aqui nessa classe já que ela se tratava de uma classe abstrata e alem daquele código estar nela ele também não era abstrato, ele tentava executar uma ação caso existisse um objeto "Pessoa" porém isso nunca iria aconteçer pois essa classe eh abstrata e ela não pode gerar novos objetos, apenas regras as classes que geram os objetos.
~~~

~~~Java
ARQUIVO DA CLASSE ALUNO

public class Aluno extends Pessoa implements User {  
    public Aluno(String nome, String cpf) {  
        super(nome, cpf);  
    }  
  
    @Override  
    public void Point_Counter(int minutos) {  
        int pontos = minutos * 2;  
        this.setPoints(pontos);  
    }  
  
    public String greeting_message() {  
        return "Olá aluno(a) " + this.getNome() + "!";  
    }  
}
Perceba que aqui nós já temos outras mudanças, veja como logo na primeira linha do código possui uma novo método, "implements User" isso quer dizer que a classe "Aluno" implementa o contrato da interface "User" e toda aquela primeira linha significa exatamente oq fizemos no primeiro código deste tópico, onde uma classe construtora vai construir algo usando os materias dela e da super classe abstrata porém seguindo as normas do contrato que ela assinou usando o "implement".
Na útima linha de código podemos ver que o código para a mensagem de boas vindas não mudou já que ele agora está sendo puxado de outro lugar porém sua lógica continua a mesma.
~~~

~~~Java
ARQUIVO DA CLASSE PROFESSOR

public class Professor extends Pessoa implements User {  
    private int salario;  
    public Professor(String nome, String cpf, int salario){  
        super(nome, cpf);  
        this.salario = salario;  
    }  
  
    public int getSalario(){  
        return salario;  
    }  
  
    public void setSalario(int salario){  
        this.salario = salario;  
    }  
  
    @Override  
    public void Point_Counter(int minutos) {  
        int pontos = minutos * 3;  
        this.setPoints(pontos);  
    }  
  
    public String greeting_message() {  
        return "Olá professor(a) " + this.getNome() + "!";  
    }  
}
Ainda seguindo a mesma lógica do códig oque vimos antes, ele ainda continua recebendo as materias e da super classe abstrat e tendo que seguir as normas assinadas no contrato da interface "User".
A última função também não apresenta alterações, ela continua com a mesma lógica e seguindo as mesmas regras, a única excessão eh que aqui estamos dando as boas vindas a um professor, logo a mensagem muda para ser coerente com quem está recebendo essa mensagem, apenas.
~~~

~~~Java
ARQUIVO DA INTERFACE "User"

public interface User {  
    public String greeting_message();  
}
Veja como apenas algumas linha de código evitarem várias dores de cabeça, vamos entender bem passo-a-passo do que aconteçeu aqui:

Criamos uma interface que regfra todos que implementam essa interface, isso quer dize que qualquer classe que tiver um "implements User" vai ter que obrigatoriamente está escrito nessa interface.

Temos uma função publica String que recebe o nome de "greeting_messege()", isso quer dizer que qualquer classe que implementar a interface "User" vai ter que obrigatoriamente ter essa mesma função nela.

E como nós vimos anteriormente as classes construtoras que implementaram/assinaram esse contrato tinham essa função junto delas porém elas alteravam seus blocos para se adaptar ao que cada classe era, na classe "Aluno" a mensagem se adaptou para receber a um aluno com uma mensagem e já na classe "Professor" a mensagem foi readaptada para dar as boas-vindas a um professor.
~~~

~~~Java
ARQUIVO MAIN

public class Main {  
    public static void main(String[] args) {  
  
        Aluno igor = new Aluno("Igor", "123456789-10");  
        Professor flavio = new Professor("Flávio", "987654321-01", 30000);  
        System.out.println(igor.greeting_message());  
        System.out.println(flavio.greeting_message());  
    }  
}
Por fim temos o arquivo "Main", ele aqui nesse momente eh responsável apenas por chamar as duas funções que criamos anteriormente.
~~~~


----


## 20: Métodos Estáticos

Digamos que tenhamos um classe que faz três cálculos simples de dois números escolhidos pelo usuário, como somar, subtrair e multiplicar. Para que isso seja possível tivemos que instanciar um novo objeto que faça esse cálculos, ela não recebe nenhum parâmetro dentro de seu método construtor e simplesmente disponibilizou funções para podermos manipular números com oq foi criado dentro da classe. 

Os métodos estáticos entram justamente nesse meio, eles entram nessa parte para que não seja necessário criar um objeto para calcularmos esses números, ele faz com que os métodos de uma classe sejam estáticos e que possamos usar os mesmo de uma maneira estática, sem instâncias desnecessárias.

Para dizermos que uma classe eh estática devemos fazer com que seus métodos sejam estáticos, onde antes de dizermos o tipo primitivo do função nós dizemos seu tipo de acesso, assim:

~~~Java
ARQUIVO DE UMA CLASSE ESTÁTICA DE EXEMPLO (INEXISTENTE)

public class Classe_estatica_de_exeplo {  
    public static double exemplo1() {  
          
    }  
}
Podemos ver bem aqui como uma classe estática funciona (lembre-se, estou usando o termo "classe estática" para esse tópico somente, já que aqui somente suas funcionalidades qu são estáticas, não a classe), podemos ver que ela continua sendo uma classe pública padrão sem nenhuma outra adição.
Dizemos que esta classe eh estática pq seu(s) método(s) são estáticos e neste exemplo temos uma função pública que recebe o termo "static" para dizermos que ela eh estática, só após isso podemos passar seu tipo primitivo, seu nome e seus parâmetros.
~~~

De uma maneira resumida, quando nós temos uma classe que guarda métodos estáticos necessidade de criamos um objeto específico só para podermos usar os métodos que esse objeto trás com ele, o legal de usar esses métodos estáticos também eh que podemos chamá-los sem precisar declarar variáveis e nem criar objetos, podemos chamá-los dentro uma um "println", vejamos o exemplo:

~~~Java
ARQUIVO DA CLASSE ESTÁTICA

public class Calculadora {  
  
    public static double soma(double n1, double n2) {  
        return n1 + n2;  
    }  
  
    public static double subtracao(double n1, double n2) {  
        return n1 - n2;  
    }  
  
    public static double multiplicacao(double n1, double n2) {  
        return n1 * n2;  
    }  
}
Aqui nós temos uma classe estática (lembre-se que não eh a classe que recebe uma parâmetro estático e sim as funcionalidades dentro dela), podemos ver que esta classe tem três métodos que recebem o "static" e por isso estamos a chamando de classe estática, estes métodos por se tratarem de  serem estéticos e públicos podem ser chamados de qualquer lugar.
O código por si só eh bem autoexplicativo, temos três funções estáticas que recebem dois parâmetros cada e depois elas executam a conta que cada uma sugere pelo nome.
~~~

~~~Java
ARQUIVO DA CLASSE MAIN

public class Main {  
    public static void main(String[] args) {  
  
        System.out.println(Calculadora.soma(1, 9));  
        System.out.println(Calculadora.subtracao(10, 9));  
        System.out.println(Calculadora.multiplicacao(2, 5));  
    }  
}
E por fim aqui temos o arquivo "Main", note como foi simples executar a função estática, não precisamos declarar nenhuma variável e nem criar nenhum objeto, fizemos tudo dentro do "println", passamos o nome da classe estática "Calculadora" e depois apenas chamamos a funçao que desejamos usar das que aquela classe oferecia, simples assim.
~~~


-----------------------------------------------------------------


## 21: Pacotes

Fugindo um pouquinho do POO e falando mais sobre o Java por si só nós temos os pacotes, eles são coisas usadas para separar classes, são como se fossem um diretório dentro do código, podemos usar bibliotecas de fora, importar classes e etc. Isso serve para que não tenha conflitos de classes dentro do código fonte, podemos separar as por pastas estes pacotes e usar o que convém na hora sem o perigo de rolar conflitos.

Quando nós vamos escrever algo no intelliJ ele mostra logo ao lado do comando um texto, esse texto diz de qual pacote vem aquele comando em específico, por exemplo, após digitarmos "String" a IDE vai sugerir os comandos que podemos escrever e logo ao lado de qual pacote ele vem, no caso da "String" logo ao lado dela vem o "java.lang", isso quer dizer que o método "String" eh um pacote padrão do próprio Java, já que todo pacote padrão do Java sempre começa com "java.".

O uso do "." eh como se fosse uma "/", ainda usando o exemplo da "String" nós temos o "java.lang", isso quer dizer que o método "String" está no diretório padrão do Java chamado "java/lang".

Para criarmos nossos próprios pacotes nós podemos dar o nome que quisermos, porém uma medida padrão adotada pela própria comunidade eh a seguinte forma:
br.com.nomedaempresa.nomedopacote.nomedogrupodepacotes

**vejamos por partes:**
- No começo temos o "br.com" isso eh o padrão para dizermos que eh um pacote do Brasil basicamente.

- Em "nome da empresa" nós podemos passar o nome da empresa, o nome do software que está sendo criado e etc. Isso serve como uma medida de organização dos pacotes para que o pacote de um cliente não seja misturado nem confundido com outro.

- "nome do pacote" eh exatamente o que seu nome sugere, aqui fica aberto para escolhermos o nome que aquele pacote vai ter.

- E por fim temos o "grupo de pacotes", isso eh para passarmos de qual grupo aquele pacote pertence, isso vai depender bastante do projeto que está sendo criado na hora.

Para podermos criar um pacote, nós precisamos apertar com o botão direito na pasta que desejamos criar o pacote, clicar e "new" e depois em "package" e basta escolhermos seu nome seguindo o padrão que a comunidade usa de preferência.

Quando temos algo dentro de uma pasta "package" o nome/extensão do pacote vem logo acima da declaração da classe por exemplo, veja:

~~~Java
package br.com.packagetest.package1.classesABC;  
  
public class ClasseA {  

}
Aqui temos o arquivo de uma classe que está dentro do diretório "br.com.packagetest.package1.classesABC", ele segue exatamente a mesma norma de nome que a comunidade normalmente usa, isso geralmente eh para questões de um código limpo e organizado, lavando a imagem de um bom programador além de ser uma boa prática por si só.
~~~

É sempre muito importante lembrar que os pacotes no Java são como se fossem diretórios ou pastas se preferir. 

Agora temos um pacote com esse nome "package br.com.packagetest.package1.classesABC", ele eh o pacote que aparece no código logo acima, vamos supor que dentro do arquivo principal (SRC), nós tenhamos que criar um novo pacote por algum motivo, esse pacote pertence ao mesmo cliente e está sendo usado no mesmo projeto do pacote que criamos anteriormente, neste caso se nós criarmos um pacote com o nome de "packagetest" quer dizer que ele eh da mesma empresa, do mesmo diretório que o pacote "dono", como se fosse uma pasta que armazena todos os pacotes que contenham esse nome, veja como podemos organizar isso:

![[Screenshot_14.png]]

assim nós podemos ver como estes pacotes ficariam organizados, sendo que nesse exemplo temos um pacote "pai", esse pacote recebe o nome da empresa, projeto ou seja lá o que for, todos os outros pacotes que também conterem esse nome vão automaticamente se agrupar dentro desse pacote "pai".

Não muito diferente de qualquer outra linguagem de programação. esses pacotes vão precisar comunicar-se entre si tanto para receber dados, processar esses dados e devolver ao request do server. Quando uma classe está dentro do mesmo pacote de uma outra classe elas podem se comunicar entre si sem problemas, digamos que dentro de "classesABC" nós tenhamos justamente estas classes, como elas estão dentro de um mesmo diretório de pacote elas se comunicar sem interferência, agora digamos que tenhamos dentro de "classesDE" as classes sugeridas e a classe D precisa pedir algo para a classe A, como isso poderia acontecer? Para que isso ocorra nós vamos precisar usar o "import" e logo passarmos o nome do pacote que desejamos importar, assim:

~~~Java
ARQUIVO DA CLASSE D

package br.com.packagetest.package2.classesDE;  
  
import br.com.packagetest.package1.classesABC.ClasseA;  
  
public class ClasseD {  
    ClasseA classeA = new ClasseA();  
}
Aqui temos um simples código, podemos ver que o arquivo da classe D está no mesmo pacote "pai", porém em uma pasta separada do da classe A, podemos ver que a classe A se localiza no diretório "package1.classesABC" enquanto a classe D se localiza no "package2.classesDE".
O "import" entra nessa hora, podemos ver que ele diz exatamente oq queremos importar, ele acessa a classe "pai", depois acessa o diretório "package1", acessa o grupo "classesABC" e depois disso ele escolhe exatamente a classe que queremos importar para usarmos em uma outra classe que se localiza num diretório totalmente diferente da classe A.
~~~

Como nós estamos usando o "intelliJ" como nossa principal IDE, ele automaticamente auxilia na hora de chamarmos uma pacote de diferentes pastas, nós só precisamos criar o objeto da classe normalmente que ele automaticamente vai criar o caminho do pacote a ser importado.

Vamos super que tenhamos um projeto com um pacote pai chamado "packagetest", e outros dois pacotes que fazem parte desse mesmo projeto porém eles contém nomes diferentes e pertencem a grupos de pacotes diferentes. Dentro do primeiro pacote filho com a seguinte extensão "package1.classesABC" contém três classes diferentes, e no outro pacote com a extensão "package2.classesDE" possuem outras duas classes, estes dois pacotes estão dentro de uma única classe pai porém não estão juntos e sim separados devido ao seu nome e grupo de pacotes distintos, isso ficaria exatamente assim:

![[images/Screenshot_13.png]]

neste exemplo podemos ver exatamente a organização dos pacotes pai e dos pacotes que a ele pertence, junto desses sub-pacotes vemos as classes que fazem parte destes pacotes menores. 

### 21.1: Modificadores de acesso entre pacotes

A alguns tópicos atrás nós vimos como os modificadores de acesso funcionam dentro do POO, vimos o que são classes públicas, privadas, estáticas e etc. Podemos aplicar os modificadores de acesso também nos entre os pacotes. 

**Os modificadores de acesso que podemos usar são:**
- public = pode ser acessado de qualquer lugar a qualquer hora.

- private = só pode ser acessado dentro da classe de origem ou com os "getter" para visualização e o "setter" para modificação.

- protected =

- default = nenhum modificador de acesso definido para ele e por isso não pode ser declarado, pois vem padrão quando algo não tem seu modificador explicitamente definido.

Dentre os 4 modificadores somente o "public", "private" e o "protected" podem ser declarados como nos exemplos que vimos. Os modificadores de acesso tem a mesma funcionalidade tanto para métodos tanto para atributos, eles não se alteram e continuam executando a mesma função igualmente para os dois. Para declararmos o modificador de acesso de um atributo ou de uma funcionalidade nós precisamos declara-lo antes de dizermos o tipo de dado do que estamos criando, como vimos nos exemplos anteriores.

Quando nós temos um atributo "default" ele pode ser livremente acessado de outras classes que estão no mesmo pacote onde esse "default" foi declarado, porém outras classes de outros pacotes diferentes do pacote de origem dessa classe "default" não podem acessar essa classe, ele fica meio que no meio termo entre uma atributo público ou não. O público pelo contrário permite que o atributo possa ser acessado de qualquer lugar a qualquer hora independente de onde está sendo chamado, um atributo público pode ser chamado de vários pacotes distintos de seu pacote de origem.

O "protected" serve para proteger as propriedades de outros pacotes de origem, ou seja, isso quer dizer que se um método recebe o "protected" qualquer classe que esteja no no mesmo pacote de origem do método que recebeu o "protected" pode acessá-lo livremente, porém qualquer outra classe que seja de um pacote deferente de onde o "protected" foi declarado não poderá acessar essa propriedade, somente quem está no mesmo pacote de origem poderá acessar ele. Para que uma propriedade "protected" possa ser acessada de uma classe distinta do seu pacote de origem a classe que vai receber o "protected" deve estender da classe de origem da propriedade protegida, e o objeto criado não pode ser a classe que possui o "protected" e sim a classe que vai receber o mesmo, vejamos:

~~~Java
ARQUIVO DE ORIGEM QUE CONTÉM O "PROTECTED"

package br.com.packagetest.package1.classesAB;  
  
public class ClasseA {  
    protected String nome = "Classe A de teste";  
}
Aqui nós podemos ver que nessa classe temos um String protegida, essa String protegida recebe seu nome de "nome", veja bem a origem do pacote e observe bem onde ele esta localizado.
~~~

~~~Java
ARQUIVO QUE CHAMA O "PROTECTED"

package br.com.packagetest.package2.classeC;  
  
import br.com.packagetest.package1.classesAB.ClasseA;  
  
public class ClasseC extends ClasseA {  
    public static void main(String[] args) {  
        ClasseC classeC = new ClasseC();  
        System.out.println(classeC.nome);  
    }  
}
Aqui a história muda um pouquinho, veja como nós importamos a "ClasseA", importamos ela para que possamos chamar a propriedade "nome" que foi criada anteriormente.
Observe que nos criamos um objeto a partir da "ClasseC" e não da "ClasseA", quando nós extendemos uma classe e queremos chamar uma propriedade dela nós não criamos um objeto a partir dela e sim da classe que está herdando a propriedade protegida.
Podemos dizer básicamente que nós importamos a "ClasseA"(isso inclui TUDO que está dentro da "ClasseA"), criamos um objeto a partir da "ClasseC" e depois dentro do "println" nós chamamos esse objeto que criamos e usando o parâmetro "nome"(sendo ele a funcionalidade protegida da "ClasseA") nós o usamos, como se ele foss um método da "ClasseC" mesmo sem ser.
~~~

resumidamente, uma funcionalidade protegida só pode ser acessada por qualquer classes dentro do pacote de origem de onde foi criado, caso contrário ele só poderá ser acessado se a classe do pacote distinto herdar a classe de origem da funcionalidade protegida.


-----------------------------------------------------------------


## 22: Design Patterns

A humanidade constantemente criam vários problemas e solucionam outros, algumas dessas soluções não mudam e continuam frequentemente a mesma solução, um exemplo disso eh a roda de um carro, por mais que seu material e forma de construção possa variar ela sempre vai continuar sendo uma roda que sempre vai cumprir o solucionar um problema, são como se fossem medidas padrões impostas para ajudar a sociedade e poupar tempo sem precisar de variações já que tudo está padronizado. O mesmo vale para a programação, onde ao longo dos anos vários problemas surgiram no mundo da programação, porém estes problemas foram sendo solucionados com o passar do tempo, isso permite que vários problemas possam ser resolvidos com algum padrão que já foi criado tempos atrás. 

Conhecer estes tipos de padrões eh extremamente importante, pois para vários tipos de problemas existem padrões específicos para sua solução.

O site [[https://refactoring.guru]] nos ajuda a entender estes padrões, ele oferece vários exemplos de padrões para problemas típicos que enfrentamos no desenvolvimento de software. Ele apresenta padrões estruturais, padrões comportamentais e etc.


-----------------------------------------------------------------


## 23: Factory

A tradução literal de "Factory" e Fábrica, ele consiste na criação de objetos a partir de algum padrão especifico para que possam ser usados em sub-classes que compartilham do mesmo padrão um estilo de fabricação de objetos basicamente.

O uso do "Factory" eh de extrema importância, vamos supor que você tenha um sistema logístico de entregas, você tem uma classe que controla toda a logística de do caminhão, calculando rotas, quantidade de combustível gasto, locais de descanso e tudo mais, porém recentemente você adquiriu um navio para fazer estes transportes e começar a exportar e importar coisas e agora você precisa implementar as novas regras desse novo tipo de transporte, já que as regras do transporte terrestre não se aplicam ao transporte marítimo. Toda a regra de transporte está dentro da classe caminhão e agora como vc adquiriu um navio para o seu negócio vc precisa criar uma classe para esse navio e criar toda a logística do código novamente.

O "Factory" pode ajudar a resolver esse problema, onde podemos criar uma fábrica que dependendo do tipo de transporte que queremos utilizar a nossa fábrica vai construir um objeto para ele, se o tipo de transporte for um avião cargueiro a fábrica vai automaticamente criar um objeto para esse tipo de transporte

Um outro exemplo que podemos usar é, imagine que temos um sistema bancário multinacional, imagine ter que instanciar um objeto para cada tipo de moeda existente no mundo? Podemos usar a "factory" para automatizar essa função, dependendo do país do usuário ela automaticamente cria o objeto para a moeda que o usuário está usando.

Antes de criarmos uma "factory" eh necessário entender quais são as características em comum dos objetos que a fábrica vai criar, usando o exemplo do sistema bancário a característica em comum eh prefixo das moedas, o Real eh de um diferente do dólar.

Vamos seguir o seguinte exemplo, digamos que tenhamos um sistema de banco que atua em vários países diferentes, o sistema vai precisar lidar com conversões de moedas diferentes, regras de prefixos diferente e etc. Dentro desse sistema nós temos que fazer a conversão do prefixo de cada tipo de moeda, por exemplo o dólar tem seu prefixo "$" enquanto o real tem seu prefixo diferente do dólar, o sistema deve agir para retornar o prefixo certo para cada tipo de moeda.

para isso teremos duas classes, uma que contém a regra do prefixo do real e outra que contém o prefixo do real e estas classes estarão dentro de um pacote que guarda esse sistema em específico.

veja bem os detalhes, estamos trabalhando com regras padronizadas, onde cada uma dessas classes contem um prefixo diferente, isso pode ser construído com uma "factory" e podemos usar uma "interface" para definir essa regra, veja os códigos detalhadamente:

~~~Java
ARQUIVO DA INTERFACE

package br.com.logisticas.patterns.factory;  
  
public interface Moeda {  
    public String getPrefixo();  
}
Veja bem como esse código funciona, note como ele esta estruturado, essa interface aqui quer dizer que toda classe que assinar dela terá obrigatoriamente que implementar a funcionalidade "getPrefixo", essa funcionalidade terá que ser também obrigatoriamente uma String.
~~~

~~~Java
ARQUIVO DA CLASSE REAL

package br.com.logisticas.patterns.factory;  
  
public class Real implements Moeda {  
    public String getPrefixo() {  
        return "R$";  
    }  
}
Agora vamos observar a classe reponsável pela mudança do prefixo do real, veja bem o pacote que ela está localizada também. Observe que a classe "Real" assina um contrato com a nossa interface que diz que toda a classe que assina um contrato com ela deve obrigatoriamente implementar a funcionalidade "getPrefixo()" já que eh essa a funcionalidade responsável por mudar o prefixo dependendo da moeda. 
~~~

~~~Java
ARQUIVO DA CLASSE DÓLAR

package br.com.logisticas.patterns.factory;  
  
public class Dolar implements Moeda {  
    @Override  
    public String getPrefixo() {  
        return "$";  
    }  
}
Temos aqui a classe do dólar, ela eh a responsável por alterar o prefixo caso a moeda seja o dólar. Essa classe segue a mesma lógica da que vimos anteriormente, ela assina um contrato com o nossa interface "Moeda", e essa interface diz que quem assinar ela terá que implementar a funcionalidade "getPrefixo()", sendo que essa funcionalidade eh responsável por aletrar o prefixo da nossa moeda, neste caso aqui ela vai alterar por dólar caso a moeda seja realmente o dólar. 
~~~

nestes três códigos que vimos agora eh perceptível que não existe nenhuma fábrica aqui, vimos até agora somente a abstração da fábrica, isso que vimos eh o esqueleto da fábrica, não adianta criar a fábrica se não tem o que ela produzir certo?

Partindo para a construção da fábrica em si, eh uma boa prática que quando criarmos uma "factory" sempre passamos métodos estáticos já que isso dá mais coerência ao código.

Veremos agora um exemplo prático de verdade, neste exemplo teremos duas classes, uma fábrica, uma interface e o arquivo main. Dentro desse exemplo teremos um sistema que pede um parâmetro ao usuário, o usuário var passar o parâmetro e depois o sistema vai retornar o prefixo da moeda local do pais que o usuário escolheu.

~~~Java
ARQUIVO DA INTERFACE "Moeda"

package br.com.logisticas.patterns.factory;  
  
public interface Moeda {  
    public String getPrefixo();  
}
Aqui nós temos nossa interface, ela diz que todos que assinarem dela terão obrigatoriamente que ter uma função "getPrefixo()" dentro do seu código. Isso serve principalmente para que o return dentro dos outros códigos tenham um efeito que seja possivel visualizalos, para assim o sistema poder trazer o prefixo da moeda local do país selecionado.
~~~

~~~Java
ARQUIVO DA CLASSE "Real"

package br.com.logisticas.patterns.factory;  
  
public class Real implements Moeda {  
    public String getPrefixo() {  
        return "R$";  
    }  
}
Nesta classe aqui temos um código que assina o contrato com a interface que vimos anteriormente. observe que essa classe eh responsável apenas por retornar o prefixo da moeda, onde nesse caso eh o real. 
Eh possível dizer que esse código eh como a planta de uma construção, são as instruções para o que a fábrica deve produzir.
~~~

~~~Java
ARQUIVO DA CLASSE "Dolar"

package br.com.logisticas.patterns.factory;  
  
public class Dolar implements Moeda {  
    @Override  
    public String getPrefixo() {  
        return "$";  
    }  
}
A mesma coisa da classe que vimos anteriormente vale para essa classe aqui também.
~~~

~~~Java
ARQUIVO DA FÁBRICA "MoedaFactory"

package br.com.logisticas.patterns.factory;  
  
public class MoedaFactory {  
    public static Moeda getInstance(String pais) {  
        return switch (pais) {  
            case "BR" -> new Real();  
            case "EUA", "CA" -> new Dolar();  
            default -> throw new IllegalArgumentException("[ERRO] O país selecionado não eh válido!");  
        };  
    }  
}
Essa classe aqui eh a responsável por fabricar os nosso objetos, podemos ver que ela logo de cara já recebe uma função que tem uma ligação direta com a interface, isso significa que quando escrevermos "moeda" dentro do nosso arquivo maim vamos estar chamando o método "getInstance", esse método pede ao usuário dentro dos seus parênteses que seja informado o pais que ele quer ver o prefixo.
Dentro da indentação do método "getInstance()" temos um estrutua switch, dentro dos parentêses da estrutura switch temos o parâmetro "pais", isso quer dizer que a estrutura switch vai pegar o país que o usuário escreveu e comparar com o que ela tem dentro da sua indentação.
Falando agora sobre o que a estrutura switch analisa, podemos ver que no primiro case temos um "BR", isso quer dizer que se o parâmetro escolhido pelo usuário for "BR" ela vai dar um retorno a um novo objeto da classe "Real()", o mesmo vale para o dólar também.
E na última linha do switch temos o nosso default, ele quer dizer que caso o parâmetro país não seja "BR", "EUA" ou "CA" ele vai retornar um texto de erro no nosso terminal para que o usuário escolha um país válido.
~~~

~~~Java
ARQUIVO MAIN

package br.com.logisticas.patterns.factory;  
  
public class MainTeste {  
    public static void main(String[] args) {  
        Moeda moeda = MoedaFactory.getInstance("EUA");  
        System.out.println(moeda.getPrefixo());
    }  
}
E por fim temos o arquivo Main, vejamos que nele temos, usando a regra que temos na interface nós criamos uma variável para podermos chamar a função da fábrica. Eh quase como se estivessemos criando um objeto a partir da nossa interface, podemos dizer que chamamos nossa interface para regrar isso tudo. Chamando a nossa fábrica logo em seguida e usando o método que criamos, o "getInstance()" nós passamos o país de origem que queriamos que fosse retornado o prefixo, como nesse caso foi o "EUA", lá na nossa fábrica o switch do "EUA" foi ativado, assim cirnando um novo objeto para.
Por fim temos o println, nele encontramos o "meoda.getPrefixo()", isso quer dizer estamos chamando nossa variável que guarda o resultado do prefixo solicitado e pedindo para que ele seja escrito no terminal.
~~~

**O código pode ter ficado meio confuso, então vamos ver ele dessa maneira:**
- Temos duas classes, uma chamada "Real" e a outra "Dolar", elas  assinam o contrato com a nossa interface, por isso elas possuem a funcionalidade "getPrefixo()", mais pra frente vamos entender seu uso.
- A interface eh responsável por regrar todos que agregam a mesma. Sua funcionalidade "getPrefixo()" eh fundamental para que aja um retorno no nosso terminal depois, essa funcionalidade eh a responsável por entregar o prefixo da moeda que o usuário vai solicitar no Main, chamando essa funcionalidade temos o retorno desse prefixo, por isso a importância dessa interface e a funcionalidade "getPrefixo()"
- Falando sobre a fábrica agora, ela eh totalmente estática, ela não retorna nenhum valor para nós, ela eh responsável exclusivamente por gerar os novos objetos que o usuário solicitar, o método "getInstance(String pais)" eh para perguntar ao usuário qual pais que ele deseja ter o retorno do prefixo e eh exatamente nesse momento que entra o switch, ele analisa o pais selecionado pele usuário com o que ele tem nas cases dele, se o país for o "EUA" ele vai criar um novo objeto com a classe dólar(lembra-se que nas classes Real e Dólar tem o getPrefixo). Ainda no switch existe o "default", ele serve para informar algum erro, caso o usuário escolha algum país inválido o sistema vai devolver um novo erro argumentativo, isso quer dizer que o argumento passado (nesse caso, o argumento pais) for inválido ele vai retornar uma mensagem de erro no terminal.
- Já no nosso arquivo main, podemos observar que ele recebe e declara um variável que vem da interface Moeda, isso eh para que o função "getPrefixo()" funcione depois. Após isso depois do "=" nós chamamos nossa classe responsável por fabricar os objetos e chamamos sua funcionalidade, funcionalidade essa responsável por pedir o país desejado pela usuário. E por fim temos o println, chamamos nossa variável "moeda" e pedimos a funcionalidade "getPrefixo()", isso que vai nos devolver o prefixo da moeda do país selecionado, isso acontece pq todas as classes Real e Dólar tem essa função com elas que retornam o seu prefixo, e quando um novo objeto (com base no país que o usuário passou) eh criado nós chamamos essa função que retorna o prefixo dessa moeda.


-----------------------------------------------------------------


## 24: Builder

O builder eh conhecido como construtor, ele eh um padrão de projeto criacional, permitindo a construção de objetos complexos passo a passo. Ele permite que objetos sejam montados com o decorrer de certa ações do código, antes na hora de criar um objeto todos os parâmetros e funções deviam ser passados na hora, porém com o builder essa necessidade se torna inútil já que com ele podemos ir montando o objeto por etapas, pecinha por pecinha.  

Podemos usar um carro como exemplo, pois o carro é um objeto complexo que pode ser construído em centenas de maneiras diferentes. Ao invés de inchar a classe `Carro` com um construtor enorme, nós extraímos o código de montagem do carro em uma classe de construção de carro separada. Essa classe tem um conjunto de métodos para configurar as várias partes de um carro, assim separando e dividindo o que antes seria um método construtor enorme.

Padronizar o builder permite que a construção de um único método construtor desnecessariamente grande seja abstraída, permitindo que o objeto seja construído passo a passo, usando somente etapas realmente necessárias, descartando assim um método construtor cheio de parâmetros.

Um dos passos para criar um builder eh usar uma interface, esse passo eh totalmente opcional, ela permite que um padrão seja implementado definido pelo projeto para a organização do código.

Vamos supor que estamos criando um sistema para um hospital, onde temos os seguintes parâmetros dentro de um método construtor:
 - nome 
 - e-mail 
 - CPF
usaremos poucos métodos neste exemplo justamente por ser um exemplo. Vamos ver sua construção separadamente para melhorar o entendimento de como chagamos no resultado, explicando cada passo feito e cada alteração.

Vamos criar um "builder" que vai criar automaticamente esse objeto "Paciente" de uma maneira mais dinâmica, criada a partir de um passo a passo.

criando uma interface que exige obrigatoriamente os três métodos que citamos anteriormente, todos eles sendo do tipo void, já que eles não vão retornar nenhum valor, vão apenas altera-lo, desee jeito:

~~~Java
ARQUIVO DA INTERFACE 

package br.com.mainpatterns.patterns.builders;  
  
public interface BuilderRuler {  
    public void setNome(String nome);  
    public void setEmail(String email);  
    public void setCpf(String cpf);  
}
Aqui nós temos o começo do nosso builder, ele diz que qualquer classe que implementar do mesmo terá que obrigatoriamente adicionar essas três funcionalidades em seu código, fazemos isso pois era isso que estaca no método construtor antes de fazermos o builder, geralmente quando usamos a interface nós passamos todos os métodos que antes iam no contrutor na própria interface, depois os configuramos mais a fundo na classe construtora. 
Esse passo eh totalmente opcional, porém por questões de organização e optar por um código limpo vamos fazer desse jeito.
~~~

~~~Java
ARQUIVO DA CLASSE "Paciente"

package br.com.mainpatterns.patterns.builders;  
  
public class Paciente {  
    private String nome;  
    private String email;  
    private String cpf;  
  
    public Paciente(String nome, String email, String cpf) {  
        this.nome = nome;  
        this.email = email;  
        this.cpf = cpf;  
    }  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public String getEmail() {  
        return email;  
    }  
  
    public void setEmail(String email) {  
        this.email = email;  
    }  
  
    public String getCpf() {  
        return cpf;  
    }  
  
    public void setCpf(String cpf) {  
        this.cpf = cpf;  
    }  
}
Esta classe eh como se fosse o paciente, aqui podemos observar vários detalhes, vemos que no método construtor existem todos os três parâmetros que citamos anteriormente, cada um deles possui um "setter" e um "getter" para que eles possam ser editados e visualizados.
~~~

~~~Java
ARQIOVO DA CLASSE "PacienteBuilder"

package br.com.mainpatterns.patterns.builders;  
  
public class PacienteBuilder implements BuilderRuler {  
    private String nome;  
    private String email;  
    private String cpf;  
  
    @Override  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    @Override  
    public void setEmail(String email) {  
        this.email = email;  
    }  
  
    @Override  
    public void setCpf(String cpf) {  
        this.cpf = cpf;  
    }  
}
Nesta classe aqui podemos observar que ela assina o contrato com a nossa interface, herdando todos os métodos passados na interface.
Observe que temos somente o set aqui, isso pq nós vamos editar esses atributos dentro do builder e não precisamos que ele retorne um valor visível de volta, isso pelo simples fato que ele vai apenas construir um objeto.
~~~

Após vermos o começo da construção do builder e como dar os primeiros passos, vamos partir para por um pouca mais em prática isso tudo, vamos fazer com que o builder realmente tenha uma funcionalidade e construir o objeto "Paciente"

~~~Java
ARQUIVO DA CLASSE "PacienteBuilder"

package br.com.mainpatterns.patterns.builders;  
  
public class PacienteBuilder implements BuilderRuler {  
    private String nome;  
    private String email;  
    private String cpf;  
  
    @Override  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    @Override  
    public void setEmail(String email) {  
        this.email = email;  
    }  
  
    @Override  
    public void setCpf(String cpf) {  
        this.cpf = cpf;  
    }  
  
    public Paciente getResultado() {  
        return new Paciente(nome, email, cpf);  
    }  
}
Na classe "PacienteBuilder" nós podemos ver que foi adicionado um novo bloco, aquele bloco eh essencial para o funcionamento do builder, ele eh o responsável por realmente criar um objeto para nós.
analisando esse bloco, podemos ver que ele retorna um novo "Paciente()", ele criar um novo objeto "Paciente()" a partir dos parâmetros que foram passados a ele, isso quer dizer que ele vai criar um novo objeto seguindo os seguintes parâmetros (nome, email, cpf).
Com esses parâmetros que passamos na hora da criação do paciente dentro do builder o "getResultado()" vai ter uma função de extrema importância para a criação e acesso dos objetos criados a partir do builder.
~~~

~~~Java
ARQUIVO MAIN "BuilderTeste"

package br.com.mainpatterns.patterns.builders;  
  
public class BuilderTeste {  
    public static void main(String[] args) {  
        PacienteBuilder builder = new PacienteBuilder();  
        builder.setNome("Igor");  
        builder.setEmail("igor@gmail.com");  
        builder.setCpf("123456789-10");  
  
        Paciente igor = builder.getResultado();  
        System.out.println(igor.getEmail());  
    }  
}
Vejamos aqui que a forma de instanciar um novo objeto paciente foi alterada, ao invés de passarmos tudo dentro de uma única linha num único parentêses nós começamos criando um objeto remetente ao builder.
Logo na primeira linha podemos observar que instanciamos um objeto usando a classe do builder e não do "Paciente".
Usando o "builder." nós conseguimos passar os parâmetros exatamente como se estivessemos usando a instanciação de um new object normal, porém agora passando cada método separadamente dentro do arquivo da classe bulder e não da classe de origem de onde vem a instancição do objeto "Paciente".
Perceba que depois disso nós chamamos a nossa classe "Paciente" e damos um nome a variável, após isso chamamos o objeto que criamos (nesse caso, com o nome "builder") e depois passamos o "getResultado", este termo tem a relação direta com a variável que criamos anteriormente, note que chamamos a classe "Paciente", depois passamos um nome pra ela, após isso chamamos novamente o objeto "builder" e usamos o método "getResultado()", isso quer dizer que nós fizemos com que o paciente "Igor" recebesse da classe Builder "getResultado" sendo essa parte fundamental porque ela que faz com que a variável que acabamos de criar tenha uma instanciação do "getResultado()", tendo em mente que o "getResultado()" retorna o nome, email e o CPF do paciente, assim fazendo com que o "builder.getResultado()" seja armazenado dentro do nome "igor" da classe "Paciente".
~~~

Desse jeito nós conseguimos criar um builder que criar automaticamente um objeto quando passado os parâmetros a ele, depois armazenamos essas informações e o objeto numa variável para que possamos retirar as informações dela através do "getResultado()".


-----------------------------------------------------------------


## 25: Singleton

O "Singleton" eh um padrão de projeto criacional, ele permite que você garanta que uma classe tenha apenas uma instância enquanto provê um ponto de acesso global para essa mesma instância. Digamos que temos um banco de dados, quando nós temos o "Singleton" podemos chamar esse padrão para que não seja preciso instanciar novamente o banco de dados, quando essa instância está sendo usada ela retorna algo e diz que está ocupada.

Vamos ver um exemplo mais prático agora, digamos que temos um banco de dados e que nós queremos que esse banco de dados seja fechado, após uma vez instanciado ele não possa mais ser instanciado, para isso nós devemos usar o "Singleton" da seguinte maneira:

~~~Java
ARQUIVO QUE FINGE SER UMA DATABASE DE CONEXÃO
  
package br.com.mainpatterns.patterns.singleton;  
  
public final class Connection {  
    private  static Connection instance;  
    public String database;  
  
    private Connection(String database) {  
        this.database = database;  
    }  
  
    public static Connection getInstance(String db_usage) {  
        if (instance == null) {  
            instance = new Connection(db_usage);  
        }  
            return instance;  
    }  
}
Neste código aqui temos um exemplo de um "Singleton", podemos observar que ele recebe um final, isso significa que ninguém pode herdar essa classe.
Temos um método chamado "instance", ele eh o responsável por analisar se o nosso banco de dados existe ou não e assim teremos dois caminhos, sendo eles:
SE o banco de dados NÃO existir com o (instance == null) ele vai criar um novo objeto chamado "Connection", sendo que esse objeto recebe o método "db_usage"
SE NÃO ele vai retornar o "instance" que ela e como se fosse o nosso banco de dados.
~~~

~~~Java
ARQUIVO MAIN

package br.com.mainpatterns.patterns.singleton;  
  
public class ConnectionTester {  
    public static void main(String[] args) {  
        Connection connection = Connection.getInstance("Usuários 1");  
        Connection connection2 = Connection.getInstance("Usuários 2");  
  
        System.out.println(connection.database);  
        System.out.println(connection2.database);  
    }  
}
E no arquivo main nós temos justamente o uso prático do "singleton", note que nós chamamos a classe "Connection" e criamos duas variáveis e essas duas variáveis chamam a função "getInstance", após isso o "db_usage" dessa mesma função recebe o "Usuário 1" para o primeira variável e "Usuário 2" para a segunda variável.
No println podemos observar que nós chamamos as duas variáveis, entretanto como estamos falando de um "singleton" o retorno desse println vai ser sempre "Usuário 1" pq nós criamos ele e o "singleton" vai sempre manter ele justmente por ser uma classe final também.
Nós podemos imaginar o "singleton" como uma variável final enorme, porém nós criamos uma classe específica somente para algo em específico e está variável não pode ser alterada, retornando sempre o mesmo valor que foi passada a ela originalmente.
~~~


-----------------------------------------------------------------


## 26: Strategy

O padrão "strategy" eh um padrão comportamental, ele permite que uma família seja definida de algarismos, sendo colocados em classes separadas e fazendo objetos deles intercambiáveis.

Vamos supor que temos um Google Maps da vida, ele mostra o mapa mundi, restaurantes no mundo inteiro, lojas e tudo mais, ele também tem uma função muito usada que faz o calculo de rotas que o usuário escolhe um ponta A e um ponto B e vê qual a rota mais fácil e rápida no mapa. Na primeira versão ele fazia as rotas somente sobre as rodovias, porém com o crescimento da aplicação mais meios de transporte foram adicionados, fazendo disso um método construtor enorme, um código gigantesco e com muitas dores de cabeça e cada vez que você adicionava um novo algoritmo de roteamento, a classe principal do navegador dobrava de tamanho. Em determinado momento, o monstro se tornou algo muito difícil de se manter e qualquer mudança a um dos algoritmos afetava toda a classe, aumentando a chance de criar um erro no código já existente.

O padrão "strategy" sugere que você pegue uma classe que fez algo específico várias vezes de maneiras diferentes (ou não) e extraia todos esses algarismos para classes separadas. A classe original deve delegar um trabalho ao "strategy" ai invés de executá-lo por conta própria.

A classe principal não é responsável por selecionar um algoritmo apropriado para o trabalho. Ao invés disso, o cliente passa a estratégia desejada para a classe principal. Na verdade, a classe principal não sabe muito sobre as estratégias ("strategy"). Ele trabalha com todas elas através de uma interface genérica, que somente expõe um único método para acionar o algoritmo encapsulado dentro da estratégia selecionada.

Desse jeito nós descartamos a necessidade de um código grande, separando o mesmo por partes, ajudando na manutenção e entendimento do código para facilitar alterações sem quebrar outras partes do código.

Agora nós vamos usar um exemplo de uma plataforma de e-commerce. Digamos que temos uma loja online onde ela aceita somente pagamentos por cartão de crédito, porém com o crescimento dessa loja ela vai precisar aceitar outros tipos de pagamento como pix, boletos, parcelas(...), nós não podemos colocar isso tudo na mesma classe e por isso nós vamos separar as classe usando o padrão "strategy".

Vamos começar visualizando o problema, assim:

~~~Java
ARQUIVO DA CLASSE "Compra"

package br.com.mainpatterns.patterns.strategy;  
  
public class Compra {  
    private int valor;  
  
    public Compra(int valor) {  
        this.valor = valor;  
    }  
  
    public int getValor() {  
        return valor;  
    }  
  
    public void setValor(int valor) {  
        this.valor = valor;  
    }  
  
    public String processar_compra(int tipo) {  
        if (tipo == 1) {  
            System.out.println("Compra realizada no débito. Valor total: " + valor);  
        }  
        if (tipo == 2)  {  
            System.out.println("Compra realizada no crédito. Valor total: " + valor);  
        }  
        if (tipo == 3) {  
            System.out.println("Compra realizada no pix. Valor total: " + valor);  
        }  
        return "";  
    }  
}
Aqui nós já podemos começar a visualizar o problema, temos um uma funcionalidade que tem várias possibilidades dentro dessa função, agora imagine que essa função é muito maior onde por exemplo o tipo 1, que é o débito, ele vai receber várias regras já o tipo 3 que, é o Pix, vai receber outros tipos de regras, onde vai ser mais barato do que o tipo 1 por exemplo. Quando isso acontece nós temos um código que fica extremamente grande e poluído, por isso que é muito importante usar esse padrão "strategy".
~~~

Agora vamos ver como podemos fazer para aplicar o padrão "strategy" dentro desse nosso código.

~~~Java
ARQUIVO DA INTERFACE "EstrategiaCompra"

package br.com.mainpatterns.patterns.strategy;  
  
public interface EstrategiaCompra {  
    void pagar(int valor);  
}
Nesta interface podemos observar que oq estava no método construtor (neste caso, o "valor") veio parar aqui também, esse contrato que criamos na interface deve ser colocado em todas as classes que implementarem do mesmo. No nosso caso as classes que vão implementar essa funcionalidade vão ser as classes que recebem os métodos de pagamentos e suas regras (sendo eles o crédito, débito e o pix), essa interface recebe o método "valor", ele eh o responsável por perguntar ao usuáiro o valor da compra, e dependo da forma de pagamento usado os resultados serão diferentes porém concluido um mesmo objetivo.
~~~

~~~Java
ARQUIVO DA CLASSE "Compra"

package br.com.mainpatterns.patterns.strategy;  
  
public class Compra {  
    private int valor;  
  
    public Compra(int valor) {  
        this.valor = valor;  
    }  
  
    public int getValor() {  
        return valor;  
    }  
  
    public void setValor(int valor) {  
        this.valor = valor;  
    }  
  
    public void processar_compra(EstrategiaCompra estrategiaCompra) {  
       estrategiaCompra.pagar(valor);  
    }  
}
Na classe compra nós podemos ver que temos um método construtor, esse mesmo método recebe o "valor" junto de um getter e um setter.
Observando a função "processar_compra" vemos que ela não retorna nenhum valor por ser um void. Nós chamamos a função da nossa interface e a partir dela nós instânciamos um método que eh o responsável por fazer o processo dessa compra, essa função vai ter como principal funcionalidade receber os valores no arquivo main, para que a lógica seja efetuada dentro das classes que implementam a interface e na classe "Compra" que repassa essas informações conforme o usuário as dita.
~~~

Abaixo veremos as regras para os três tipos de pagamentos possíveis para efetuar as compras, todos seguem a mesma lógica e por isso vou poupar explicações de um por um.

~~~Java
ARQUIVO DA CLASSE "CompraCredito"
package br.com.mainpatterns.patterns.strategy;  
  
public class CompraCredito implements EstrategiaCompra{  
  
    @Override  
    public void pagar(int valor) {  
        System.out.println("Compra realizada no crédito. Valor total: " + valor);  
    }  
}
Aqui nós temos a lógica da compra caso ela seja no Crédito, onde uma mensagem própria seria enviada ao usuário informando o método de pagamento e o valor total, toda a lógica de pagamento no Crédito deve ficar aqui.
~~~

~~~Java
ARQUIVO DA CLASSE "CompraDebito"

package br.com.mainpatterns.patterns.strategy;  
  
public class CompraDebito implements EstrategiaCompra{  
  
    @Override  
    public void pagar(int valor) {  
        System.out.println("Compra realizada no débito. Valor total: " + valor);  
    }  
}
~~~

~~~Java
ARQUIVO DA CLASSE "CompraPix"

package br.com.mainpatterns.patterns.strategy;  
  
public class CompraPix implements EstrategiaCompra{  
    @Override  
    public void pagar(int valor) {  
        System.out.println("Compra realizada no pix. Valor total: " + valor);  
    }  
}
~~~

E agora veremos como podemos efetuar a compra desses no arquivo "Main"

~~~Java
ARQUIVO MAIN "CompraTeste"

package br.com.mainpatterns.patterns.strategy;  
  
public class CompraTeste {  
    public static void main(String[] args) {  
        Compra celular = new Compra(1570);  
        Compra camiseta = new Compra(80);  
  
        celular.processar_compra(new CompraCredito());  
        camiseta.processar_compra(new CompraPix());   
    }  
}
Por fim nós temos o arquivo Main, ele eh o responsável por efetuarmos a compra, para que seja possível usarmos as classes e suas lógicas que criamos anteriormente.
Podemos observar que nós instânciamos duas variáveis com a classe "Compra", sendo elas um "celular" e uma "camiseta", para que seja possível criamos a compra ele deve ser instânciado como um objeto e por isso existe um new ali, isso quer dizer que vamos criar um novo objeto a partir da classe compra e dentro dos parentêses vamos passar o "valor" dessa mesma compra.
Após isso nós chamamos os objetos que acabamos de criar e usando a função "processar_compra" dentro de seus parâmetros nós criamos outro objeto, esse objeto tem a função de dizer qual o método de pagamento utilizado para pagar o produto.
~~~


-----------------------------------------------------------------


## 27: Collections Framework - List

"Collections Framework" nada mais eh do que um conjunto de pacotes, podendo trabalhar com listas, objetos e etc. 

Falando sobre o "List", ele nada mais eh do que uma interface que traz inúmeras opções de uso que podemos ver deixando o mouse em cima do nome "List" nós podemos ver todas as suas funcionalidades e o que eles retornam. 

Vejamos abaixo um exemplo (incompleto) de como o básico da instância de uma "List" funciona, assim:

~~~Java
ARQUIVO MAIN "ListTeste"

package br.com.collectionframework.util.collection;  
  
import java.util.ArrayList;  
import java.util.List;  
  
public class ListTeste {  
    public static void main(String[] args) {  
        List lista = new ArrayList();  
        lista. // as opções dos comandos de uso dessa "list" vão aparecer aqui
    }  
}
Neste código simples (incompleto) podemos observar como funciona o básico de uma lista e como elas normalmente são instânciadas da maneira mais básica.
A linha de código que contém o "List lista = new ArrayList();" quer dizer básicamente que dentro da interface "List" estamos, vamos criar um objeto com o nome "lista" que vai receber uma "ArrayList()", isso quer dizer que a partir de uma interface nós demos origem ao objeto "lista". É literalmente a implementação da interface "List" usando o "ArrayList()".
O "lista." eh para exemplificar as funções que podemos usar após a criação desse objeto, que infelizmente só eh possível visualizar numa IDE.
~~~

#### Algumas funções do "list": 
- add()
	- Usado para adicionar itens a uma lista, todos os itens adicionados numa lista a partir do "add()" serão considerados como objetos para o Java.

- addAll()
	- A função "addAll()" que serve para adicionar todos a lista todos os itens passados como parâmetro ao mesmo.

- remove()
	- Temos o "remove()" que faz exatamente o que sugere, o "remove()" pode remover objetos ou um número inteiro, tendo em vista que o número inteiro faz referência ao índice do elemento em relação a sua posição da lista. O usa das aspas dentro do "remove()" faz referência ao nome do objeto que está dentro da lista, isso quer dizer que se tem um objeto chamado "Laranja" dentro desta lista, dentro do "remove()" devemos passar entre aspas o exato nome do objeto que queremos remover.

- clear()
	- Ele serve para limpar todos os elementos de uma lista, a tornando uma lista totalmente vazia, seu retorno seria apenas os colchetes vazios.

- get()
	- Funcionando também como o uso de números inteiros do "remove()", o "get()" também recebe um número inteiro dentro dos parâmetros, ele pode ser combinado com variáveis por exemplo. 

- contains()
	- Servindo para verificar se existe aquele objeto dentro da lista, como ele retorna um valor boleano ele precisa estar dentro de uma variável para que seja possível observar seu retorno, todos os caracteres, letras maiúsculas, espaços devem ser IGUIAS a como foram inseridas posteriormente dentro da lista.

- isEmpty()
	- Também retornando um valor boleano, ele diz se a lista está com algum objeto ou não, caso a lista esteja vazia o seu retorno será "true", se ela estiver com qualquer objeto independentemente da quantidade, seu retorno será igual a "false".

- set()
	- Recebendo o índice de um objeto, ele permite que você modifique um objeto já existente na lista, permitindo que o item do índice XX com o argumento YY, se eu passar o índice do elemento YY e substituir o argumento desse índice o valor do índice XX vai mudar a vai passar a valer ZZ por exemplo.

- size()
	- Responsável por retornar o valor do tamanho da lista, vai sempre retornar um valor inteiro. Diferente do índice que começa a contar a partir do 0, o "size()" contar a partir do 1. 


-----------------------------------------------------------------


### 27.1: Collections Framework - List (Tipagem e Lista de objetos)

As listas quando não são passadas as especificações de qual tipo de dado aquela lista vai armazenar ela acaba aceitado todo tipo de dado. Para que isso não aconteça, nós podemos fazer uma lista tipada para que ela só receba um tipo de dado específico que desejarmos. 

para podermos tipar uma lista, devemos abrir os sinais de maior ou menor (<>) antes de declararmos o nome da lista e depois dentro destes mesmos sinais devemos passar o tipo de dado que a lista vai armazenar e depois de passarmos a declaração do objeto construtor, assim:

~~~Java
ARQUIVO DA CLASSE "ListTeste"

package br.com.collectionframework.util.collection;  
  
import java.util.ArrayList;  
import java.util.List;  
  
public class ListTeste {  
    public static void main(String[] args) {  
        List<String> lista = new ArrayList<String>();
        lista.add("Olá, mundo!") 
    }  
}
Deste jeito, essa lista só vai aceitar dados que sejam strings, qualquer outro tipo de dado que não seja uma string vai quebrar o código. O mesmo vale também para os outros tipos de dados, sejam eles int, double e etc.
~~~

O uso de classes e objetos para listas também eh possível, nós criar classes e objetos dentro da nossa própria lista, podemos dizer que a tipagem daquela lista só vai aceitar dados provenientes da classe que lhe foi passada posteriormente. Eh um pouco mais complexo do que parece, vejamos o exemplo a seguir:

~~~Java
ARQUIVO DA CLASSE "Pessoa"

package br.com.collectionframework.util.collection.list;  
  
public class Pessoa {  
    private String nome;  
    private int idade;  
  
    public String getNome() {  
        return nome;  
    }  
  
    public void setNome(String nome) {  
        this.nome = nome;  
    }  
  
    public int getIdade() {  
        return idade;  
    }  
  
    public void setIdade(int idade) {  
        this.idade = idade;  
    }  
  
    public Pessoa(String nome, int idade) {  
        this.nome = nome;  
        this.idade = idade;  
    }  
}
Nesta classe aqui nós temos a criação das características do objeto pessoa, no método construtor dessa pessoa nós podemos ver que ela recebe dados básicos, sendo eles o "nome" e a "idade", eles devem ser passados antes de criarmos um objeto desta classe. Tanto o "nome" e a "idade" recebem getters e setters.
~~~

~~~Java
ARQUIVO DA CLASSE "ListTeste"

package br.com.collectionframework.util.collection.list;  
  
import java.util.ArrayList;  
import java.util.List;  
  
public class ListTeste {  
    public static void main(String[] args) {  
        Pessoa igor = new Pessoa("Igor", 18);  
        Pessoa mari = new Pessoa("Mari", 18);  
        Pessoa clara = new Pessoa("clara", 15);  
        Pessoa ihara = new Pessoa("Ihara", 40);  
        Pessoa emanuel = new Pessoa("Emanuel", 37);  
  
        List<Pessoa> users = new ArrayList<Pessoa>();  
  
        users.add(igor);  
        users.add(mari);  
        users.add(clara);  
        users.add(ihara);  
        users.add(emanuel);  
  
        for (Pessoa usuario:users) {  
            System.out.println(usuario.getNome());  
            System.out.println(usuario.getIdade());  
        }  
    }  
}
Nesta classe aqui nós criamos 5 objetos a partir da classe "Pessoa", percebemos que cada um recebeu seu "nome" e a "idade", sendo eles de tipos de dados diferentes (String e int respectivamente). Nós criamos uma lista que o seu tipo de dado eh da classe "Pessoa", isso quer dizer que essa lista só vai aceitar objetos que estejam de acordo com as norma impostas sobre a classe "Pessoa", caso contrário vai dar erro.
Após a criação dos objetos e a criação da lista a partir do "Pessoa", nós adicionamos os 5 objetos recém criados dentro da lista "users" usando o "add()".
O for faz com que essa lista seja apresentável e legível, isso quer dizer que para pessoa usuario (no singular) vai percorrer (represtado pelo uso do ":") a lista "users", os dois println vão acessar o "usuario" criado neste for (lembrando q este "usuario" está percorrendo a lista "users") e vão pegar o "nome" e "idade" de cada um dos objetos criados a partir da classe "Pessoa".
~~~


-----------------------------------------------------------------


### 27.2: Collections Framework - Set

O "set()" estende do "collection" como o "list()". O "set()" tem as mesmas características da interface que regra o "collection".

O "set()" também cria uma lista, porém diferente do "list()" que permite a adição de vários objetos o "set()" permite a adição de somente um objeto, isso faz com que ela não permita que sejam adicionados dois objetos iguais numa lista.

Como ele estendo da interface que regra o "list()", podemos criar o "set()" da mesma maneira que o "list()", podemos também definir o tipo de dado que aquela lista única vai receber, da mesma maneira que o "list()".

Após declararmos o "new" quando vamos criar uma lista nova, podemos ver q automaticamente são sugeridos duas principais funções, sendo elas o "HashSet" e o "TreeSet", sendo que o "HashSet" tem uma performance melhor em relação ao "TreeSet".

Já citado anteriormente, o "set()" também trabalha com as mesmas funções do "list()", isso quer dizer que podemos usar o "clear()", "add()" e etc. O "remove()" tem uma exceção, já que dentro do "set()" para podermos remover um objeto nós não podemos remover o objeto pelo índice e sim somente pelo nome do objeto.

Uma das características próprias do "set()" tá a sua capacidade de auto organização, ou seja, ele eh capaz de ajustar os valores. Vamos supor que temos uma lista que só aceita Strings e dentro desta lista temos os valores: "Igor", "Mari" e "Clara" nesta sequencia e usando o println nós chamamos essa lista, o seu retorno será: Igor, Clara, Mari. Vejamos um exemplo:

~~~Java
ARQUIVO DA CLASSE "setTeste"

package br.com.collectionframework.util.collection.set;  
  
import java.util.HashSet;  
import java.util.Set;  
  
public class SetTeste {  
    public static void main(String[] args) {  
        Set<String> nomes = new HashSet<String>();  
  
        nomes.add("Igor");  
        nomes.add("Mari");  
        nomes.add("Clara");  
  
        System.out.println(nomes);  
    }  
}
Neste código aqui podemos observar que criamos uma lista a partir do "Set", falamos que ela só aceita Strings e seu nome eh "nomes".
Podemos observar que também criamos uma lista usando o "Set" e o "HashSet" já que ele tem um desempenho melhor que a outra opção que citamos anteriormente.
Após isso, adicionamos três objetos dentro dessa lista, sendo eles três nome que não seguem nenhuma sequencia.
O println vai ser o responsável por escrever no terminal oq tem dentro dessa lista, ea está fora de qualquer ordem, porém como eh uma das características do "Set()" esta lista vai automaticamente se organizar em alguma sequência.
~~~


-----------------------------------------------------------------


### 27.3: Collections Framework - Map

O "map" tem a função de mapear uma lista onde foi definido as chaves que definem aquela lista. O método "map" tem algumas diferenças em relação aos dois outros que vimos antes, um diferença bem importante eh que o "map" tem a função "KeySet()" e ela se faz fundamental para o "map()". O uso do "HashMap()" e o "TreeMap()" também se vê presente no uso do "map()" como o do "set()", sendo o "HashMap()" tendo um desempenho melhor.

Para criar um lista "map()" se faz do mesmo jeito do que as outas duas que vimos antes, onde nós criamos a lista do mesmo jeito que instanciamos um nono objeto. Assim:

~~~Java
ARQUIVO DA CLASSE "MapTeste"

package br.com.collectionframework.util.collection.map;  
  
import java.util.HashMap;  
import java.util.Map;  
  
public class MapTeste {  
    public static void main(String[] args) {  
        Map<String, String> mapa = new HashMap<String, String >();  
    }  
}
Aqui nós podemos observar como funciona a criação de uma lista "map()", note que ele recebe dois argumentos dentro dos sinas de maior e menor (<>) já que isso faz parta da sua criação como objeto.
~~~

A instanciação do "map()" deve conter esse operador (<>) com os dois argumentos por conta do jeito que o mesmo trabalha, pois ele funciona com a chaves, ou seja, isso quer dizer que o primeiro argumento String diz que a chave identificadora eh uma String e o conteúdo que essa chave está relacionada também eh uma String, eh como se fosse uma lista numerada onde primeiro passamos o tipo de dado da chave e após isso passamos o tipo de dado do valor a ser adicionado na lista. Uma outra informação relevante eh que nós não podemos passar tipos primitivos diretos, o uso de uma String eh permitido porém o uso do int não, para isso devemos usar o "Integer" no lugar de onde ficaria o int.

A forma de adicionar itens a uma lista "map()" também muda, o comando para adicionar itens muda de "add()" para "put()". A forma de passar os argumentos dentro da lista também mudam, onde primeiro devemos passar a chave de identificação do objeto para depois passarmos o objeto em si. Vejamos o exemplo:

~~~Java
ARQUIVO DA CLASSE "MapTeste"

package br.com.collectionframework.util.collection.map;  
  
import java.util.HashMap;  
import java.util.Map;  
  
public class MapTeste {  
    public static void main(String[] args) {  
        Map<String, String> mapa = new HashMap<String, String>();  
  
        mapa.put("1", "Chaves");  
        mapa.put("2", "Kiko");  
        mapa.put("3", "Seu");  
        mapa.put("3", "Seu Madruga");  
  
        System.out.println(mapa);  
    }  
}
Neste código aqui nós temos um exemplo de como podemos adicionar itens a uma lista criada a partir do "map()". 
Observe que na linha onde criamos a lista ela recebe duas Strings dentro dos operadores de maior ou menor (<>), isso quer dizer que o tipo de dado da chave identificadora eh uma String e o objeto que vai estar dentro da lista também eh uma String.
Após isso podemos observar que usamos o ".put()" para adcionarmos quatro itens a lista, sendo que o primeiro tem sua chave de idntificação como "1" e o nome do obejto eh "Chaves", fizemos a mesma coisa para o segundo objeto também. A diferença entra quando nós usamos a mesma chave para dois objetos quase totalmente difderentes, neste caso o próprio "map()" tem a função de organizar os obejtos e como desta nós tinhamos a primera palavra igual no começo do nome ele concatenou com oq tinha no último ".put()". O input disso tudo seria portanto:
{1=Chaves, 2=Kiko, 3=Seu Madruga}
~~~

Como nós passamos uma chave de identificação para os objetos eles passam a não possuir mais um índice automático e sim o argumento que passamos para a chave, ou seja, se o objeto "Chaves" tinha o índice igual a 0 no "list()", ele dentro do "map()" (em referencia ao código que vimos acima!) vai passar a possuir o índice 1. Isso quer dizer que caso nós queiramos chamar algum objeto em especifico dentro de um get por exemplo, nós devemos passar o valor da chave de identificação e não o índice.

Existem outros pontos muito importantes a serem vistos dentro do map, sendo eles:

   - values()
	   - Nós sabemos que não podemos passar o println diretamente no "map()", porém com o "values()" podemos fazer isso se tornar possível. Com ele nós podemos fazer exatamente oq seu nome sugere, mostrar os valores do uma lista "map()", apresentando todos os nomes dos objetos que aquela lista possui.

- keySet()
	- Ele possui uma funcionalidade muito do "values()", porém ao invés de apresentar o nome dos objetos dentro da lista ele apresenta os valores das chaves em alguma ordem.

Agora veremos um código de exemplo para podermos visualizarmos melhor como funciona o "map()", observe:

~~~Java
ARQUIVO DA CLASSE "MapTeste"

package br.com.collectionframework.util.collection.map;  
  
import java.util.HashMap;  
import java.util.Map;  
  
public class MapTeste {  
    public static void main(String[] args) {  
        Map<String, String> mapa = new HashMap<String, String>();  
  
        mapa.put("1", "Chaves");  
        mapa.put("2", "Kiko");  
        mapa.put("3", "Seu");  
        mapa.put("4", "Seu Madruga");  
  
        System.out.println(mapa.values());  
  
        System.out.println(mapa.keySet());  
  
        for (String nome:mapa.values()) {  
            System.out.println(nome);  
        }  
    }  
}
Aqui nesse código podemos observar logo de cara que temos a criação de uma lista que recebe uma key String e um objeto q tbm eh uma String.
Após isso podemos observar que adcionamos 4 obejetos dentro dessa lista com o ".put()", dentro deles foram passados dois argumentos, o primeiro argumento eh a chave de identificação do objeto e depois temos o objeto em si.
Usamos um println para mostrar os valores (ou só os nomes) dos obejetos usando o ".values()" e outro println para apresentar as chaves de identificação de cada objeto usando o ".keySet()".
O método for serve para que nós possamos percorrer a lista, a variável nome dentro do for serve para armazenar os valores obtidos da lista que fizemos usando o "map()". Podemos interpretar isso assim:
nome = mapa.values()
e como isso está dentro do for nós pedimos para ele apresentar no terminal o "nome".
~~~


-----------------------------------------------------------------


## 28: Wrappers

O termo "String" eh um objeto, ele eh um conjunto de caracteres montado num objeto que recebe esse nome. Isso ocorre para que seja possível usarmos seus super poderes, um tipo primitivo de um conjunto de caracteres não pode ser manipulado como uma "String", pois todas as funções do "toUpperCase()" ou o "toLowerCase()" só existem pq foram criadas dentro da classe "String".

Aqui onde entra os "wrappers", eles que dão os superpoderes para esses tipos de dados, ele fornece as ferramentas para que seja possível transformar um tipo de dado primitivo simples em algo mais complexo com super poderes como nós vimos com a "String". Veja agora os "wrappers" de cada um dos tipos primitivos:

| Tipo primitivo | Classe Wrapper |
| -------------- | -------------- |
| boolean        | Boolean        |
| char           | Character      |
| byte           | Byte           |
| short          | Short          |
| int            | Integer        |
| long           | Long           |
| float          | Float          |
| double         | Double         |

Cada um desses wrappers tem funcionalidades e poderes diferentes para fins diferentes, um exemplo disso eh o "Integer", o "wrapper" do int. Ele contém várias funções junto dele, alguns exemplos são:

- floatValue()
	- Apresenta como seria aquele número inteiro num valor decimal.

- equals()
	- Deve ser passado dentro dos parênteses o valor que deseja sem comparado, caso o valor seja o mesmo o retorno será um boleano true, caso contrário vai retornar um boleano false.

- compareTo()
	- Faz exatamente oq o nome sugere, ele compara o valor da variável a qual foi atribuído com o valor passado dentro dos parênteses, veja a explicação mais detalhada dos possíveis retornos que ele pode dar:
		- 0 = os valores são iguais.
		- -1 = o valor do objeto q qual o "compareTo()" foi atribuído e menor em relação ao número q ele está sendo comparado.
		- 1 = o valor do objeto a qual o "compareTo()" está atribuído eh maior em relação ao número q ele está sendo comparado.

~~~Java
ARQUIVO DA CLASSE "WrapperTeste"

package br.com.collectionframework.util.wrappers;  
  
public class WrappersTeste {  
    public static void main(String[] args) {  
        Integer num1 = 10;  
        Integer num2 = 20;  
  
        System.out.println(num2.floatValue());  
        System.out.println(num1.equals(5));  
        System.out.println(num1.compareTo(num2));  
    }  
}
Aqui neste exemplo nós usamos os exemplo acima para que seja possível visualizarmos a aplicação deles num código real. 
~~~

O "Boolean" também não foge muito deste exemplo, ele também tem vários comando parecidos com o "Integer", como por exemplo o "booleanValue()", onde ele apresenta qual o valor boleano está armazenado dentro daquela variável.

O mesmo vale para o "Double" que também possui seus comando muito parecidos com os outro exemplo que vimos. Veja um outro exemplo:

~~~Java
ARQUIVO DA CLASSE "WrappersTeste"

package br.com.collectionframework.util.wrappers;  
  
public class WrappersTeste {  
    public static void main(String[] args) {  
  
        Boolean flag = true;  
        System.out.println(flag.booleanValue());  
  
        Double valor = 15.99;  
        System.out.println(valor.intValue());  
    }  
}
Neste exemplo nós apenas usamos alguns métodos simples de cada um dos "wrappers" dos exemplos que vimos antes, nada muito complexo e complicado de se compreender.
~~~
 
Usando os tipos "wrappers" ao invés dos tipos primitivos nós ganhamos muito mais flexibilidade, isso pode ser aplicado na criação de uma lista "map()" por exemplo, onde ao invés de passarmos a chave de identificação como "String" nós podemos usar o "Integer", assim permitindo criar uma lista numerada já que o "map()" não permite que possamos o tipo primitivo como chave identificadora.


-----------------------------------------------------------------


## 29: Lambda

Uma "lambda" permite a implementação rápida de uma função, ela serve para anular a criação de classes, métodos e etc. Eh válido lembrar que seu uso pode variar bastante e portanto devemos saber quando usar uma função lambda e quando não devemos usar ela.

A sintaxe de uma lambda não eh muito complexa, para que ela possa ser instanciada devemos fazer o seguinte código:

~~~Java
() -> {  
    }
~~~~

Para que uma "lambda" seja funcional ela precisa estar em uma variável que normalmente essa variável eh derivada de uma interface que o próprio Java/IDE nos sugere. Quando nós criamos uma "lambda" sem estar numa variável a IDE vai automaticamente sugerir que ela seja armazenada numa variável locar, essa variável local recebe a implementação de uma interface chamada "Runnable" e ela já vem pronta para uso, deixando assim uma "lambda" funcional. Veja um exemplo de como isso funcionaria:

~~~Java
ARQUIVO DA CLASSE "LambdaTeste"

package br.com.collectionframework.util.lambda;  
  
public class LambdaTeste {  
    public static void main(String[] args) {  
        Runnable runnable = () -> {  
            System.out.println("Olá, mundo!");  
        };  
        runnable.run();  
    }  
}
Neste código aqui observa-se que nós temos uma "lambda" que deriva de "Runnable", esse "Runnable" nada mais eh uma interface que dá a vida a nossa "lambda", ou seja, caso não não estejamos usando uma interface que nós mesmos criamos para dar vida a uma "lambda" nós obrigatoriamente precisamos dizer que essa "lambda" extende dessa interface.
Após dizermos de qual interface ela vao vim, nós podemos passar o nome da "lambda" e neste caso usei um nome padrão sugerido pela prórpia IDE.
Podemos observar a declaração da "lambda" a partir da variável que acabamos de criar, usamos a sintaxe que vimos anteriormente para criarmos a "lambda" passamos que sempre que ela for chamada ela vai escrever "Olá, mundo!" no terminal.
E por fim nós chamamos o nome da variável que guarda a nossa "lambda" e passamos o "run()" para que possamos forçar e execução dela.
~~~

Eh válido lembrar que as "lambdas" também são funções, isso significa que elas também podem receber parâmetros dentro do seus parênteses. 

Agora para usarmos uma "lambda" que recebe uma interface que nós mesmo criamos podemos fazer assim:

~~~Java
ARQUIVO DA CLASSE "LambdaTeste"

package br.com.collectionframework.util.lambda;  
  
interface TesteLambda {  
    public String executar(String texto);  
}  
  
public class LambdaTeste {  
    public static void main(String[] args) {  
        TesteLambda testeLambda = (String texto) -> {  
            return texto;  
        };  
        System.out.println(testeLambda.executar("Olá, mundo!"));  
    }  
}
Já podemos observar que criamos uma interface dentro da nossa classe, fizemos isso par agilizar o exemplo. Observe os parâmetros que essa interface recebe, olhe que ela recebe um comando "executar" e qualquer um que derivar dela vai precidar passar uma String como argumento.
Criamos uma "lambda" usando a nossa interface recém criada para podermos instanciar a variável que recebe a "lambda". Essa mesma "lambda" recebe a String que foi passado o uso obrigatorio na interface e essa mesma String recebe o nome de texto para que o return no final devolva oq foi passado como argumento desse praâmetro quando chamado esta função "lambda".
O println recebe a função de chamar a variável que contém a "lambda" e ai sim chamamos a função "executar" e passamos o parâmetro que essa fução pede (sendo ela o parâmetro texto, uma String).
~~~

Os jeitos de se usar uma "lambda" são muito variados. Um exemplo disso eh onde nós podemos usar uma "lambda" dentro do um "ForEach", lembra o jeito que usávamos para percorrer os objetos de uma lista usando o "for"? Agora eh possível fazer isso em três linhas de código apenas usando uma "lambda", veja o exemplo abaixo:

~~~Java
ARQUIVO DA CLASSE "LambdaTeste"

package br.com.javalearning.util.lambda;  
  
import java.util.ArrayList;  
import java.util.List;  
  
public class LambdaTeste {  
    public static void main(String[] args) {  
        List<String> usuarios = new ArrayList<String>();  
        usuarios.add("João");  
        usuarios.add("Maria");  
        usuarios.add("Pedro");  
  
        usuarios.forEach((usuario) -> {  
            System.out.println(usuario);  
        });  
    }  
}
Neste código podemos observar que temos a criação de uma lista simples, ela contém três objetos/usuários.
O diferencial desse código entra quando nos chamamos a lista "usuarios" e passamos um código chamado "forEach", essa função faz práticamente a mesma coisa de um for normal, entretanto a sua instanciação eh mais fácil e rápida. Dentro dos parâmetros da "lambda" nós criamos um método "usuario" sendo ele o responsável por ser a variável que armazena o nome de cada objeto, escreve no terminal e muda para o próximo objeto, repetindo o ciclo até acabat todos os usuários na lista. 
~~~


-----------------------------------------------------------------


## 30: Stream

Para o Java, uma stream é uma sequência de elementos de uma fonte de dados que suporta operações de agregação. As streams são uma abstração introduzida no Java 8 e permitem processar sequências de elementos de forma declarativa.

Podendo ser usada de vários jeitos diferentes, nós podemos criar listas "Stream" a partir de uma instanciação baseado numa outras lista, neste caso aqui vamos umae, observe o exeplo:

~~~Java
ARQUIVO DA CLASSE "StreamTeste"

package br.com.javalearning.util.stream;  
  
import java.util.ArrayList;  
import java.util.List;  
import java.util.stream.Stream;  
  
public class StreamTeste {  
    public static void main(String[] args) {  
        List<String> nomes = new ArrayList<String>();  
        nomes.add("Igor");  
        nomes.add("Mari");  
        nomes.add("Clara");  
  
        Stream<String> nomes2 = nomes.stream();  
    }  
}
Neste código nós fizemos a criação de uma lista simples usando o "List()", passamos junto dela três nomes também.
Após isso nós chamamos a "Stream" e pode-se dizer que criamos uma lista a partir da lista que nós já tinhamos usando o "list()".
~~~

Normalmente a "Stream" eh muito usada com as lambdas, eh muito frequente vermos uma "Stream" acompanhada de uma função "lambda", já que muitas vezes as ações a serem executadas precisam ser rápidas e não costumam serem complexas e por isso são criadas a juntos a uma "lambda".

Uma função lista permite que seja convertida para uma "Stream" e uma "Stream" pode ser convertida para uma lista, podemos ver isso com clareza neste código abaixo:

~~~Java
ARQUIVO DA CLASSE "StreamTeste"

package br.com.javalearning.util.stream;  
  
import java.util.ArrayList;  
import java.util.List;  
import java.util.stream.Stream;  
  
public class StreamTeste {  
    public static void main(String[] args) {  
        List<String> nomes = new ArrayList<String>();  
        nomes.add("Igor");  
        nomes.add("Mari");  
        nomes.add("Clara");  
  
        Stream<String> nomes2 = nomes.stream();  
  
        Stream<String> resultados = nomes2.filter(nome -> nome.startsWith("Mari"));  
        System.out.println(resultados.toList());  
    }  
}
Neste código nós criamos uma lista usando o "List()", colocamos três objetos dentro dessa mesma lista. Após isso nós pegamos essa mesma lista e a transformamos numa "Stream()" e demos o seu nome de "nomes2".
Por fim criamos uma "Sream()" a partir de uma outra "Stream()" sendo ela a responsável por analisar quais nomes começam com a letra M dentro do "nomes2".
Usando o println para chamamos o "resultado" da nossa análise nós solicitamos que os resultados dessa análise fosse retornado como uma lista por conta da função "toList()". 
~~~ 

O uso da  "Stream" eh extremamente vasto, podemos misturar ela com as "Lambdas" e muito mais, vejamos um exemplo a baixo de como podemos fazer isso:

(tenha em mente que temos uma classe pessoa que recebe nome e sobrenome, os dois possuem getters e setters)

~~~Java
ARQUIVO DA CLASSE "StreamTeste"

package br.com.javalearning.util.stream;  
  
import java.util.ArrayList;  
import java.util.List;  
import java.util.stream.Stream;  
  
public class StreamTeste {  
    public static void main(String[] args) {  
        Pessoa igor = new Pessoa("Igor", "Gonçalves");  
        Pessoa mari = new Pessoa("Mari", "Luiz");  
        Pessoa clara = new Pessoa("Clara", "Silveira");  
  
        List<Pessoa> usuarios = new ArrayList<Pessoa>();  
        usuarios.add(igor);  
        usuarios.add(mari);  
        usuarios.add(clara);  
  
        Stream<Pessoa> usuariosStream = usuarios.stream();  
  
        Stream<String> resultado = usuariosStream.map(usuario -> {  
            return usuario.getNome() + " " + usuario.getSobrenome();  
        });  
  
        System.out.println(resultado.toList());  
    }  
}
Aqui nós criamos três objetos e cada um desses objetos recebe um seu "nome" e "sobrenome". Observe que todos os três objetos foram adicionados e respectivamente cada um recebeu seu nome.
Todos os três usuário foram adicionados numa "ArrayList" e após isso todos os usuário foram foram embuidos no método "stream()".
A última "Stream" foi para que todos os usuários passasem numa lista ".map", criamos uma "lambda" que pega cada usuário e o adiona numa variável "usuario", após isso ela concatena o "nome" e "sobrenome" do usuário e o retorna no terminal, quando esse processo termina ela pula para o próximo usuário e faz a mesma coisa até que não tenha mais nenhum usuário disponivel, finalizando o loop.
~~~


----------------------------------------------------------------- 


## 31: JavaIO - Reader

O termo "JavaIO" significa input e output, ele trabalha com entradas e saídas dos programas. Vamos começar com o "reader", ele faz a leitura de coisas. Veja o exemplo de como começar a instanciação de um "reader":

~~~Java
package br.com.javalearning.util.io.reader;  
  
import java.io.FileInputStream;  
import java.io.FileNotFoundException;  
  
public class InputTeste {  
    public static void main(String[] args) throws FileNotFoundException {  
        FileInputStream arquivoTXT = new FileInputStream("caminho do arquivo aq");  
    }  
}
Neste código nós criamos podemos ver a base de como instanciar a criação de um "reader()", podemos observar que ele tem a função "throws", ela serve para retornar uma mensagem de erro caso o arquivo não seja encontrado, se vendo obrigatório seu uso.
Eh notável também vermos que a criação de um "reader()" se parece bastante com a criação de uma lista ou algum objeto.
~~~

Quando nós passamos um "reader" e o atribuímos a uma variável, aquela variável passará a conter as informações dos bytes do arquivo que está lendo, e não seu conteúdo por si só. Para que isso não ocorra nós usamos um método chamado "InputStreamReader" junto do método "read()", assim:

~~~Java
ARQUIVO DA CLASSE "InputTeste"

package br.com.javalearning.util.io.reader;  
  
import java.io.FileInputStream;  
import java.io.IOException;  
import java.io.InputStreamReader;  
  
public class InputTeste {  
    public static void main(String[] args) throws IOException {  
        FileInputStream arquivoTXT = new FileInputStream("src/teste.txt");
          
        InputStreamReader arquivoTrad = new InputStreamReader(arquivoTXT);  
  
        System.out.println(arquivoTrad.read());  
    }  
}
Aqui nós podemos ver como funciona a criação do arquivo, podemos observar que para que o arquivo a ser lido foi parar dentro da instanciação do "InputStreamReader", criado como um objeto e dentro dos parâmetros foi passado o nome da variável que contém esse arquivo a ser lido.
No println nós podemos observar que usamos o método "read()" para ver os dados contidos no arquivo que queremos ler.
~~~

Entretanto, infelizmente não é tão simples assim a leitura dos arquivos, o println vai retornar o número 79, esse número representa o primeiro caractere presente no arquivo que está sendo lido, caso outro println com o "read()" seja implementado ele vai passar o número do segundo caractere presente no arquivo que está sendo lido e assim por diante. Para que seja possível a leitura desse arquivo nós devemos usar a função "BufferedReader", ele é literalmente um reader melhorado como seu nome sugere, ele eh instanciado da mesma maneira dos métodos que vimos até agora, assim:

~~~Java
ARQUIVO DA CLASSE "InputTeste"

package br.com.javalearning.util.io.reader;  
  
import java.io.BufferedReader;  
import java.io.FileInputStream;  
import java.io.IOException;  
import java.io.InputStreamReader;  
  
public class InputTeste {  
    public static void main(String[] args) throws IOException {  
        FileInputStream arquivoTXT = new FileInputStream("src/teste.txt");  
  
        InputStreamReader arquivoByte = new InputStreamReader(arquivoTXT);  
  
        BufferedReader arquivoFinal = new BufferedReader(arquivoByte);  
  
        System.out.println(arquivoFinal.readLine());  
    }  
}
Desse jeito nós conseguimos fazer com que seja possível a leitura de uma linha do arquivo de texto que pedimos para ser lido para nós. Caso nós passasemos mais um "readLine()" é mais uma linha que vai ser lida, da mesma forma que o "read()"
~~~

Para que seja possível nós possível lermos completamente um arquivo e lermos o que ele armazeno nós podemos usar o método "while", desse jeito:

~~~Java
ARQUIVO DA CLASSE "InputTeste"

package br.com.javalearning.util.io.reader;  
  
import java.io.BufferedReader;  
import java.io.FileInputStream;  
import java.io.IOException;  
import java.io.InputStreamReader;  
  
public class InputTeste {  
    public static void main(String[] args) throws IOException {  
        FileInputStream arquivoTXT = new FileInputStream("src/teste.txt");  
        InputStreamReader arquivoByte = new InputStreamReader(arquivoTXT);  
        BufferedReader arquivoFinal = new BufferedReader(arquivoByte);  
  
        String BRLinha = arquivoFinal.readLine();  
  
        while (BRLinha != null) {  
            System.out.println(BRLinha);  
            BRLinha = arquivoFinal.readLine();  
        }  
    }  
}
Deste jeito nós conseguimos fazer com que seja possível a leitura de todas as linhas do arquivo que queremos ler, criamos uma variável que contém o "readLine()", após isso fizemos uma função while, ela dize que enquanto a variável "BRLinha" foi diferente de nulo ela vai escrever uma linha e depois passar pra próxima linha e sobre escrevendo, sendo a "RLinha = arquivoFinal.readLine();" dentro do while responsável por sobreescrever a linha que já foi apresentada a nós.
~~~


-----------------------------------------------------------------


### 31.1: JavaIO - Writer

Como seu nome sugere, o "writer" eh capaz de escrever escrever coisas. Ele também eh instanciado como um objeto de uma maneira muito parecido com o "Reader", veja o exemplo de como o instanciar:

~~~Java
package br.com.javalearning.util.io.writer;  
  
import java.io.FileWriter;  
import java.io.IOException;  
  
public class WriterTeste {  
    public static void main(String[] args) throws IOException {  
        FileWriter fileWriter = new FileWriter("caminho do arquivo a ser escrito");  
    }  
}
Desse jeito nós podemos fazer a criação básica do um "Writer", muito parecido com o "Reader()", não?
~~~

Da mesma maneira que vimos no "Reader()" onde ele possuí o "BufferedReader" nós temos o "BufferedWriter" dentro do "Writer", ele faz exatamente o que sugere, ele eh capaz de escrever nos arquivos, vejamos o exemplo:

~~~Java
ARQUIVO DA CLASSE "WriterTeste"

package br.com.javalearning.util.io.writer;  
  
import java.io.BufferedWriter;  
import java.io.FileWriter;  
import java.io.IOException;  
  
public class WriterTeste {  
    public static void main(String[] args) throws IOException {  
        FileWriter fileWriter = new FileWriter("src/teste.txt");  
        BufferedWriter bufferedWriter = new BufferedWriter(fileWriter);  
  
        bufferedWriter.write("Usei o Java para escrever isso!");   
        bufferedWriter.close();  
    }  
}
Dsse jeito nós conseguimos escrever dentro de um arquivo usando o Java, de uma maneira muito parecida com o "Reader" nós fomos capazes de escrever algo novo. 
Tenha em mente que a função "write()" sobrescreve o que já tem no arquivo e o "close()" se vé obrigatório seu uso, pense nele como se fosse para salvar as alterações feitas pelo "write()".
~~~

Para que algo novo seja adicionado sem que com sobre escreva o que já está no arquivo alvo, nós devemos usar a função "append()" além de informamos se ele vai poder ser adicionado itens a ele ou não, assim:

~~~Java
ARQUIVO DA CLASSE "WriterTeste"

package br.com.javalearning.util.io.writer;  
  
import java.io.BufferedWriter;  
import java.io.FileWriter;  
import java.io.IOException;  
  
public class WriterTeste {  
    public static void main(String[] args) throws IOException {  
        FileWriter fileWriter = new FileWriter("src/teste.txt", true);  
        BufferedWriter bufferedWriter = new BufferedWriter(fileWriter);  
  
        // bufferedWriter.write("Usei o Java para escrever isso!");  
  
        bufferedWriter.append("\nUsei o Java para escrever isso!");  
        bufferedWriter.close();  
    }  
}
Desse jeito nós somos capazes de adicionarmos itens novos a um arquivo.
Veja que existe o "true" junto do caminho do arquivo, ele quer dizer que podemos adicionar itens sem sobre escrever o que já está presento no arquivo, caso ele fosse um "false" ele iria sobre escrever o que está presento no arquivo alvo.
O \n serve apenas para dizer que o que vem a seguir dele vai ser escrito numa nova linha, caso contrário ele iria escrever ao lado do que está presente no arquivo.
~~~


-----------------------------------------------------------------


## 32: Generics

Vamos pegar o exemplo de uma lista qualquer, ela pode conter dentro do sinais de maior e menor(<>) o tipo de dado que ela vai receber, podendo ser uma String, Long e etc. Nós também podemos usar o termo para dizer que ela vai ser genérica, normalmente se usa o termo "E" para dizer que ela eh genérica, podemos até mesmo passar dois genéricos a uma única classe.

Os métodos genéricos são usados quando nós não sabemos o tipo de dado que vai vim, nós não sabemos se ele vai ser uma String, ou inteiro ou até mesmo um boleano, nestes casos nós usamos o termo genérico. Vamos ver um exemplo:

~~~Java
ARQUIVO DA CLASSE "Objeto"

package br.com.javalearning.util.generic;  
  
public class Objeto<E> {  
    private E nome;  
  
    public Objeto(E nome) {  
        this.nome = nome;  
    }  
  
    public E getNome() {  
        return nome;  
    }  
  
    public void setNome(E nome) {  
        this.nome = nome;  
    }  
}
Aqui nós podemos ver como funciona o método genérico e sua instanciação nos construtores, getters e setters. Ele básicamente substitui onde ficaria a tipo de dado pela letra "E", ela que informa que tipo de dado eh genérico neste caso.
~~~

Ele se torna menos controlador, ele se adapta automaticamente conforme o tipo de dado que ela recebeu, como nesse exemplo aqui:

~~~Java
ARQUIVO DA CLASSE "GenericTeste"

package br.com.javalearning.util.generic;  
  
public class GenericTeste {  
    public static void main(String[] args) {  
  
        Objeto<String> letra = new Objeto<String>("Mari");  
  
        Objeto<Integer> numero = new Objeto<Integer>(5);  
          
        Objeto<Boolean> truefalse = new Objeto<Boolean>(false);  
    }  
}
Aqui podemos observar que a partir da classe "Objeto" nós criamos três objetos com tipos de dados diferentes, isso devido ao tipo genérico que foi passado na classe que estamos usando de instancia para esses objetos.
~~~


-----------------------------------------------------------------
## 33: Observações Importantes

No intelliJ podemos usar o "sout" para escrever automaticamente "System.out.println();", poupando assim tempo sem precisar escrever
mais do que o necessário

Ainda no intelliJ, nós podemos escrever a abreviação "psvm", ele eh uma abreviação para esse bloco que vamos usar bastante:
~~~Java
public static void main(String[] args) {  
    }

~~~
lembre-se que esse código serve para que uma classe seja executável, sem esse bloco de códigos uma classe não pode ser executada.

Para fazer uma quebra de linhas dentro de um "println" usamos o "\n" dentro do próprio "println", como se o "\n" fosse parte do texto.

Usando o atalho "alt+ins" podemos criar getters, setter, constructors...selecionando os que desejamos criar automaticamente

Quando uma classe recebo o "final" ela automaticamente se torna uma classe que não pode ser extendida/herdada. Assim:

~~~Java
public final class Connection {  

    }
~~~

Quando uma "lambda" está dentro de um parênteses de algum outro comando e ela só tem um único parâmetro a necessidade de usar os parenteses para passar os métodos da "lambda" se anula e só vai ser necessário seu uso novamente caso a "lambda" receba mais de um método.
 

-----------------------------------------------------------------