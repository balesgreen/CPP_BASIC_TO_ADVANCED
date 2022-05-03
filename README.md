# C++ BASICO AO AVANÇADO

<strong>A minha ideia neste livro é transformar a mente dos desenvolvedores C++ em uma fonte de verdade, onde será atribuído uma resposta a todos os "por que?" de cada dúvida sobre C++. Esse livro é destinado a todas as pessoas que não renunciaram ao conhecimento e mesmo nessa grande barafunda que é o mundo, ainda conseguem dedicar o próprio tempo para estudar.
 <br>
 <br>
 Ass: Rafael Romão (Mark Security)</strong>

 <h3>Tópicos</h3>
 
  * Entendendo a estrutura principal do programa C++
  * Entendendo variáveis e declarações condicionais
  * Operadores matemáticos
  * Operadores lógicos


  <h2>Entendendo a estrutura principal do programa C++</h2>
  
  <img src="https://imgur.com/velYOuH.png">
  
  ```cpp
  
  #include <iostream>
  ```
   * Essa função nos permite incluir em nosso código algumas bibliotecas para que possamos utilizar funções disponibilizadas por elas. A biblioteca padrão do C++ é conhecida como IOSTREAM (fluxo de entrada e saída). Essa biblioteca é muito importante para utilizarmos alguns objetos de fluxos globais, como por exemplo: cout, cin, cerr, clog, werr, wcin, etc..."

 ```cpp
 using namespace std;
 ```
 
  * A funçao using namespace std é essencial para evitarmos o uso de identificadores como <code>std::</code> em nosso código. Um desses exemplos é o seguinte: <code> std::cout << "Hello world" << std::endl;</code>

 ```cpp
 int main() {
 
 return 0;
 }
 ```
 
 * Essa função é essencial para os nosso programas em C++. A main é onde ficará toda estrutura do nosso programa e é pela main que é identificado por onde começa e termina o nosso programa.

<code>Bom, podemos fazer uma pequena anatomia da nossa estrutura main e compreendermos de uma forma mais elaborada sobre o nosso programa.</code>

 * 1 Por que a main se inicia como um int?
 * 2 Por que ela se chama main?
 * 3 Por que ela termina com o return 0?

1 - <code> Bom, a nossa main se inicia com int pelo fato de que o nosso return ou será 0 (true) ou será false (1). Esses dois números são considerados números inteiros, ou seja... o motivo de usarmos o int no inicio da nossa main é porque o nosso identificador return ou ele será 0 ou ele será 1 que são dois números inteiros.</code>

2 - <code> A tradução de main é algo como "principal", ou seja, ela é basicamente o vetor principal de nosso código, é por ela que o compilador reconhecerá onde o nosso programa se inicia. </code>

3 - <code> O motivo é o mesmo da resposta número 1... pois o valor de 0 em C++ tem valor de true e 1 tem valor de false, portanto só saberemos se o nosso código deu certo caso o retorno for igual a 0 e se algo deu errado, caso o retorno for 1.</code>

```cpp
 cout << "Hello world" << endl;
```

 * Essa parte do nosso código nos mostra o famoso "Olá mundo" que é bastante utilizado como representação do nosso primeiro programa escrito em determinada linguagem de programação. Podemos fazer a anatomia desse pequeno parâmetro de código.
    * <strong>cout</strong> = essa é a função que determina ao nosso programa que iremos imprimir mensagens no nosso console/terminal. Essa mensagem seja ela colocada por nós ou imprimida por meio de um valor de uma variável atribuida por nós.
    * <strong><<</strong> = Conhecido como operadores de deslocamento bit a bit, informa ao nosso programa que terá uma saída de dados (output).
    * <strong>"Hello world"</strong> = essa é a mensagem que será imprimida em nossa tela. Essa mensagem foi inserida manualmente, portanto conseguimos inserir valores de variáveis para serem imprimidos em nosso console. (veremos sobre isso logo, logo.)
    * <strong>endl</strong> = determina o nosso programa que após a execução da mensagem, será pulado uma linha para criar espaçamento entre objetos.

<br>

