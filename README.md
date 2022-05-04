# C++ BASICO AO AVANÇADO

<strong>A minha ideia neste livro é transformar a mente dos desenvolvedores C++ em uma fonte de verdade, onde será atribuído uma resposta a todos os "por quês" de cada dúvida sobre C++. Esse livro é destinado a todas as pessoas que não renunciaram ao conhecimento e mesmo nessa grande barafunda que é o mundo, ainda conseguem dedicar o próprio tempo para estudar.
 <br>
 <br>
 Ass: Rafael Romão (Mark Security)</strong>

 <h3>Tópicos</h3>
 
  * Entendendo a estrutura principal do programa C++
  * Entendendo variáveis e declarações condicionais
  * Operadores matemáticos
  * Tomada de decisão, IF/ELSE e comando GOTO.
  * Operadores lógicos


  # Entendendo a estrutura principal do programa C++
  
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


  # Entendendo variáveis e declarações condicionais
  
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

# Técnicas utilizando o casting em C++

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
 
# Tomada de decisão IF/ELSE e comando GOTO.
 
 Bom, chegamos finalmente na parte onde se trabalha toda lógica de decisão em um programa de computador, independente da linguagem de programação, sempre existirá funções atribuídas a tomadas de decisões. Vejamos abaixo o código representando sobre este conteúdo.
 
 <img src="https://imgur.com/QzpaXEf.png">

Podemos fazer uma anatomia deste código e entender como ele funciona.
 
```cpp
 
int num;

num = 1;

if (num == 1) {
	cout << "Num é igual a 1!" << endl;
}
 
```
 
 * <code>int num</code> -> Está sendo declarado uma variável do tipo inteiro com nome de "num".
 * <code>num = 1</code> -> Está sendo declarado um determinado valor diretamente na variável "num".
 * <code>if (num == 1)</code> -> Nessa função, estamos verificando se num é igual a 1. Se essa verificação for verdadeira (true), ele irá executar a mensagem, mas caso for falso (false), o programa será fechado.
	
Execução:<br>
<img src="https://imgur.com/trtdeRU.png">
	
Bom, podemos observar que a mensagem foi exibida e por isso temos a certeza de que o valor de num era verdadeiro, caso contrário nada seria executado. Mas onde o else entraria nessa história? O ELSE é nada mais que uma função de (senão). Observe na imagem abaixo o else sendo utilizado.
	
<img src="https://imgur.com/XtXtJVK.png">
	
Observe que o valor de num agora foi alocado como 2, ou seja, um valor totalmente diferente do que está definido na nossa condição if(num == 1). Bom, vamos executar o nosso programa e vamos observar o que será feito.
	
<img src="https://imgur.com/NvBrznm.png">
	
Pode-se observar que a mensagem que foi exibida, é a que está dentro da condição else, pois caso a condição else não existisse, nada seria executado e simplesmente o programa seria parado. O que entende-se sobre isso, é que o if e else são duas condições com funcionalidades diferentes porém sempre trabalhando juntas. Se (<b>if</b>) a minha condição for verdadeira, execute o que há dentro de "if", senão (<b>else</b>) for verdadeira, execute o que há dentro de "else".
 
	
<h4>Comando Goto</h4>

A condição goto é bastante interessante quando se trata de fazer um loop em nosso programa. O que acontece, é que essa função nos permite reexecutar o nosso programa sem precisarmos executar um comando para que o nosso programa seja executado. Criei um pequeno programa de calculos de adição e mostrarei como exemplo para que vocês possam compreender de uma forma mais simples.
	
<img src="https://imgur.com/XkIwOA6.png">
	
Adicionei uma biblioteca chamada cstdlib, pois ela possui a função de <code>system()</code> para que eu possa utilizar o comando cls em meu console, para que depois da reexeução do programa, não fique ocupando espaço em meu console com impressões de execuções passadas.

