## 1: Introdução

O SprigBoot permite que a criação de projetos meio que prontos, ele faz com que não seja necessário fazer um projeto totalmente do zero, ele faz com que seja possível cortar muito tempo de trabalho. Ele é capaz de criar micro serviços, REST API e muitos mais.


----------------


## 2: Configurando um projeto Spring Boot

No site oficial do [Spring Initializr](https://start.spring.io/) nós podemos montar o começo de um projeto que usa o SpringBoot, ele fornece várias ferramentas de inicialização para nosso projeto, podendo até mesmo fazer a pré-instalação de dependências do nosso projeto, algumas IDE podem fazer a inicialização a partir dela mesma, porém o intelliJ na versão gratuita não é capaz de fazer isso. 
O Java por padrão utiliza o gerenciador de dependências Maven, ele faz com que seja possível a instalação de bibliotecas externas e suas dependências. 
Na escolha de versão do Spring, SEMPRE escolha a versão estável, jamais opte por versões da Snapshot ou M1.
Geralmente usamos o grupo de pacotes invertido para os metadados do nosso projeto, como nós já vimos antes. Um exemplo disso seria:
br.com.exemplodenome.apirest
Para a escolha do artefato e o nome geralmente colocamos o mesmo nome para não nos perdermos, a descrição fica aberta a qualquer coisa, o mesmo vale para o nome do pacote, colocamos o mesmo nome do grupo por questões de organização.
O pacote usamos o Jar, ele diz a versão do sistema quando queremos subir essa aplicação em algum servidor.
A versão do Java fica aberta a escolha, ela vária demais de acordo com as necessidades do seu projeto.

As dependências são essências num projeto Spring, elas podem ser alteradas a qualquer momento. As mais usadas são o Sring Web, JPA e o Lombok. 


---------------------


## 3: Conceitos de API REST

Uma REST API é um conjunto de instruções que determina como se comunicar com uma aplicação, isso faz com que ela possa ser consumida por outras aplicações. Uma API também podem se comunicar com outras, como se fosse uma rede gigantesca, uma espécie de trabalho terceirizado. 

Na prática, podemos criar uma API para se comunicar com o Front End, ou seja, é o Back End se comunicando com o Front End.

O termo REST quer dizer:
Representational State Transfer
ou seja, eh um conjunto de restrições de arquitetura para o uso de uma API.

A organização de uma API REST tem algumas etapas, sendo alguns deles:
- Coleção de recursos: Os dados manipulados de uma API são chamados de recursos e estes recursos são agrupados em coleções.
- Identificador de Recursos: Cada recurso possui um identificador único e imutável.
- Representação de Recursos JSON: JSON é uma representação para representar estes mesmos recursos.

Digamos que temos uma API para uma biblioteca, vamos identificar a organização desta API:
#### Coleção e Recursos:
- Livro: Recurso.
    - Listagem de livros: Coleção.
- Cada Recurso tem um identificador único e imutável, usado para obter informações específicas de cada recurso individualmente.
	- Neste exemplo, podemos ter uma coleção de autores e cada um destes autores possuem uma coleção de livros.

#### Manipulação da Coleção de Recursos:
- Numa requisição HTTP podemos definir os métodos(verbos) para indicar ima ação a ser realizada no recurso.
	- GET /livros: Utilizamos o verbo GET para listar os recursos contidos numa coleção;
	
	- GET /livros/3: Também usando o GET para acessar um recurso específico;
	
	- POST /livros: Usando para adicionar um novo recurso numa coleção;
	
	- PUT /livros/12: O verbo PUT é usado para alterar completamente um recurso numa coleção;
	
	- PATCH /livros/12: Também serve para atualizar um recurso numa coleção, porém alterando somente uma parte específica do recurso ao invés de recurso completo;
	
	- DELETE /livros/17: Deleta por completo um recurso dentro de uma coleção.

#### Códigos de respostas HTTP
- Status Code:
	Em cada resposta de uma requisição HTTP utilizamos um código para informar o status da solicitação. Em uma requisição HTTP pode ser bem sucedida ou não e por isso usamos códigos de respostas para um sucesso ou um erro na requisição, como no try e catch. Existe também códigos informativos para o redirecionamento, porém não usamos em respostas de uma API's REST.
	- Exemplos de um Status Code:
		- 2xx: Sucesso, tudo oq está entre 100 até 299 indica um sucesso de solicitação.
		- 4xx: Erro do cliente, tudo que está entre 400 até 499 indica que a solicitação do cliente foi recebida, porém, possui erros.
		- 5xx: Erro do servidor, tudo q está presente entre 500 até 599 indica um erro interno inesperado no servidor.

	Códigos de série 2xx:
		200: OK
			requisição bem sucedida
				Caso essa requisição seja de criação ela NÃO deve retornar o 200 e sim o 201!
		201: Created
			requisição bem sucedida e algo foi criado;
		204: No Content
			requisição bem sucedida porém não contém conteúdo no corpo da resposta.
	
	Códigos da série 4xx:
		400: Bad Request
			O servidor não entendeu a requisição pois está com uma sintaxe inválida.
		401: Unauthorized
			O usuário não está autenticado.
		403: Forbidden
			O usuário não ter a permissão necessário para acessar o recurso solicitado.
		404: Not Found
			O servidor não pode encontrar o recurso solicitado.

	Códigos da série 5xx:
		500: Internal Server Error
			O servidor encontrou uma situação com a qual não soube lidar ou um erro inesperado.


---------------------


## 4: endpoint

Quando temos um projeto com Spring nós usamos os "controllers", eles controlam as operações que aquela API tem. Usando o exemplo da API para a biblioteca podemos criar os controladores para adicionar livros, pesquisar livros, deletar livros e etc.

Um método de definirmos que um arquivo vai ser responsável por ser um controlador é passar a annotation
@RestController
aplicamos essa annotation acima da classe responsável por esse controle, veja o exemplo:

~~~java
package br.com.igsolutions.apirest.apiRest.controllers;  
  
import org.springframework.web.bind.annotation.RestController;  
  
@RestController  
public class TesteController {  
  
}
~~~
desse jeito nós informamos que essa classe se torna um controlador.

Para que nós possamos passar um endpoint para uma classe (um endpoint é pode ser um http//loja/produtos, o "produtos" vira o endpoint) nós usamos a annotation:
@RequestMapping()
dentro dos parenteses nós informamos o endpoint que desejamos passar vejamos o exemplo:

~~~java
package br.com.igsolutions.apirest.apiRest.controllers;  
  
import org.springframework.web.bind.annotation.RequestMapping;  
import org.springframework.web.bind.annotation.RestController;  
  
@RestController  
@RequestMapping("/teste")  
public class TesteController {  
  
}
~~~
assim, no "localhost//8080/teste" temos o nosso caminho do endpoint passado.

Para q possamos fazer o retorno do controlador usamos outra annotation, sendo ela:
@GetMapping
lembre-se que existe outros tipos de annotations, neste caso essa é apenas um simples GET como vimos anteriormente. Veja o exemplo prático:

~~~java
package br.com.igsolutions.apirest.apiRest.controllers;  
  
import org.springframework.web.bind.annotation.GetMapping;  
import org.springframework.web.bind.annotation.RequestMapping;  
import org.springframework.web.bind.annotation.RestController;  
  
@RestController  
@RequestMapping("/teste")  
public class TesteController {  
  
    @GetMapping  
    public String teste() {  
        return "Olá, mundo!";  
    }  
}
~~~
ou seja, quando nós usamos o postman passando um GET no endpoint "teste", teremos um retorno de uma String, sendo ela "Olá, mundo!". Podemos ver isso no postman quando passamos o "http//localhost:8080" junto do endpoint "/teste", assim:

![[postman ola mundo.png]]
desse jeito, temos um controller dentro do nosso projeto e com o endpoint no /teste, podemos usar o postman para vermos esse endpoint ou podemos ver diretamente no navegador.


---------------------


## 5: Conexão com banco de dados PostgreSQL

IMPORTANTE
Nesta seção vamos ver uma conexão com a database PostgreSQL, porém a mesma coisa pode ser efetuada para outros tipos de databases (mySQL por exemplo).

Antes de qualquer coisa para que seja possível adicionarmos uma database a um projeto devemos primeiro adicionar sua dependência dentro do "pom.xml", após a adição da dependência podemos atualizar o projeto maven podemos dar continuidade.

Quando nós adicionamos um database a algum projeto nós devemos adicionar ela nas propriedades da configuração já que ele é o responsável por fazer a conexão com o banco de dados da aplicação.

no !application.properties" nós adicionamos as seguintes funções:

~~~properties
spring.jpa.hibernate.ddl-auto=uptade  
spring.datasource.url=jdbc:postgresql://localhost:5432/apirestjava  
spring.datasource.username=postgres  
spring.datasource.password=postgres
~~~
vamos entender cada uma delas com a explicação passo a passo
- spring.jpa.hibernate.ddl-auto=update  
	Essa linha é responsável por fazer com que a aplicação manipule o banco de dados sempre que alguma alteração em uma tabela for feita.
-  spring.datasource.url=jdbc:postgresql://localhost:5432/apirestjava  
	- spring.datasource.url
			informa a URL de conexão
	- jdbc:postgresql
			o tipo de banco de dados que estamos usando, sendo que nesse caso é o "postgresql"
	- localhost:5432/apirestjava  
			o local onde esse banco de dados está 
	- spring.datasource.username=postgres  
	- spring.datasource.password=123456
			define a senha e o usuário para esse banco de dados


---------------------


# 







---------------------











---------------------
