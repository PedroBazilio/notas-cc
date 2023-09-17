#### Um programa é dito confiável quando está de acordo com as suas especificações em qualquer situação.


##### Verificação de tipos

- É a execução de testes para detecter erros de tipo num programa  tanto por parte do compilador quanto durante a execução.

-> Em **tempo de execução** é caro, em **tempo de compilação** é mais desejável

-> Quanto mais cedo erros forem detectados, menos custoso é o custo dos reparos. Por isso o projeto de Java requer praticamente todas as verificações de tipo em tempo de compilação, quase eliminando os erros em tempo de execução.

	-> Um exemplo é uma linguagem que não verifica parametros de uma função em
	relação ao que foi passado a ela, podendo ocorrer assim problemas de tipo.

##### Tratamento de Exceções

- É a habilidade de um programa para interceptar erros em tempo de execução, tomar medidas corretivas e então continuar

##### Utilização de apelidos

- **Apelidos** são permitidos quando é possível ter mais de uma forma para se acessar uma variável ou um endereço na memória

- Amplamente aceito por várias linguagens que é um recurso perigoso

- Podem ser utilizados para resolver deficiências em relação a abstração de dados.


##### Legibilidade e Facilidade de Escrita

- Os dois influenciam na na confiabilidade. Um programa escrito numa linguagem que não oferece maneiras naturais para escrever um recurso, irá usar abordagens não convecionais o que pode causar a existir mais erros.

- Quanto mais fácil é escrever um programa, mais provável dele estar correto.

- A legibilidade afeta a confiabilidade tanto na escrita quanto na manutenção e no ciclo de vida do código. Programas difíceis de ler são difíceis de escrever e modificar

