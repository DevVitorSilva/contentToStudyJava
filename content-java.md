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
