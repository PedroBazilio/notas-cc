

- Ciências -> Fortran
- Empresarial -> Cobol
- IA -> Lisp
- Sistemas -> C
- Web -> Js/PHP

# 1 - Critérios para Avaliação de Linguagens

1. [Legibilidade](/linguagens-de-programação/legibilidade) 
2. [Redigibilidade](/linguagens-de-programação/redigibilidade)
3. [Confiabilidade](/linguagens-de-programação/confiabilidade)
4. [Eficiência](/linguagens-de-programação/eficiencia)
5. [Facilidade de Aprendizado](/linguagens-de-programação/facilidade-aprendizado)
6. [Ortogonalidade](/linguagens-de-programação/ortogonalidade)  polimorfismo, uso de operadores para diferentes sem perdas
7. [Reusabilidade](/linguagens-de-programação/reusabilidade)
8. [Modificabilidade](/linguagens-de-programação/modificabilidade)
9. [Portabilidade](/linguagens-de-programação/portabilidade)


Usuarios focam na redigibilidade e facilidade de escrita enquanto projetistas focam no elegancia e a na chance de atrair novos usuarios. Essas características entram em conflito


##### [Tradeoffs no Projeto de Linguagens](/linguagens-de-programação/Tradeoffs) 



##### [Compilação](/linguagens-de-programação/Compilação) 


##### [Interpretação](/linguagens-de-programação/interpretação) 



### Resumo:

-> Os critérios mais importantes são legibilidade, redigibilidade, confiabilidade e custo geral.

<hr>

# 2 - Nomes, Vinculações e Escopos


#### 2.1 - Nome (*Identificador*):

###### Questões de Projeto:

	-> O nome é sensível a capitalização?
	-> As palavras especiais da linguagem são reservadas?

###### Formato dos nomes:

- A sensibilidade a capitalização é considerada para algumas pessoas uma perda para a legibilidade, porque os nomes que se parecem atualmente são entidades diferentes:
	-> Ex.: **rosa, Rosa e ROSA**

- Porém, por outros é considerada um problema de redigibilidade pois é necessário lembrar da capitalização específica o que pode tornar mais dificil uma escrita correta do código.

###### Palavras especiais:

- **Palavra-chave:** é uma palavra especial usada apenas em alguns contextos. 

- **Palavra reservada:** é uma palavra especial que não pode ser usada como um nome(*identificador*)

* **Possíveis  Problemas:** 
	-> Caso existam muitas palavras reservadas, o usuário tem dificuldade para criar nomes que não sejam reservados


#### 2.2 Variáveis:


###### Variáveis são as abstrações para as células da memória


##### Variáveis são caracterizadas por uma coleção de atributos:

- **nome:** 
	-> tratado acima

- **endereço:**
	-> é o endereço da memória ao qual ela está associada
	-> quando mais de uma variável pode ser usada para acessar o mesmo endereço da memória, são usado os *alias*, eles são um problema para a legibilidade pois permite que variável mude o valor a partir de outra
	-> o uso de apelidos torna a verificação de programas mais difícil

	 
- **valor:**
	-> é o conteúdo das células de memória associadas a ela

- **tipo:**
	->  o tipo determina a faixa de valores que uma variavel pode armazenar e o conjunto de operações definidas para valores deste tipo 

- **tempo de vida:**


- **escopo:** 

##### 2.2.1 Vinculações:

- **Duas coisas importantes sobre a vinculação são como o tipo é especificado e quando a vinculação ocorre**

###### **Vinculação Estática:** 
-> é quando ela ocorre antes do tempo de execução e permanece intocada ao longo da execução

###### **Vinculação Dinâmica:** 
-> é quando ocorre em tempo de execução ou pode ser mudada ao longo do curso da execução do programa