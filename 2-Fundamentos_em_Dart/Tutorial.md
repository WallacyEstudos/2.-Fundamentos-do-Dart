### Tutorial: Fundamentos de Dart para Iniciantes

Neste tutorial, você aprenderá os conceitos básicos da linguagem de programação Dart. Cada seção inclui código, explicações detalhadas e screenshots para ajudar você a entender o conteúdo. O tutorial é dividido em cinco partes:

1. Variáveis e Tipos de Dados
2. Null Safety
3. Controle de Fluxo (If e Switch)
4. Funções e Métodos
5. Classes e Objetos

### **Parte 1: Variáveis e Tipos de Dados**

#### **Passo 1: O que são Variáveis?**

As variáveis são usadas para armazenar informações que podem ser usadas e manipuladas ao longo do código. Em Dart, cada variável tem um tipo específico, como `int` (para números inteiros), `String` (para textos), `double` (para números com casas decimais), entre outros.

##### **Exemplo de Código**:

```dart
void main() {
  String nome = "João"; // Declara uma variável do tipo texto (String)
  int idade = 25; // Declara uma variável do tipo inteiro (int)
  double altura = 1.80; // Declara uma variável do tipo decimal (double)
  
  print("Nome: $nome"); // Exibe o nome
  print("Idade: $idade"); // Exibe a idade
  print("Altura: $altura"); // Exibe a altura
}
```

#### **Passo 2: Executando o Código**

No editor Dart, ao executar o código acima, o resultado será exibido no terminal como:

```
Nome: João
Idade: 25
Altura: 1.8
```

#### **Screenshot**:

![Variáveis e Tipos de Dados](link_to_screenshot)

Neste código, utilizamos:
- **String** para armazenar texto.
- **int** para números inteiros.
- **double** para números com casas decimais.
- Usamos **print()** para exibir as informações no console.

---

### **Parte 2: Null Safety**

Dart introduziu o conceito de **null safety**, que ajuda a prevenir erros ao acessar variáveis que não foram inicializadas.

#### **Passo 1: Declarando Variáveis Nulas**

Usamos o `?` para indicar que uma variável pode ser nula. Isso nos protege de tentarmos usar uma variável que ainda não foi inicializada.

##### **Exemplo de Código**:

```dart
void main() {
  String? nome; // A variável 'nome' pode ser nula
  nome = "Maria"; // Inicializamos com um valor
  print(nome); // Exibe: Maria
  
  nome = null; // Agora a variável é nula
  print(nome); // Exibe: null
}
```

#### **Screenshot**:

![Null Safety](link_to_screenshot)

Aqui, vemos que a variável `nome` pode armazenar um valor ou ser nula. Com null safety, o código evita erros como "Null Pointer Exception".

---

### **Parte 3: Controle de Fluxo (If e Switch)**

#### **Passo 1: O que é Controle de Fluxo?**

Controle de fluxo é o processo de tomar decisões no código. O Dart oferece duas estruturas principais para isso: `if` e `switch`.

##### **Exemplo de Código (If)**:

```dart
void main() {
  bool seguirEmFrente = true;
  
  if (seguirEmFrente) {
    print("Andar"); // Se a condição for verdadeira, exibe "Andar"
  } else {
    print("Parar"); // Se for falsa, exibe "Parar"
  }
}
```

#### **Passo 2: Usando o Switch**

O `switch` permite verificar múltiplos valores de uma variável.

##### **Exemplo de Código (Switch)**:

```dart
void main() {
  int numero = 2;
  
  switch (numero) {
    case 1:
      print("Um");
      break;
    case 2:
      print("Dois");
      break;
    default:
      print("Outro número");
  }
}
```

#### **Screenshot**:

![Controle de Fluxo](link_to_screenshot)

No exemplo do `if`, o código verifica se a condição é verdadeira ou falsa. No `switch`, verificamos o valor da variável `numero` e exibimos diferentes mensagens com base no seu valor.

---

### **Parte 4: Funções e Métodos**

#### **Passo 1: O que são Funções?**

Funções são blocos de código que realizam uma tarefa específica e podem ser reutilizados várias vezes.

##### **Exemplo de Código**:

```dart
void main() {
  int resultado = soma(3, 4); // Chama a função 'soma' passando dois números
  print(resultado); // Exibe: 7
}

int soma(int a, int b) {
  return a + b; // Retorna a soma de 'a' e 'b'
}
```

#### **Screenshot**:

![Funções](link_to_screenshot)

Neste exemplo, criamos a função `soma` que recebe dois números como parâmetros e retorna a soma. A função é chamada no `main()`.

---

### **Parte 5: Classes e Objetos**

#### **Passo 1: O que são Classes?**

Classes são moldes que definem como os objetos (instâncias) serão. Os objetos são criados a partir das classes.

##### **Exemplo de Código**:

```dart
void main() {
  Celular celularDoJoao = Celular("Azul", 5.5, 200); // Cria um objeto da classe 'Celular'
  print(celularDoJoao.cor); // Exibe: Azul
  print(celularDoJoao.peso); // Exibe: 200
}

class Celular {
  String cor;
  double tamanho;
  double peso;
  
  Celular(this.cor, this.tamanho, this.peso); // Construtor da classe
  
  String descricao() {
    return "Cor: $cor, Tamanho: $tamanho, Peso: $peso"; // Método que descreve o celular
  }
}
```

#### **Passo 2: Explicação**

Aqui, criamos a classe `Celular` com os atributos `cor`, `tamanho` e `peso`. O método `descricao()` retorna uma string que descreve o celular. No `main()`, criamos um objeto `celularDoJoao` da classe `Celular`.

#### **Screenshot**:

![Classes e Objetos](link_to_screenshot)

---

### **Conclusão**

Agora que você aprendeu os conceitos básicos do Dart, tente criar suas próprias funções e classes. Você pode continuar explorando, criando classes mais complexas e aplicando o que aprendeu em projetos reais.

---

Se precisar de mais exemplos ou de assistência para instalar o ambiente de desenvolvimento, consulte o guia oficial do Dart e Flutter no site oficial: [https://dart.dev](https://dart.dev).