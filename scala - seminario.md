
### Scalable Langugage 

-> Tipagem: estática, forte e inferida
-> tem um propósito geral
-> type-safe
-> incorpora recursos funcionais e de orientação a objetos

-> feita para ser concisa e a maioria das escolhas de projeto foram feitas para criticar java:
	
	-> sobrecarga de operadore ( + / - ) - são usado de fomra
	não numerica somente para concatenação de string. Perde com
	implementação de objetos matematicos como numeros complexos
	e matrizes
	
	-> concorrencia falha:ava's thread-based concurrency model
	can be error-prone. Scala offers a more advanced concurrency
	model through libraries like Akka, which uses actors for
	concurrent and distributed programming. 
	
	-> Boilerplate code 
	
	-> falta de tuplas


- O código pode ser compilado para JavaByecode e rodar na JVM
- Também pode ser compilado no Scalajs para javascript, para ser executado num navegador.
- Tem interoperabilidade com java, onde bibliotecas escritas numa linguagem podem ser referenciadas na outra

#### Caraterísticas funcionais

- inferencia de tipos
- nested functions
- currying
- imutabilidade
- lazy-evaluatuig
- pattern-matching
- Além de suporte a tipos avançados:
	- tipos anonimos
	- sobrecarga de operadores
	- parametros opcionas


-> Scala não tem variáveis estáticas nem metodos. Ela tem *singleton objects*, que são basicamente classes com só uma instancia 

![[Pasted image 20230912205919.png]]

-> não faz distinção entre expressões e declarações. Todas as declarações são de fato expreessões que são avaliadas para um valor.
	
	->funções que são declaradas como void em C e Java, e declarações como While que logicamente não retornam um valor, em Scala são retornada com o tipo Unit, que é um singleton type.

	-> funções e operadores que nunca retornam como um todo, (throw) retornam o tipo Nothing, um tipo especial que não contém objetos 

como uma declaraçãp é também uma expressão, nós temos coisas do tipo
![[Pasted image 20230912211412.png]]