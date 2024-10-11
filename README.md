1. Introdução ao Dart
Objetivo: Apresentar a linguagem Dart, mencionando que é amplamente usada no desenvolvimento de aplicativos móveis com Flutter.
Destaques:
Dart é uma linguagem moderna, com foco em simplicidade e produtividade.
Oferece recursos como tipagem opcional e suporte a programação orientada a objetos.
1. Introdução às Variáveis
Objetivo: Explicar o que são variáveis, como declarar e inicializar variáveis, e os tipos de dados mais comuns em Dart.
Definição: Variáveis são contêineres que armazenam dados temporários que podem ser utilizados e manipulados ao longo da execução do código.
2. Exemplos e Explicações do Código
dart
Copiar código
void main() {
  // Função principal onde o código será executado
  // É o ponto de entrada do programa Dart
  
  // 1 - Introdução a Variáveis
  
  // Declaração de uma variável do tipo String (texto)
  String variavelNome = "José";
  // A variável 'variavelNome' armazena o valor "José"
  print(variavelNome); 
  // Exibe o valor da variável 'variavelNome' no console

  // Declaração de uma variável do tipo int (número inteiro)
  int valorVariavel = 10;
  // A variável 'valorVariavel' armazena o valor 10
  print(valorVariavel); 
  // Exibe o valor da variável 'valorVariavel' no console

  // Declaração de uma variável do tipo bool (valor booleano: true ou false)
  bool ehVerdadeiro = true;
  // A variável 'ehVerdadeiro' armazena o valor booleano true (verdadeiro)
  print(ehVerdadeiro); 
  // Exibe o valor da variável 'ehVerdadeiro' no console

  // Declaração de uma lista (List) que armazena Strings
  List<String> listaDePalavas = ["David", "Wilyan"];
  // A variável 'listaDePalavas' armazena uma lista de Strings contendo "David" e "Wilyan"
  
  // Acessando elementos da lista com índice
  print(listaDePalavas[0]); 
  // Exibe o primeiro elemento da lista, que é "David"

  print(listaDePalavas[1]); 
  // Exibe o segundo elemento da lista, que é "Wilyan"

  // Utilizando interpolação de Strings para exibir múltiplos valores
  print('${listaDePalavas[0]} - ${listaDePalavas[1]}');
  // Exibe os dois nomes concatenados no formato: "David - Wilyan"
}
3. Detalhamento do Roteiro
A. Declaração de Variáveis
Explicação:
Variáveis armazenam dados em memória, e cada variável possui um tipo específico.
Os tipos mais comuns em Dart incluem String para textos, int para números inteiros, bool para valores booleanos, e List para coleções de dados.
B. String:
Exemplo:
dart
Copiar código
String variavelNome = "José";
Explicação: A variável variavelNome é uma String e armazena o texto "José".
Demonstrar: Use o comando print(variavelNome) para exibir o valor armazenado no console.
C. Inteiro (int):
Exemplo:
dart
Copiar código
int valorVariavel = 10;
Explicação: A variável valorVariavel armazena um número inteiro, no caso o valor 10.
Demonstrar: Use print(valorVariavel) para exibir o número no console.
D. Booleano (bool):
Exemplo:
dart
Copiar código
bool ehVerdadeiro = true;
Explicação: A variável ehVerdadeiro armazena um valor booleano, que pode ser true (verdadeiro) ou false (falso). Neste caso, estamos utilizando o valor true.
Demonstrar: print(ehVerdadeiro) exibirá true no console.
E. Listas (List):
Exemplo:
dart
Copiar código
List<String> listaDePalavas = ["David", "Wilyan"];
Explicação: A variável listaDePalavas armazena uma coleção de Strings. Listas são uma maneira de armazenar vários valores em uma única variável.
Acessando elementos: Utilize os índices para acessar elementos individuais na lista.
Exemplo:
dart
Copiar código
print(listaDePalavas[0]); // Exibe "David"
print(listaDePalavas[1]); // Exibe "Wilyan"
Interpolação de Strings: Mostre como combinar diferentes variáveis dentro de uma String:
dart
Copiar código
print('${listaDePalavas[0]} - ${listaDePalavas[1]}');
Isso exibe "David - Wilyan".
4. Conclusão e Prática
Resuma a importância das variáveis para armazenar diferentes tipos de dados.
Desafie os alunos a criar variáveis de diferentes tipos e utilizar o comando print para exibir seus valores.
