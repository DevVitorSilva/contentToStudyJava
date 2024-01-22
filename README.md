# Registro dos meus estudos de conteudo Java

## Java ME, Java SE e Java EE

Java ME - Java Micro Edition para IoT(internet das coisas).

Java SE - Java Standard Edtion é o core.

Java EE - Java Enterprise Edtion é um conjunto de especificações para apps corporativos.

## Estrutura de um app Java

- Uma aplicação é composta por classes.
- Package é o agrupamento lógico de classes relacionadas.
- Módulo é o agrupamento lógico de packages relacionados.
- Runtime é o agrupamento fisico.
- Aplicação é o agrupamento de módulos relacionados.

## Precedência de operadores

1° **\*** (multiplicação), **/** (divisão), **%** (módulo, resto da divisão)

2° +(soma), -(subtração)

## Como são declaradas as variáveis em Java

\<tipo> \<nome da variável> = \<valor inicial>

exemplo:

```java
int numeroInteiro = 10;
```

Observe: as variáveis também podem ser declarada sem um valor inicial, e somente depois ser atribuido um valor a variável.

exemplo:

```java
int numeroInteiro;
numeroInteiro = 10;
```

Também pode criar mais de uma variável ao mesmo tempo desde que sejam do mesmo tipo.

exemplo:

```java
int numero1, numero2, numero3 = 10; // variavel declarada e inicializada
int numero4, numero5, numero6; // variavel sem valor inicial, somente declarada
```

Vale lembrar que variáveis não inicializada não pode ser usada, o compilador irá acusar um erro.

Linhas de código em Java sempre terminam com ponto e virgula;

## Tipos primitivos e seus valores iniciais

| tipos primitivos | bits | valor inicial padrão |
| ---------------- | ---- | -------------------- |
| byte             | 8    | 0                    |
| short            | 16   | 0                    |
| int              | 32   | 0                    |
| long             | 64   | 0l                   |
| float            | 32   | 0.0f                 |
| double           | 64   | 0.0                  |
| char             | 16   | \\'u000'             |
| boolean          | 1    | false                |

Vale lembrar que também temos o tipo **String** que é uma classe. Variáveis do tipo String guardam referências a objetos, e não um valor, como acontece com os tipos primitivos.

## Saida de dados

Em Java tem algumas formas de saida de dados.

1. `print` para saida de dados sem quebra de linha, **print** é de imprimir na tela.

```java
System.out.print("Hello world!");
```

2. `println` para saida de dados com quebra de linha, **ln** é de linha, imprime na tela e quebra uma linha.

```java
System.out.println("Hello world!");
```

3. `printf` para saida de dados formatados, **f** é de format, imprime na tela os dados formatados.

```java
int myAge = 22;
System.out.printf("Hello world!, my age is %s", myAge);
```

**Máscaras para interpolação de dados usando o printf**

- `%s` é usado para formatar texto.
- `%f` é usado para formatar número de ponto flututante.
- `%d` é usado para formatar número inteiro.
- `%n` é usado para quebra de linha.
- `\n` também usado para quebra de linha.
- `\t` é usado para tabulação, dar um `Tab`.

Observe: quando limita o número de casas decimais, perde a precisão do valor.

## Locale

`Locale.setDefault(Locale.US);` é usado para configurar em qual o local que sua aplicação irá ser usada, deve ser colocado no inicio do seu app.

## Casting

Casting é a conversão de tipo explicita.

Link para saber mais sobre [casting](https://medium.com/@jhonata.ribeiro.ti/casting-impl%C3%ADcito-x-casting-expl%C3%ADcito-no-java-d635c506f1d5).

## Entrada de dados

- `Scanner` usamos o Scanner para a entrada de dados no console, o Scanner já no pacote java.util.

Criando uma entrada de dados string:

```java
Scanner sc = new Scanner(System.in); // instanciando a classe Scanner
sc.next(); // usado para entrada de dados do tipo String
sc.close(); // informa ao scanner que não haverá mais entradas de dados
```

Tipos de entrada de dados:

`sc.close();` usado para quando não precisa mais do objeto sc.

`sc.next();` usado para String.

`sc.nextLine();` usado para ler a entrada até quebrar a linha, ou seja quando der enter.

`sc.nextInt();` usado para entrada do tipo inteiro.

`sc.nexDouble();` usado para entrada do tipo double, atenção quanse se usar, pois ele usa o padrão usado na localidade do sistema padrão. Lembre-se de usar o `Locale` para setar a localidade que deseja.

`sc.next().charAt(0);` usado para pegar o primeiro caractere da entrada.

## Math

**Math** é uma classe para calculos matemáticos, esta classe não precisa ser instanciada.

`Math.sqrt(value)` - é usado para calcular a raiz quadrada de um valor.

`Math.pow(value, value)` - usado para calcular a potência de um valor.

`Math.abs(value)` - usado para calcular o valor absoluto de um valor.

## Operadores comparativos

Expressões comparativas o resultado é um boolean. O valor esquerdo é comparado com o com o valor direito.

| operadores | significado    |
| ---------- | -------------- |
| >          | maior que      |
| <          | menor que      |
| >=         | maior ou igual |
| <=         | menor ou igual |
| ==         | igual          |
| !=         | diferente      |

## Operadores aritméticos

Operadores aritméticos são operadores matemáticos comum.

| operadores | significado             |
| ---------- | ----------------------- |
| +          | soma                    |
| -          | subtração               |
| \*         | multiplicação           |
| /          | divisão                 |
| %          | módulo/resto da divisão |

Shorcut para operadores aritméticos:

| operadores | significado             | seria o mesmo que |
| ---------- | ----------------------- | ----------------- |
| +=         | soma                    | a = a + b;        |
| -=         | subtração               | a = a - b;        |
| \*=        | multiplicação           | a = a \* b;       |
| /=         | divisão                 | a = a / b;        |
| %=         | módulo/resto da divisão | a = a % b;        |

## Operadores lógicos

| operadores | significado |
| ---------- | ----------- |
| &&         | e           |
| \|\|       | ou          |
| !          | negação     |

Tabela verdade operador lógico `&&`

- Só retorna `true` se todos forem `true`.

| comparação        | retorno |
| ----------------- | ------- |
| `true` && `true`  | `true`  |
| `true` && `false` | `false` |
| `false` && `true` | `false` |

Tabela verdade operador lógico `||`

- Só retorna `false` se todos forem `false`.

| comparação           | retorno |
| -------------------- | ------- |
| `true` \|\| `true`   | `true`  |
| `true` \|\| `false`  | `true`  |
| `false` \|\| `true`  | `true`  |
| `false` \|\| `false` | `false` |

Tabela verdade operador lógico `!`

- Retorna `true` se for `false`, se for `false` retorna `true`.

| comparação | retorno |
| ---------- | ------- |
| !`true`    | `false` |
| !`false`   | `true`  |

## Operador bitwise

| operadores | significado  |
| ---------- | ------------ |
| &&         | e            |
| \|         | ou           |
| ^          | ou exclusivo |

## Estrutura condicional `if`, `else if` e `else`

As estruturas condicionais permitem que um bloco de código seja executado somente **se** certa condição for atendida.

| condicional | significado |
| ----------- | ----------- |
| `if`        | se          |
| `else if`   | se não se   |
| `else`      | se não      |

Exemplos:

```java
int numero = 10;

if(numero == 10){
    System.out.println("É igual a 10");
}else if(numero > 9){
    System.out.println("É maior que 10");
}else{
    System.out.println("É igual a 10");
}
```

No exemplo acima temos uma variável chamada `numero` com o valor de 10, logo em seguida ela é verificada se o `numero` é igual a 10, se for igual será impresso no console **É igual a 10**. Neste exemplo, o único bloco que será executado é o `if`, pois atende a condição passada, porém se não fosse, o programa irá verificar nas demais condicionais, caso nenhuma condição fosse atendida ele iria executar o `else` e finalizaria a verificação condicional.

## Condicional switch case

O `switch case` é mais uma condicional, a diferença é a forma como se escreve, e que ele verifica se o valor fornecido é igual aos `case` fornecidos, se não atender nenhum dos `case` será executado o bloco `default`.

Exemplo:

```java
int value = 1;

switch(value){
  case 15:
    System.out.println("value é maior que 15");
    break;
  case 5:
    System.out.println("value é menor que 5");
    break;
  default:
    System.out.println("value é igual a " + value);
    break;
}
```

No exemplo acima mostra a estrutura do `switch case`, no `switch` vai o valor de condição, no `case` vai o valor que será comparado. Observe que só irá entrar em um bloco `case` caso o valor da condição seja igual ao valor de comparação, caso não seja o `switch` irá executar o bloco `default` e encerrar a condicional `switcth`. O `break` informa ao `switch` para que ele pare de verificar e que a condição foi atendida no bloco atual.

## Operador ternário

O operador ternário nada mais é que um `if else` simplificado. Geralmente usado em verificações condicionais onde não é necessário escrever muitas linhas de código.

\<condição> `?` \<executa se atender a condição> `:` \<executa se a condição não for atendida>

Exemplo:

```java
int numero = 10;

numero == 10 ? System.out.println("É igual"); : System.out.println("Não é igual");
```

## Loop de repetição `while`

O loop de repetição `while` repete o bloco de comando enquanto uma condição for verdadeira(true).

Exemplo:

```java
int n = 0;

while(n<100){
  System.out.println(n);
  n++;
}
```

No exemplo acima temos um programa que irá contar até 99. A lógica de funcionamento é o seguinte: primeiro ele verifica a condição e depois executa o bloco de comandos, caso seja a condição seja falsa o bloco de comandos não será executado.

## Loop de repetição `do while`

Diferente do `while`, o `do while` executa primeiramente o bloco de comandos e somente depois faz a verificação da condição.

Exemplo:

```java
int n = 0;

do{
  System.out.println(n);
  n++;
}while(n<100)
```

No exemplo acima temos um app que irá contar até 99, porém escrito usando o loop de repetição `do while`.

## Loop de repetição `for`

O `for` é mais uma forma de fazer loops de repetição em Java, diferente do `while` e `do while`, o `for` tem uma sintaxe diferente.

Exemplo:

```java
for(int index = 0; index < 100; index++){
  System.out.println(index);
}
```

No exemplo acima temos mais um app que irá contar até 99, porém usando o loop `for`.

No loop `for` temos o `index` que é uma variável do tipo inteiro que será usado como um contador, essa variável sempre deve ser inicializada com algum valor. Temos também a condição `index < 100` que irá ser usada para colocar um limite até onde o loop irá ser executado. E por último temos o `index++`, que é um incremento de `index`, ou seja, é `index` + 1. Quando o loop está sendo executado ele irá verificar a condição, se a condição é verdadeira ele soma +1 ao `index` e executa o bloco de comandos, quando a condição se tornar falsa ele irá sair do loop.

## Métodos para String

**Formatar**

- `toLowerCase()` transforma toda a String em minúscula.

```java
String hello = "Hello World!";

hello.toLowerCase(); // a saida será 'hello world!'
```

- `toUpperCase()` transforma toda a String em maiúscula.

```java
String hello = "Hello World!";

hello.toUpperCase(); // a saida será 'HELLO WORLD!'
```

- `trim()` remove os espaços em branco do inicio e fim da String.

```java
String name = "  John Doe  ";
System.out.println(name.trim()); // a saida será 'John Doe'
```

**Recortar**

- `substring()` retorna uma substring da String atual. Este método pode receber dois parâmetros, o primeiro é indice inicial: é onde irá iniciar sua substring, o segundo é indice final: é onde irá terminar sua substring.

```java
String name = "John Doe";
System.out.println(name.substring(0,4)); // a saida será 'John'
```

**Substituir**

- `replace()` método procura por um caractere especificado como parâmetro, e retorna uma nova String com o caractere trocado por um outro caractere que é passado como segundo parâmetro.

```java
String name = "John Doe";
System.out.println(name.replace('o','1')); // a saida será 'J1hn D1e'
```

**Buscar**

- `indexOf()` retorna a posição do primeiro caractere encontrado dentro da String especificada.

```java
String name = "John Doe";
System.out.println(name.indexOf('o')); // a saida será 1
```

- `lastIndexOf()` retorna a posição do último caractere encontrado dentro da String especificada.

```java
String name = "John Doe";
System.out.println(name.lastIndexOf('o')); // a saida será 6
```

**Fatiar**

- `split()` retorna um Array de substrings a partir de um caractere passado por parâmetro.

```java
String name = "John Doe";
String[] names = name.split(" ");
for(int index = 0; index < names.length; index++){
  System.out.println(names[index]); // serão duas saidas: 1° 'John' e 2° 'Doe'
}
```

## Comentários

Os comentários não são interpretados pelo compilador.

- `//` usado para fazer comentário em linha, será um comentário até quebrar a linha.

```java
// este é um comentário em linha
```

- `/* */` usado para fazer blocos de comentários, será um comentário enquanto estiver dentro do bloco.

```java
/*
  este é
  um bloco
  de
  comentários
*/
```

## Funções OOP

Em OOP(Object Oriented Programing), funções em classes recebem o nome de **métodos**.

- `public` disponibiliza a função em outras classes.
- `static` permite a função ser chamada sem a necessidade de criar um objeto.
- `double` é o tipo de dado que será retornado quando o método/função for execultado.

```java
public class Calc{
  public static double sum(double firstValue, double secondValue){
    return firstValue + secondValue;
  }