O resultado de exeução do nosso programa é:
<br>
<img src="https://imgur.com/6yvFhQz.png">


  <h2>Entendendo variáveis e declarações condicionais</h2>
  
  <img src="https://imgur.com/VHhYxNl.png" />
  
  ```cpp
    int inteiro = 10;
    float flutuante = 1.0;
    char caracter = 'C';
    string strings = "Hello world";
    bool TorF = false;
    double doublen = 10000000;
 ```
<strong> Bom, vamos compreender então o que cada variável nos quer mostrar e o como elas funcionam.</strong>
<br>
 * <strong>Int</strong> - Essa variável é chamada de variável do tipo inteiro. Essa variável sempre será atribuída a valores númericos de 0 (um) ao 9 (nove), ou seja, é determinada somente para números puros (sem pontos e vírgulas.)
 * <strong>Float</strong> - Essa variável é chamada de variável do tipo ponto flutuante, pois todos os seus valores númericos são trabalhados com pontos, como por exemplo: 3.1415.
 * <strong>Char</strong> - Essa variável é chamada de variável do tipo caractere, ou seja, utiliza-se letras para se atribuir valores as variáveis do tipo char.
 * <strong>String</strong> - Essa variável é chamada de variável do tipo referência, ou seja, contém um endereço de objeto. Normalmente é utilizada para expressar mensagens com grandes valores de letras.
 * <strong>Bool</strong> - Essa variável é chamada de variável do tipo booleana, ou seja, contém apenas duas sintaxes atribuídas a ela: true or false, 1 or 0. Muito eficiente para ser utilizada em situações como tentar validar se algo é verdadeiro ou falso.
 * <strong>Double</strong> - Essa variável é chamada de variável do tipo double porque ela armazena números de ponto flutuantes, com precisão dupla, ou seja normalmente possui o dobro de capacidade de uma variável do tipo float.

 ```cpp
    cout << inteiro << endl;
    cout << flutuante << endl;
    cout << caracter << endl;
    cout << strings << endl;
    cout << TorF << endl;
    cout << doublen << endl;
```

Aqui nós estamos imprimindo em nosso terminal/console todas as informações que foram atribuídas as nossas variáveis.

<h3>Técnicas utilizando o casting em C++</h3>

Você pode utilizar algumas formas de mudar valores usando o método de casting. Bom, mas o que seria o Cast? O Cast é basicamente uma função que nos permite mudar valores de variáveis sem que precisamos mudar o seu tipo em seu escopo.

```cpp
int valor = 100 // Sabemos que essa variável é do tipo inteiro (int) como foi explicado logo acima e estou atribuindo a ela um valor que é 10.

cout << valor;  // Aqui estou imprimindo em meu console o valor desta variável que no caso é 10.
```
Caso eu queira que o valor dela seja retornado como 100.000... sem que eu mude em seu escopo de definição do tipo de variável, eu apenas adiciono a função (float) na frente da variável que está sendo chamada em cout: <code>cout << (float)valor; </code>

<img src="https://imgur.com/62IYOXq.png" /> 
<br>
<img src="https://imgur.com/Q7xEY1q.png" />
<strong>OBS: Aqui eu estou usando o printf() da biblioteca <stdio.h> pois o meu cout estava gerando um bug.</strong>
 
 
# Operadores matemáticos
 
 Irei abordar sobre os operadores matemáticos no C++ e isso poderá facilitar a forma de lidar com problemas de multiplicação, divisão, substração e adição no dia a dia de vocês.
 
 **Bom, são quatro operadores matemáticos que existem no C++, fora o operador de restos mas que não será falado nesse tópico.**
 
 <img src="https://imgur.com/60qQ41W.png">
 
 Podemos utilizá-los de diversas formas em nosso código, mas como padrão, farei uma pequena calculadora para que seja representado de forma eficaz utilizando todos os operadores matemáticos ao mesmo tempo.
 
 Resultado:
 <img src="https://imgur.com/bG3YyAw.png">

 
# Operadores lógicos

 Os operadores lógicos ou operadores aritméticos são elementos que trabalham com operações juntos das variáveis. Os operadores lógicos sempre trabalharão com o corportamento de true (1) ou false (0). Representarei abaixo em códigos e mostrarei as diversas formas de se utilizar esses operadores. Antes disso, vamos conhecer quais são e que funções eles atribuem ao nosso código.
 
 * <code>><code> (Maior que)
 
