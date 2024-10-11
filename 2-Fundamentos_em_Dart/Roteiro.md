Aqui está um roteiro de aula sobre os fundamentos do **Dart**, com foco em iniciantes que nunca programaram antes. O objetivo é introduzir conceitos básicos da linguagem Dart de forma progressiva, explicando cada trecho do código à medida que ele é apresentado. A aula será dividida em seções temáticas para facilitar o aprendizado.

---

### **Roteiro de Aula: Fundamentos de Dart para Iniciantes**

---

### **Objetivo da Aula**:
Nesta aula, vamos aprender os fundamentos da linguagem Dart, que é usada para desenvolvimento com Flutter. Vamos abordar os seguintes tópicos:
1. Variáveis e Tipos de Dados
2. Null Safety
3. Controle de Fluxo (If e Switch)
4. Funções e Métodos
5. Classes e Objetos

### **Duração Estimada**: 1h 30m

---

### **Introdução**: 
- **Dart** é uma linguagem de programação criada pelo Google, usada principalmente para o desenvolvimento de aplicativos móveis com **Flutter**.
- Antes de começarmos, lembre-se de que Dart é **fortemente tipada**. Isso significa que devemos especificar o tipo de dado que uma variável pode armazenar.

---

### **Parte 1: Variáveis e Tipos de Dados**

**Objetivo**: Mostrar o que são variáveis e como armazenamos informações em Dart.

#### **Explicação teórica**
- **Variáveis**: Espaços na memória onde podemos guardar dados. Elas podem armazenar números, textos, listas e muito mais.
- **Tipos de Dados**: Determinam o tipo de valor que uma variável pode armazenar, como `int`, `double`, `String`, `bool`, entre outros.

#### **Exemplo de código**:

```dart
void main() {
  // Declarando uma variável do tipo String para armazenar texto
  String variavelNome = "José"; // Variável de texto
  print(variavelNome); // Exibe: José
  
  // Declarando uma variável do tipo inteiro (int)
  int valorVariavel = 10; // Armazena um número inteiro
  print(valorVariavel); // Exibe: 10
  
  // Declarando uma variável do tipo booleano (bool), que pode ser true ou false
  bool ehVerdadeiro = true; // Armazena verdadeiro
  print(ehVerdadeiro); // Exibe: true
  
  // Declarando uma lista (array) de Strings
  List<String> listaDePalavras = ["David", "Wilyan"];
  print(listaDePalavras[0]); // Acessa o primeiro elemento da lista - Exibe: David
  print(listaDePalavras[1]); // Acessa o segundo elemento da lista - Exibe: Wilyan
  
  // Usando interpolação de strings (colocando variáveis dentro de uma string)
  print('${listaDePalavras[0]} - ${listaDePalavras[1]}'); // Exibe: David - Wilyan
}
```

#### **Explicação passo a passo**:
1. **String**: Usamos `String` para guardar textos. A variável `variavelNome` armazena "José".
2. **int**: `int` é usado para armazenar números inteiros (sem casas decimais). A variável `valorVariavel` armazena o número 10.
3. **bool**: `bool` guarda valores booleanos, ou seja, **true** ou **false**. A variável `ehVerdadeiro` armazena `true`.
4. **List**: Uma **lista** guarda vários valores. Aqui, a lista `listaDePalavras` contém dois nomes.

---

### **Parte 2: Null Safety**

**Objetivo**: Introduzir o conceito de **null safety** em Dart.

#### **Explicação teórica**:
- **Null Safety**: Significa que Dart protege o seu código para que você não tente acessar variáveis que não foram inicializadas (ou que estão vazias).

#### **Exemplo de código**:

```dart
void main() {
  // Declarando uma variável que pode ser nula (adicionando o '?')
  String? nome;
  
  // Inicializando a variável com um valor
  nome = "ABC";
  print(nome); // Exibe: ABC
  
  // Atribuindo null à variável
  nome = null;
  // Se tentarmos usar a variável agora, o código daria erro, pois nome é null

  // Usando a palavra 'late' para inicializar a variável depois
  late String sobrenome;
  sobrenome = "Wallacy";
  print(sobrenome); // Exibe: Wallacy
}
```

