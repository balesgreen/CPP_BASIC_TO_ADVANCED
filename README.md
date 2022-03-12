# C++ BASICO AO AVANÇADO

 <h3>Tópicos</h3>
 
  * Entendendo a estrutura principal do programa C++


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

