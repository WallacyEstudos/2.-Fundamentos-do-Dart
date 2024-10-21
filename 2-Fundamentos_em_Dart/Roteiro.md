Aqui está o roteiro de aula detalhado, incluindo o conteúdo a ser apresentado e sugestões de falas para guiar os alunos.

---

### **Roteiro de Aula: Fundamentos de Dart para Iniciantes**

---

### **Objetivo da Aula**:
- Introduzir os conceitos básicos da linguagem Dart.
- Ensinar o uso de variáveis, controle de fluxo, funções e classes.
- Fornecer uma base sólida para o desenvolvimento com Dart, preparando para o Flutter.

### **Duração Estimada**: 1h 30m

---

### **Introdução (5 min)**:

**Professor diz**:
“Olá pessoal, bem-vindos à aula de Dart! Hoje vamos aprender os fundamentos dessa linguagem de programação criada pelo Google. Para quem não conhece, Dart é usada principalmente no desenvolvimento de aplicativos móveis com o Flutter. Vamos começar do zero, então, mesmo que você nunca tenha programado antes, não se preocupe! Vamos dar um passo de cada vez. Prontos?”

**Slide/Quadro**:  
**Objetivos da aula**:
1. Variáveis e Tipos de Dados
2. Null Safety
3. Controle de Fluxo (If e Switch)
4. Funções e Métodos
5. Classes e Objetos

---

### **Parte 1: Variáveis e Tipos de Dados (15 min)**

**Professor diz**:  
“Vamos começar falando sobre variáveis. Vocês podem pensar em variáveis como ‘caixinhas’ onde guardamos dados. E esses dados podem ser de vários tipos: números, textos, verdadeiros ou falsos, entre outros.”

**Slide/Quadro**:  
- **Variáveis**: Espaços na memória para guardar informações.
- **Tipos de Dados**: `int`, `double`, `String`, `bool`, `List`, etc.

**Professor apresenta o código no IDE**:

```dart
void main() {
  String nome = "José"; // Variável de texto
  int idade = 25; // Variável de número inteiro
  bool ativo = true; // Variável booleana
  List<String> amigos = ["Ana", "Carlos"]; // Lista de Strings

  print(nome); // Exibe: José
  print(idade); // Exibe: 25
  print(ativo); // Exibe: true
  print(amigos[0]); // Exibe: Ana
}
```

**Professor explica passo a passo**:  
“Primeiro, temos a variável `nome`, do tipo `String`, que guarda um texto. Depois, a variável `idade`, do tipo `int`, que guarda números inteiros. A variável `ativo` é um valor booleano, ou seja, pode ser **verdadeiro** (`true`) ou **falso** (`false`). E finalmente, temos a `lista` de amigos, que armazena vários textos.”

**Professor diz**:  
“Podemos acessar os valores dentro da lista usando um índice. Por exemplo, `amigos[0]` nos dá o primeiro amigo, que é `Ana`.”

**Tarefa Rápida**:  
“Agora, tente criar uma variável chamada `altura`, do tipo `double`, e atribua um valor decimal a ela, como 1.75.”

---

### **Parte 2: Null Safety (10 min)**

**Professor diz**:  
“Agora, vamos falar sobre algo muito importante no Dart: **null safety**. Vocês já ouviram falar do problema de tentar acessar algo que não existe, certo? Em Dart, se você não inicializar uma variável, ela pode causar erros no seu código. Para evitar isso, Dart tem um sistema que garante que as variáveis estejam seguras contra valores nulos.”

**Slide/Quadro**:  
- **Null Safety**: Protege seu código contra erros de variáveis não inicializadas.

**Professor apresenta o código no IDE**:

```dart
void main() {
  String? nome; // Pode ser nula
  nome = "ABC";
  print(nome); // Exibe: ABC

  nome = null;
  // print(nome); // Isso causaria um erro se tentássemos acessar

  late String sobrenome;
  sobrenome = "Wallacy";
  print(sobrenome); // Exibe: Wallacy
}
```

**Professor explica**:  
“Neste exemplo, a variável `nome` pode ser nula, porque usamos o `?`. Isso significa que, em algum momento, ela pode não ter valor. O `late` permite que a gente declare uma variável e a inicialize depois, sem causar problemas.”

**Professor diz**:  
“Essa proteção do Dart ajuda a evitar muitos erros comuns que acontecem em outras linguagens.”

---

### **Parte 3: Controle de Fluxo (If e Switch) (20 min)**