#### **Explicação passo a passo**:
1. **String?**: O ponto de interrogação `?` indica que a variável pode ser nula, ou seja, pode não conter valor.
2. **late**: A palavra `late` permite declarar uma variável sem valor e inicializá-la depois.

---

### **Parte 3: Controle de Fluxo (If e Switch)**

**Objetivo**: Mostrar como tomar decisões no código com estruturas de controle de fluxo.

#### **Explicação teórica**:
- O **if** executa código apenas se uma condição for verdadeira.
- O **switch** é usado para verificar múltiplas condições.

#### **Exemplo de código**:

```dart
void main() {
  // Declaração de uma variável booleana
  bool seguirEmFrente = true;
  
  // Estrutura de decisão IF
  if (seguirEmFrente) {
    print("Andar"); // Exibe: Andar
  } else {
    print("Parar");
  }
  
  // Outro exemplo de IF
  if (10 > 5) {
    print("10 é maior que 5"); // Exibe: 10 é maior que 5
  }

  // Estrutura de decisão SWITCH
  int valorInt = 5;
  
  switch (valorInt) {
    case 0:
      print("ZERO");
      break;
    case 1:
      print("UM");
      break;
    case 2:
      print("DOIS");
      break;
    default:
      print("PADRÃO"); // Exibe: PADRÃO
  }
}
```

#### **Explicação passo a passo**:
1. **If**: Verifica uma condição. Se a condição for verdadeira, executa um bloco de código.
2. **Else**: Executa outro bloco de código se a condição for falsa.
3. **Switch**: Verifica múltiplos valores de uma variável e executa o código correspondente.

---

### **Parte 4: Funções e Métodos**

**Objetivo**: Introduzir o conceito de funções e métodos, que são blocos de código reutilizáveis que podem ser chamados para realizar tarefas específicas, reduzindo a duplicação e tornando o código mais organizado.

#### **Explicação Teórica**:
- **Funções**: São blocos de código independentes que executam uma tarefa específica. Funções podem receber **parâmetros** (dados de entrada), e algumas podem retornar **valores** após a execução. 
- Funções são úteis para organizar o código e evitar repetições. Uma vez que uma função é definida, você pode chamá-la em qualquer parte do código sempre que precisar daquela funcionalidade.

**Sintaxe básica de uma função**:
```dart
// Declaração da função
tipoDeRetorno nomeDaFuncao(parametros) {
  // Corpo da função
  return valor; // (Opcional, dependendo do tipo de retorno)
}
```

- **Tipo de retorno**: Indica o tipo de dado que a função vai retornar, como `int`, `String`, `void` (caso não retorne nada), etc.
- **Parâmetros**: São os dados que a função precisa para realizar sua tarefa. Parâmetros são opcionais, dependendo da função.

---


#### **Exemplo 3: Função com parâmetros e retorno**

```dart
int soma(int a, int b) {
  return a + b;  // Retorna a soma de 'a' e 'b'
}

void main() {
  int resultado = soma(5, 3);  // A função 'soma' retorna 8
  print("O resultado é: $resultado");  // Exibe: O resultado é: 8
}
```

**Explicação**:
- A função `soma(int a, int b)` recebe dois inteiros (`a` e `b`) e retorna a soma deles.
- No `main()`, a função `soma(5, 3)` é chamada, e o valor retornado (8) é armazenado na variável `resultado`. O resultado é então impresso no console.

---

### **Funções vs Métodos**

Uma **função** é definida fora de qualquer classe e serve como um bloco de código reutilizável, enquanto um **método** é uma função associada a uma classe. Ou seja, todas as funções que pertencem a objetos ou classes são chamadas de **métodos**.

---

#### **Exemplo de Métodos em uma Classe**