  public static double sub(double firstValue, double secondValue){
    return firstValue - secondValue;
  }

  public static double mult(double firstValue, double secondValue){
    return firstValue * secondValue;
  }

  public static double div(double firstValue, double secondValue){
    return firstValue / secondValue;
  }
}
```

## Classes OOP

Classes é um **tipo** estruturado que pode conter membros:

- Atributos(dados/campos)
- Métodos(funções/operações)

A classes também pode prover muitos outros recursos, tais como:

- Construtores
- Sobrecarga
- Encapsulamento
- Herança
- Polimorfismo

Classes é a difinição de tipo. Objetos são instâncias da classe.

**this** é uma alto referência para o objeto.

Toda classe em java é uma subclasse da classe `Object`.

`Object` possui os métodos:

- `getClass` retorna o tipo do objeto.
- `equals` compara se o objeto é igual a outro.
- `hashCode` retorna um código hash do objeto.
- `toString` converte o objeto para String.
- `format` retorna uma String formatada usando as especificações passadas e os argumentos.

## Membros estáticos OOP

Também chamados membros de classe, em oposição a membros e instância. São membros que fazem sentido independente de objetos. Não precisam de objetos para serem chamados, não precisa instanciar a classe. São chamados a partir do próprio nome da classe.

Aplicações comuns:

- Classes utilitárias
- Declaração de constantes

Uma classe que possui somente membros estáticos, pode ser uma classe estática também. Esta classe não poderá ser instanciadas.

Observe: não é possivel chamar um método/função que não é estático dentro de um que é estático.

## Construtores OOP

Construtores são uma operação especial da classe, que é executada no momento da instanciação do objeto.

Usos comum:

- Iniciar valores dos atributos.
- Permitir ou obrigar que o objeto receba dados/dependências no momento de sua instanciação(injeção de dependência).
- Se um construtor customizado não for especificado, a classe disponibiliza o construtor padrão: `Product p = new Product();`.
- É possível especificar mais de um construtor na mesma classe(sobrecarga).

## Palavra `this` OOP

A palavra `this` é uma referência para o próprio objeto.

Uso comum:

- Diferenciar atributos de variáveis locais.
- Passar o próprio objeto como argumento na chamada de um método ou construtor.

```java
public class People{
  // variáveis locais
  String name;
  int age;

