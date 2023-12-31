

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

###### **Tipagem Estática:** 

-> é quando ela ocorre antes do tempo de execução e permanece intocada ao longo da execução

	-> Declaração explícita: ocorre quando o tipo é definido pelo programador na
	declaração da variável

	-> Declaração implícita: é uma forma de associar tipos por meio de convenções
	padronizadas ao invés da declaração de tipos por sentença. Neste caso a
	primeira aparição da variável constitui sua declaração.

  * Declarações implícitas podem ser um problema para a confiabilidade da linguagem pois previnem a compilação de detectar alguns erros de programação e digitação.

###### **Tipagem Dinâmica:** 

-> é quando ocorre em tempo de execução ou pode ser mudada ao longo do curso da execução do programa.

- Neste caso a variável é vinculado a um tipo quando é atribuido um valor a ela numa sentença

- Fornece uma flexibilidade imensa ao programador. Exemplo: um programa que processos dados numéricos pode ser escrito de forma genérica para processar qualquer tipo de dado


- **Desvantagens:**

	-> Faz programas serem menos confiáveis, pois diminui a capacidade de detecção de erros do compilador

	-> Outra grande desvantagem é o custo. Pois, o custo para implementar a vinculação de atributos dinâmico, principalmente em tempo de execução. Além disso, cada variável tem que ter um descritor em tempo de execução associado a ela de forma a manter o tipo atual.




##### 2.2.2 Vinculações de armazenamento e tempo de vida:


###### Variáveis estáticas

- São vinculadas a células de memória antes da execução do programa e permanecem vinculadas a mesma célula até a finalização do programa

-> **Vantagens:** Eficiências
-> **Desvantagens:** redução da flexibilidade. não permite que programa tenham funções recursivas. O armazenamento não pode ser compartilhado por variáveis





###### Variáveis Dinâmicas de Pilha


criada quando sua sentença 
tipo estáticamente vinculado
pilha de tempo de execução


vantagens: cada cópia de um programa recursivo mantém a sua variável local

desvantagens: sobrecarga em tempo de execução, da alocação e liberação. acesso mais lento e funções que não podem ser sensíveis a histórico



###### Variáveis dinâmicas do monte explícitas


 monte -> heap
	 -> acesso rápido
	 -> desorganizado
acessáveis apenas por ponteiros

**desvantagens:** acesso somente por ponteiros, dificuldade de usá-los. custo de referencias as variáveis e a complexidade do gerenciamento de armazenamento


###### Variáveis dinâmicas do monte implícitas

vinculados ao armazenamento no monte somente quando valores são atríbuidos a elas.

Permite flexibilidade, códigos altamente genéricos.

**desvantagens:** sobrecarga em tempo de execução para manter todos os atributos das variáveis, perda de detecção de erros por parte do compilador








## Tipos de Dados


**Descritor:** é a coleção de atributos de uma variável. Numa implementação, o descritor é área na memória que armazena os atributos de uma variável. 
 
##### 1. Ponto Flutuante

- Modelam números reais, mas representações são aproximações para os valores verdadeiros

- Armazenados em binários, o que agrava o problema

- Perda de precisão em operações. A subtração de números muito próximos pde gerar um numero bem pequeno oq acarreta na perda de numeros significativos

**Float**: é o tamanho padrão, normalmente armazenado em 4 bytes
**Double:** Normalmente ocupa o dobro do tamanho e fornece o dobro do valor de tipos float.


##### 2. Decimal

-> Armazenam um número fixo de digitos, com o ponto decimal em uma posição fixa 

-> Armazenam precisamente valores numa faixa fixa


**Desvantagem:** 

	- a faixa de valores é restrita pois não são permitidos expoentes
	- representação na memória é custosa
	- Costuma ser um dígito por byte ou até dois dígitos por byte


##### Ponteiros

**Atribuir:** é o ato de apontar um ponteiro para um endereço da memória

**Desreferenciar:** é o ato de acessar o valor de uma varíavel

###### Problemas com ponteiros

- **1. Ponteiros Soltos**
	-> é um ponteiro que contém o endereço de uma variável da heap que já foi liberada
	![[Pasted image 20230926205211.png]]

	**Solução:** 
		1. A utilização de *lápides*, nas quais as variaveis da heap possuem uma célula especial, chamada de lápide que é um ponteiro para a variavel. quando uma variavel da heap é liberada, o ponteiro original aponta para a lápide que terá uma valor nulo, resultando assim num erro de acesso. Lápides são caras tanto em tempo quanto de espaço
		2. Existe *fechaduras e chaves*, que consiste nos ponteiros serem representados por conjuntos de chave valor (chave, endereço), onde a chave é um valor inteiro. Quando variaveis do monte são criadas, valores são associados a elas e a variavel de ponteiro correspondente. cada acesso verifica a chave e se não corresponder dá erro
		3. **A melhor solução para os ponteiros soltos é tirar a responsabilidade pela liberação de variáveis do programador**
###### 2. Variáveis da heap perdidas
	-> São variáveis que não estão mais acessíveis ao usuário.
	Ex. p1 aponta para a v1, p1 agora aponta para v2. Perdemos v1



##### Verificação de Tipos

**1. Tipagem Forte**
	-> é quando erros de tipo são sempre detectados
	-> não permite operações entre diferentes tipos sem antes realizar uma conversão explícita
	-> a coerção de tipos acarreta na perda da detecção de erros
	-> erros de tipo geralmente resultam em erros em tempo de compilação

- A coerção faz linguagens de tipagem forte perderem a verificação de erros.




### Expressões e Sentenças de Atribuição


#### Efeitos Colaterais

	-> Acontece quando uma função modifica um de seus parametros ou uma variavel
	global 
	a = 10
	b = a + fun(a)

-> Alargamento de inteiro para float é de alargamento mas pode vir a perder precisão pois o tipo float tem cerca de 7 bits de precisão, enquanto o tipo inteiro tem 9 dígitos.

#### Avaliação em curto-circuito

alguma multiplicação por zero
(13 * a) * (a + 2 + b)

alguma verificação AND

(a >= 0) && (b < 10)

possível erro caso n tenha curto-circuito
![[Pasted image 20230927204250.png]]