Bom, a função goto entra diretamente logo depois das declarações de variáveis, chamado de <code>inicio:</code>. Na função de decisão if(), observa-se que há um comando chamado <code> goto inicio;</code>. Esse comando permite que ele volte até onde a minha primeira declaração foi feita, que no caso foi onde determinei a função <code>inicio:</code>.
	
<img src="https://imgur.com/HroTE7S.gif">
	
# Operadores lógicos

 Os operadores lógicos ou operadores aritméticos são elementos que trabalham com operações juntos das variáveis. Os operadores lógicos sempre trabalharão com o corportamento de true (1) ou false (0). Representarei abaixo em códigos e mostrarei as diversas formas de se utilizar esses operadores. Antes disso, vamos conhecer quais são e que funções eles atribuem ao nosso código.
 
 * <code> > (Maior que...) </code> Esse operador é utilizado para indicar que se determinado número for maior que outro, então será "true", mas caso for menor, será "false".<br>
 * <code> < (Menor que...) </code> Esse operador é utilizado para indicar que se um determinado número for menor que outro, então será "true", mas caso for maior, será "false".<br>
 * <code> != (Diferente de) </code> Esse operador é utilizado para indicar diferença entre dois valores. Se determinado valor for diferente de outro valor, então será "true", mas caso for igual, será "false".<br>
 * <code> >= (Maior ou igual a...) </code> Esse operador é utilizado para indicar que se um número for maior ou igual a outro número, então será "true", mas caso for menor ou não igual, será "false".<br>
 * <code> <= (Menor ou igual a...) </code> Esse operador é utilizado para indicar que se um número for menor ou igual a outro número, então será "true", mas caso for maior ou não igual, será "false".<br>
 * <code> == (Igual a...) </code> Esse operador é utilizado para indicar igualdade a um valor. Caso 1 for igual a 1, então será "true", mas caso 1 não for igual a 1, então será "false".<br>
  
Código (==):<br>
<img src="https://imgur.com/FHBScuZ.png">
 
Resultado:<br>
<img src="https://imgur.com/SaGptdG.png">

Foi declarado que x é igual a y, pois o valor que foi atribuído na variável x é o mesmo valor que foi atribuído na variável y.

<h1></h1>
	
Código (<):<br>
<img src="https://imgur.com/IvDsjbg.png">
	
Resultado:<br>
<img src="https://imgur.com/GNRUDOh.png">
	
Podemos observar aqui que o console imprimiu que x é menor que y, pois o valor que foi atribuído na variável x é menor que o valor que está atribuído na variável y.
	
<h1></h1>
	
Código (>):<br>
<img src="https://imgur.com/MsnUdUD.png">
	
Resultado:<br>
<img src="https://imgur.com/vAiaujA.png">
	
Uh! Parece que o resultado foi "false", pois ele não retornou a mensagem dizendo que x é maior que y. O valor que foi atribuído em x é bem menor que o valor atribúido em y.
	
<h1></h1>

Código (<=):<br>
<img src="https://imgur.com/L3hgYok.png">
	
Resultado:<br>
<img src="https://imgur.com/rc75hwY.png">
	
Observe que o valor que foi atribuído ao x, não é menor que o valor de y mas sim igual ao valor de y, portanto sendo verdadeiro, foi exibido a mensagem dentro da condição de "if".
	
<h1></h1>
	
Código (>=):<br>
<img src="https://imgur.com/iEHXjX1.png">

Resultado:<br>
<img src="https://imgur.com/AHxQTZq.png">
	
O resultado exibido em nosso console está dizendo que x é maior ou igual a y, e de fato isso é verdadeiro. O valor que foi atribuído em x é maior do que y mas não é igual a y.
	
<h1></h1>
	
Código (!=):<br>
<img src="https://imgur.com/nQCzGHw.png">

Resultado:<br>
<img src="https://imgur.com/a6rBsz7.png">
	
A resposta em geral foi dada como verdadeiro, pois o valor que está atribuído em x é diferente do valor que está atribuído em y, portanto o valor é verdadeiro e será exibido a mensagem dentro da condição de "if".