  // atributos do construtor personalizado
  public People(String name, int age){
    // atribuindo os valores recebidos como parâmetro para as variáveis locais da classe
    this.name = name;
    this.age = age;
  }
}
```

## Sobrecarga OOP

Sobrecarga é um recurso que uma classe possui de oferecer mais de uma operação com o mesmo nome, porém com diferentes listas de parâmetros.

```java
public class People{
  String name;
  int age;

  public People(){}

  public People(String name){
    this.name = name;
  }

  public People(String name, int age){
    this.name = name;
    this.age = age;
  }
}
```

No código acima temos três contrutores, dessa forma quando for instânciar a classe podemos passar ou não os atributos.

## Ecapsulamento OOP

Ecapsulamento é um principio que consiste em esconder detalhes de implementação de uma classe, expondo apenas operações seguras e que mantenham os objetos em um estado consistente.

**Regra de ouro**: o objeto deve sempre estar em um estado consistente, e a própria classe deve garantir isso.

Regra geral básica:

- Um objeto **não** deve expor nenhum atributo(modificador de acesso `private`).
- Os atributos devem ser acessados por meio de métodos `get` e `set`.

Exemplo:

```java
public class People{
  private String name;
  private int age;

  public People(){}

  public People(String name){
    this.name = name;
  }

