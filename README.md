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