```dart
class Pessoa {
  String nome;
  int idade;
  
  Pessoa(this.nome, this.idade);
  
  void exibirDados() {
    print("Nome: $nome, Idade: $idade");
  }
  
  int calcularAnoDeNascimento(int anoAtual) {
    return anoAtual - idade;
  }
}

void main() {
  // Criando um objeto da classe Pessoa
  Pessoa pessoa = Pessoa("João", 30);
  
  // Chamando o método exibirDados()
  pessoa.exibirDados();  // Exibe: Nome: João, Idade: 30
  
  // Chamando o método calcularAnoDeNascimento()
  int anoNascimento = pessoa.calcularAnoDeNascimento(2024);
  print("Ano de Nascimento: $anoNascimento");  // Exibe: Ano de Nascimento: 1994
}
```

**Explicação**:
- A classe `Pessoa` tem dois métodos: `exibirDados()`, que apenas imprime as informações da pessoa, e `calcularAnoDeNascimento()`, que recebe o ano atual e calcula o ano de nascimento com base na idade da pessoa.
- Um **método** sempre é chamado através de uma instância de uma classe, como `pessoa.exibirDados()`.

---

### **Resumo**:
- Funções são blocos de código reutilizáveis que podem ser chamados repetidamente no programa.
- Funções podem receber parâmetros e retornar valores. Elas ajudam a organizar o código e evitam repetição.
- Dart permite a definição de parâmetros opcionais e nomeados, oferecendo flexibilidade ao chamar funções.
- Métodos são funções que pertencem a classes e são chamadas a partir de objetos.

---

### **Parte 5: Classes e Objetos**

**Objetivo**: Apresentar os conceitos de Programação Orientada a Objetos (POO), com exemplos de classes e objetos.

#### **Explicação teórica**:
- **Classes**: São como moldes que definem as características (atributos) e ações (métodos) dos objetos.
- **Objetos**: São instâncias de uma classe.

#### **Exemplo de código**:

```dart
void main() {
  // Criação de dois objetos da classe Celular
  Celular celularDoDeivid = Celular('Azul', 5, 0.000, 5.7);
  Celular celularDoZe = Celular('Preto', 10, 0.000, 5.7);
  
  // Exibindo os valores do celular usando o método toString
  print(celularDoDeivid.toString()); // Exibe: Cor Azul, qtdPros 5, Peso 0.0, Tamanho 5.7
  print(celularDoZe.toString()); // Exibe: Cor Preto, qtdPros 10, Peso 0.0, Tamanho 5.7
  
  // Calculando o valor do celular com base no número de processadores
  double resultado = celularDoDeivid.valorDoCelular(1000);
  print(resultado); // Exibe: 1005.0
}

// Definindo a classe Celular
class Celular {
  final String cor;
  final int qtdPros;
  final double tamanho;
  final double peso;
  
  // Construtor da classe Celular
  Celular(this.cor, this.qtdPros, this.peso, this.tamanho);
  
  // Método toString para exibir as informações do celular
  String toString() {
    return 'Cor $cor, qtdPros $qtdPros, Peso $peso, Tamanho $tamanho';
  }
  
  // Método que calcula o valor do celular
  double valorDoCel

ular(double preco) {
    return preco + qtdPros.toDouble();
  }
}
```

#### **Explicação passo a passo**:
1. **Classe Celular**: Definimos uma classe com atributos como `cor`, `qtdPros`, `peso` e `tamanho`.
2. **Construtor**: O construtor inicializa esses atributos quando criamos um objeto.
3. **Métodos**: A classe tem métodos como `toString()` para exibir os valores e `valorDoCelular()` para calcular um valor com base em parâmetros.

---

### **Conclusão e Exercício Final**

Agora que cobrimos os fundamentos de Dart, que tal tentar criar uma nova classe chamada `Carro`? Adicione atributos como `marca`, `modelo` e `ano`, e crie um método que exiba as informações do carro. 

**Exemplo de Tarefa**:
- Crie uma classe `Carro`.
- Adicione um método `toString()` que exiba os detalhes do carro.
- Crie um objeto da classe `Carro` e exiba suas informações.

---

Este roteiro explica cada parte do código em detalhes, fornecendo uma abordagem didática e progressiva para iniciantes.