  public People(String name, int age){
    this.name = name;
    this.age = age;
  }

  public String getName(){
    return this.name;
  }

  public void setName(String name){
    this.name = name;
  }

  public int getAge(){
    return this.age;
  }

  public void setAge(int age){
    this.age = age;
  }
}
```

No exemplo acima foi usado encapsulamento, onde os métodos da classe `People` são privados e só podem ser acessados e modificados pelos métodos `get` e `set`.

Observe: no IntelliJ IDE, há como criar os métodos `get` e `set` de forma automática sem precisar digitar tudo. Uma recomendação pessoal é que, se é seu primeiro contato com Java, não faça de modo automático, realmente escreva o código para que você vá se acostumando com sintaxe da linguagem.

## Modificadores de acesso OOP

- `private`: o membro só pode ser acessado na própria classe.

```java
public class People{
  private String name;
}
```

- (nada): o membro só pode ser acessado nas classes do mesmo pacote.

```java
public class People{
  String name;
}
```

- `protected`: o membro só pode ser acessado no mesmo pacote, bem como em subclasses de pacotes diferentes.

```java
public class People{
  protected String name;
}
```

- `public`: o mebro é acessado por todas as classes(ao menos que ele resida em um módulo diferente que não exporte o pacote onde ele está).

```java
public class People{
  public String name;
}
```

## Tipos referência

Recomanda-se ter um pouco de entendimento sobre memória **stack** e **heap**. Leia esse [debate no stackoverflow](https://pt.stackoverflow.com/questions/3797/o-que-s%C3%A3o-e-onde-est%C3%A3o-a-stack-e-heap) para ter mais conhecimento sobre memória **stack** e **heap**.

Classes são do tipo referência. Variáveis cujo tipo são classes não devem ser entendidas como caixas, mas sim "tentáculos"(ponteiros) para caixas.

```java
Product p1 = new Product("Smartphone", 2500.00);
Product p2 = p1;
```

Exemplo como funciona a alocação de memória para tipos de referência, exemplo do código acima:

![representação de alocação de memória para tipos de referência](./images/memoryStackAndHeap.svg)

Quando se usa tipos de referência, os valores são armazenados na memória heap, na memória **stack** fica armazenado somente um ponteiro(como se fosse um id) que aponta para os valores na memória **heap**.

Passo a passo:

1. A aplicação busca a variável na **stack**
2. Encontra um ponteiro(id) que faz referência aos valores que estão armazenados na **heap**
3. Busca os valores na **heap** e trás os valores para nossa aplicação

**Atenção**: cuidado ao declarar variáveis que recebem outra variável de tipos referência, pois como elas irão apontar para o mesmo valor, caso mude o valor de umas delas as duas serão alteradas.

## Valor `null`

Tipos de referência aceitam o valor `null`, que indica que a variável aponta pra ninguém.

![Exemplo de valor null na memória](./images/valueNull.svg)

## Tipos valor

Os tipos primitivos são valores. Em Java tipos primitivos são tipos valor. Tipos valor são caixas e não ponteiros.

```java
double x = 10;
double y = x;
```

`y` recebe uma cópia de `x`, se o valor de `y` for alterado não irá alterar o valor de `x`.

![representação de alocação de memória para tipos de valor](./images/usingMemoryStack.svg)

Tipos primitivos que são tipos valor, são armazenados diretamente na memória **stack**. Isso significa que o acesso de tipos primitivos são mais rápidos que os tipos de referência.

## Valores inicial padrão para os tipos referência

Quando alocamos (new) qualquer tipo estruturado (classes e arrays), são atribuídos valores padrão aos seus elementos.

| Tipo    | Valor padrão       |
| ------- | ------------------ |
| números | 0                  |
| boolean | false              |
| char    | caractere código 0 |
| objeto  | null               |

## Tipos referência vs tipos valor

| Classe                                                                                 | Tipo primitivo                                                                     |
| -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Usufrui de todos recursos OO                                                           | É mais simples e mais perfomático                                                  |
| Variáveis são ponteiros                                                                | Variáveis são caixas                                                               |
| Objetos precisam ser instanciadas usando `new`, ou apontar para um objeto já existente | Não instancia. Uma vez declarados, estão prontos para uso                          |
| Aceita valor `null`                                                                    | Não aceita valor `null`                                                            |
| Y = X; "Y passa a apontar para onde X aponta"                                          | Y = X; "Y recebe uma cópia de X"                                                   |
| Objetos instanciados no heap                                                           | "Objetos" instanciados no stack                                                    |
| Objetos não utilizados são desalocados em um momento próximo pelo garbage collector    | "Objetos" são desalocados imediatamente quando seu escopo de execução é finalizado |

## Desalocação de memória Garbage Collector

Garbage Collector é um processo que automatiza o gerenciamento de memória de um programa em execução. O Garbage Collector monitora os objetos alocados dinamicamente pelo programa(no heap), desalocando aqueles que não estão mais sendo utilizados.

Um objeto que não possui referência(ponteiro), ou que perdeu a referência, será desalocado pelo Garbage Collector em breve.
