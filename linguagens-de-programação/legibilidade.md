### Facilidade com que programas podem ser lidos e entendidos


-> A facilidade de manutenção está ligada diretamente a legibilidade dos programas


#### Características que contribuem para a legibilidade:

- Comentários
- Marcadores de Blocos
- Desvios Incondicionais
- Palavras reservadas




-> Um complicador para a legibilidade é a existência de muitas estruturas básicas numa linguagem.
-> Outro complicador pode ser a multiplicidade de recursos, ou seja, existe mais de uma possibilidade para realizar alguma operação.
	Ex. em java existem  4 maneiras de incrementar uma variável
		count = count + 1
		count += 1
		count++
		++count
-> Um terceiro complicador é a sobrecarga de operadores, onde um operador tem mais de um significado. Pois, apesar de ser útil, pode levar a uma diminuição da legibilidade caso seja permitido ao programador criar as suas próprias sobrecargas.
	Ex. Utilizar o símbolo de "+" tanto para adição de inteiros quanto para adição de pontos flutuantes. Esta sobrecarga simplifica a linguagem 