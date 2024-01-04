# Registro dos meus estudos de conteudo Java

Java ME - Java Micro Edition para IoT(internet das coisas).

Java SE - Java Standard Edtion é o core.

Java EE - Java Enterprise Edtion é um conjunto de especificações para apps corporativos.

---

## Estrutura de um app Java

- Uma aplicação é composta por classes.
- Package é o agrupamento lógico de classes relacionadas.
- Módulo é o agrupamento lógico de packages relacionados.
- Runtime é o agrupamento fisico.
- Aplicação é o agrupamento de módulos relacionados.

---

## Precedência de operadores

1° **\*** (multiplicação), **/** (divisão), **%** (módulo, resto da divisão)

2° +(soma), -(subtração)

---

## Como são declaradas as variáveis em Java

\<tipo> \<nome da variável> = \<valor inicial>

exemplo:

```java
int numeroInteiro = 10;
```

Observer: as variáveis também podem ser declarada sem um valor inicial, e somente depois ser atribuido um valor a variável.

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

Linhas de código em Java sempre terminam com ponto e virgula;

---

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

No exemplo acima temos uma variável chamada `numero` com o valor de 10, logo em seguida ela é verificada se o `numero` é igual a 10, se for igual será impresso no console **É igual a 10**. Neste exemplo, o único bloco que será executado é o `if`, pois atende a condição passada, porém se não fosse o programa irá verificar nas demais condicionais, caso nenhuma condição fosse atendida ele iria executar o `else` e finalizaria a verificação condicional.
