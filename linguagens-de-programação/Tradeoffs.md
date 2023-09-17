

-> Dois critérios que são conflitantes, são a **confiabilidade** e o **custo de execução** 

	-> Um exemplo pode ser Java, que exige uma verificação de todas as referencias
	aos elementos de um vetor sejam feitas para garantir que os indíces estejam em
	suas faixas legais. Esta verificação adiciona um custo de execução de um
	programa que contenha um grande numero de referencias aos elementos de um vetor

	-> Já em C, nós não temos a exigencia da verificação da faixa de indíces, desta
	forma programas semanticamente iguais rodam mais rápido em C.



-> Facilidade de escrita x Redigibilidade

	->Um exemplo é APL que tem um conjunto muito grande operadores para matrizes. E
	como existe um grande numero de operadores, foi necessário um grande numero de
	símbolos. Além disso, esses operadores podem ser escritos em sentenças longas e
	complexas o que resulta num alto grau de expressividade para operações com
	matrizes, facilitando assim a escrita porém deixando a legibilidade pobre, pois
	uma grande computação pode ser escrita com poucos elementos