**Professor diz**:  
“Agora vamos falar sobre como o Dart toma decisões com base em condições. Existem duas maneiras principais de fazer isso: o `if` e o `switch`.”

**Slide/Quadro**:  
- **If/Else**: Verifica uma condição e executa um bloco de código.
- **Switch**: Usa múltiplas condições de forma organizada.

**Professor apresenta o código no IDE**:

```dart
void main() {
  bool continuar = true;

  if (continuar) {
    print("Vamos continuar!"); // Exibe: Vamos continuar!
  } else {
    print("Parei");
  }

  int opcao = 2;
  switch (opcao) {
    case 1:
      print("Opção 1");
      break;
    case 2:
      print("Opção 2"); // Exibe: Opção 2
      break;
    default:
      print("Opção desconhecida");
  }
}
```

**Professor explica**:  
“O `if` verifica se `continuar` é verdadeiro. Se for, ele exibe uma mensagem. Se não for, exibe outra. O `switch` verifica o valor da variável `opcao` e executa o código baseado no número escolhido.”

**Professor diz**:  
“Agora, quero que vocês façam o seguinte: criem um `if` que verifique se um número é maior que 10. Se for, exiba ‘Maior que 10’, se não, exiba ‘Menor ou igual a 10’.”

---

### **Parte 4: Funções e Métodos (20 min)**

**Professor diz**:  
“Agora, vamos falar sobre **funções**. Funções são blocos de código que podemos reutilizar, o que torna o nosso programa mais organizado.”

**Slide/Quadro**:  
- **Funções**: Blocos de código reutilizáveis.

**Professor apresenta o código no IDE**:

```dart
void main() {
  int resultado = somar(3, 5); // Chama a função
  print(resultado); // Exibe: 8
}

// Função que soma dois números
int somar(int a, int b) {
  return a + b;
}
```

**Professor explica**:  
“Aqui, temos uma função chamada `somar`, que recebe dois números como parâmetros e retorna a soma deles. No `main()`, chamamos essa função e armazenamos o resultado na variável `resultado`.”

**Professor diz**:  
“Agora, criem uma função chamada `subtrair`, que recebe dois números e retorna a diferença entre eles. Depois, testem a função.”

---

### **Parte 5: Classes e Objetos (30 min)**

**Professor diz**:  
“Chegamos à parte de **classes e objetos**. Dart é uma linguagem orientada a objetos, o que significa que usamos classes para criar moldes de objetos.”

**Slide/Quadro**:  
- **Classes**: Moldes que definem as características e comportamentos de objetos.
- **Objetos**: Instâncias de uma classe.

**Professor apresenta o código no IDE**:

```dart
void main() {
  Carro meuCarro = Carro('BMW', 'X5', 2022);
  print(meuCarro.toString()); // Exibe: Marca: BMW, Modelo: X5, Ano: 2022
}

class Carro {
  String marca;
  String modelo;
  int ano;

  Carro(this.marca, this.modelo, this.ano);

  String toString() {
    return 'Marca: $marca, Modelo: $modelo, Ano: $ano';
  }
}
```

**Professor explica**:  
“Neste exemplo, temos uma classe `Carro`, que tem três atributos: `marca`, `modelo` e `ano`. O construtor é chamado quando criamos um objeto, como `meuCarro`. E o método `toString()` retorna uma descrição do carro.”

**Professor diz**:  
“Agora é a vez de vocês: Criem uma classe chamada `Pessoa` com os atributos `nome`, `idade` e `cidade`. Depois, criem um método que exiba essas informações.”

---

### **Conclusão e Exercício Final (10 min)**

**Professor diz**:  
“Para finalizar, tentem fazer o seguinte exercício: Crie uma nova classe `Carro`, adicione os atributos `marca`, `modelo` e `ano`, e crie um método `detalhes()` que exiba as informações do carro. Depois, criem um objeto dessa classe e exibam os detalhes.”

**Slide/Quadro**:  
**Exemplo de Tarefa**:
- Crie a classe `Carro`.
- Adicione um método `detalhes()`.
- Crie um objeto e exiba as informações.

---

**Professor encerra**:  
“Ótimo trabalho, pessoal! Hoje

 vocês aprenderam os conceitos básicos de Dart. Lembrem-se de praticar bastante para fixar o conteúdo. Na próxima aula, vamos explorar mais sobre funções e objetos. Até mais!”

---

Esse roteiro cobre os principais tópicos, equilibrando teoria e prática.
