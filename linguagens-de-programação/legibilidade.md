### Facilidade com que programas podem ser lidos e entendidos


-> A facilidade de manutenção está ligada diretamente a legibilidade dos programas


#### Características que contribuem para a legibilidade:

- Comentários
- Marcadores de Blocos
- Desvios Incondicionais
- Palavras reservadas
- Existência de de mecanismos adequados para definir tipos e estruturas de dados.

##### Legibilidade x Simplicidade

	-> Pode ser exposta pela existencia de linguagens que usam menos palavras
	reservadas, o que gera uma maior simplicidade porém prejudica a legibilidade


#### Características que prejudicam a legibilidade:


-> Um complicador para a legibilidade é a existência de muitas estruturas básicas numa linguagem.
-> Outro complicador pode ser a multiplicidade de recursos, ou seja, existe mais de uma possibilidade para realizar alguma operação.
	Ex. em java existem  4 maneiras de incrementar uma variável
		count = count + 1
		count += 1
		count++
		++count
-> Um terceiro complicador é a sobrecarga de operadores, onde um operador tem mais de um significado. Pois, apesar de ser útil, pode levar a uma diminuição da legibilidade caso seja permitido ao programador criar as suas próprias sobrecargas.
	Ex. Utilizar o símbolo de "+" tanto para adição de inteiros quanto para adição de pontos flutuantes. Esta sobrecarga simplifica a linguagem 

-> a possibilidade de palavras reservadas serem usadas livrementes como identificadores para variaveis


-> outro complicador é a existencia de palavras que possam ser usadas em mais de um contexto
	Isto pode ser visto com a palavra **static** em c onde, na declaração de uma variavel dentro de uma função ela significa que a variavel é criada em tempo de compilação, já se for usada numa variável fora de funções ela significa que a variavel só é acessivel no arquivo de sua definição