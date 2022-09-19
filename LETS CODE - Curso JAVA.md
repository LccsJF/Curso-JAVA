# **LETS CODE**

## **CURSO JAVA**

 

Java é uma linguagem compilada que precisa de um ambiente próprio para execução. O ambiente de execução se chama **JRE (JavaRuntime Enviroment)**. Para desenvolver em Java precisa do kit de instalação **JDK (Java Development Kit)**.

Baixar no site da Oracle: <https://www.oracle.com/java/technologies/downloads/>; a versão 17 LTS (long-term support), tem suporte extendido, é mais segura para desenvolver software para o mercado, empresas. Para o curso, baixar aversão 18 que tem novos recursos. Selecionar o sistema operacional utilizado na máquina.

Selecionar o sistema operacional (Windows) e baixar o arquivo: **x64 Installer**;executar e será instalado: **C:\Program Files\Java\jdk-18.0.2.1**; depois de instalado, abrir o prompt de comando (CMD), utilizando Windows+R e digitar CMD; digitar: **java –version** para saber a versão instalada;



### **COMANDOS**

 **jshell **– é o ambiente de trabalho do Java; todos os comandos no Java finalizam com (***;***) é obrigatório, não pode esquecer.

**System.out.println(“helloWorld”);** – primeira linha de comando para escrever a clássica frase: *hello World*.

**/exit**– sair do ambiente Java e voltar ao terminal CMD do Windows.

![java1](assets/java1.jpg)

Para programar em Java utilizar a **IDE** *(IntegratedDevelopment Enviroment)* **IJ –IntelliJ IDEA, **ferramenta ideal para desenvolvimento Java; É a mais utilizada na atualidade.

**IDE** - Ambiente onde se desenvolve um código: **VSCode, IntelliJ**

No site **JETBRAINS**: https://www.jetbrains.com/pt-br/idea/download/#section=windows, selecionar o sistema operacional; versão **Ultimate** é completa e requer pagar uma assinatura; versão **Community** é gratuita; baixar a versão **Community **para o desenvolvimento do curso.



## IntelliJ IDEA

Quando a IDE abrir selecionar: NEW PROJECT; 

![intelliJ1](assets/intelliJ1.jpg)

Na próxima tela definir o nome olocal onde será salvo o projeto:

![intelliJ2](assets/intelliJ2.jpg)

Após criar o projeto: clicar emSRC/NEW/JAVA CLASS

![intelliJ3](assets/intelliJ3.jpg)

Por padrão do Java a **CLASSE** tem o mesmo nome do **ARQUIVO**

![intelliJ4](assets/intelliJ4.jpg)

![intelliJ5](assets/intelliJ5.jpg)

A estrutura inicial está pronta. Para criar o método principal do Java, digitar **“main”**.O IntelliJ tem o **code completion** (auto-completar) quando você digita um comando ou um sinal ortográfico: aspas, parênteses, chaves, colchetes.

Para imprimir algum texto na saída padrão do sistema, digite o comando:

$System.out.println(“hello World”);  — Atalho: sout + enter$

**IMPORTANTE: sempre finalizar as linhas de comando com (;) é obrigatório no Java.**

Podemos iniciar, digitando apenas 2 letras para a palavra do código: “Sy” (System) e pressionar **“CTRL+ . (ponto)”** e o IntelliJ completará a palavra e colocará o “ponto” após: **“System.”**

Após criar a primeira aplicação basta clicar no **botão verde “play”** ao lado do código para **“rodar”** a aplicação total ou somente o módulo: 

![intelliJ6](assets/intelliJ6.jpg)

O resultado aparece no terminal com a frase: **Hello, World!** 

A mensagem: ***"Process finished with exit code 0"*** quer dizer que o código foi processado e passou sem nenhum erro, conforme indica o número "***0***" no final da frase.

 

## VARIÁVEIS

As variáveis no Java são fortemente tipadas, ou seja, você precisa identificar o tipo da variável: 

- Informar qual o tipo da variável: `String`, sempre com a primeira letra ***'maiúscula'***;

- O nome da variável no estilo **'camelCase'**;

- O sinal '**`=`**' para atribuição;

- O conteúdo, se String entre **`""`**;

- E o '**`;`**' no final

  Ex: 

  ```java
  String nome = "Cláudio";
  ```

----

### TIPOS DE DADOS PRIMITIVOS

#### string

Para trabalhar com `string` em que o conteúdo pode variar, a forma correta de escrever o código é declarando a variável ***'nome'*** mas, sem lhe atribuir valor; abaixo declare e atribua o valor desejado para a variável, como está abaixo:

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        String nome;
        nome = "Cláudio";
        nome = "André";
        nome = "Eduardo";
        System.out.println("Olá, " + nome);
    }
}
```

----

#### number

Tipos de váriaveis utilizadas para o tipo number:

- **byte** : O `byte`tipo de dados é um inteiro de complemento de dois de 8 bits com sinal. Tem um valor mínimo de -128 e um valor máximo de 127 (inclusive). O `byte`tipo de dados pode ser útil para economizar memória em [arrays](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html) grandes , onde a economia de memória realmente importa. Eles também podem ser usados no lugar de `int`onde seus limites ajudam a esclarecer seu código; o fato de o alcance de uma variável ser limitado pode servir como uma forma de documentação.

- **short** : O `short`tipo de dados é um inteiro de complemento de dois de 16 bits com sinal. Tem um valor mínimo de -32.768 e um valor máximo de 32.767 (inclusive). Assim como com `byte`, as mesmas diretrizes se aplicam: você pode usar a `short`para economizar memória em arrays grandes, em situações em que a economia de memória realmente importa.

- **int** : Por padrão, o `int`tipo de dados é um inteiro de complemento de dois com sinal de 32 bits, que tem um valor mínimo de -2 31 e um valor máximo de 2 31 -1. No Java SE 8 e posterior, você pode usar o `int`tipo de dados para representar um inteiro sem sinal de 32 bits, que tem um valor mínimo de 0 e um valor máximo de 2 32 -1. Use a classe Integer para usar `int`o tipo de dados como um inteiro sem sinal. Consulte a seção As Classes de Números para obter mais informações. Métodos estáticos como `compareUnsigned`, `divideUnsigned`etc foram adicionados à [`Integer`](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html)classe para suportar as operações aritméticas para inteiros sem sinal.

- **long** : O `long`tipo de dados é um inteiro de complemento de dois de 64 bits. O longo assinado tem um valor mínimo de -2 63 e um valor máximo de 2 63 -1. No Java SE 8 e posterior, você pode usar o `long`tipo de dados para representar um comprimento de 64 bits sem sinal, que tem um valor mínimo de 0 e um valor máximo de 2 64 -1. Use esse tipo de dados quando precisar de um intervalo de valores mais amplo do que os fornecidos por `int`. A [`Long`](https://docs.oracle.com/javase/8/docs/api/java/lang/Long.html)classe também contém métodos como `compareUnsigned`, `divideUnsigned`etc para dar suporte a operações aritméticas para unsigned long.

- **float** : O `float`tipo de dados é um ponto flutuante IEEE 754 de 32 bits de precisão simples. Seu intervalo de valores está além do escopo desta discussão, mas é especificado na seção [Tipos, formatos e valores](https://docs.oracle.com/javase/specs/jls/se7/html/jls-4.html#jls-4.2.3) de ponto flutuante da Especificação de linguagem Java. Assim como nas recomendações para `byte`e `short`, use a `float`(em vez de `double`) se precisar economizar memória em grandes matrizes de números de ponto flutuante. Esse tipo de dados nunca deve ser usado para valores precisos, como moeda. Para isso, você precisará usar a classe [java.math.BigDecimal . ](https://docs.oracle.com/javase/8/docs/api/java/math/BigDecimal.html)Capas de [Numbers e Strings](https://docs.oracle.com/javase/tutorial/java/data/index.html)`BigDecimal` e outras classes úteis fornecidas pela plataforma Java.

- **double** : O `double`tipo de dados é um ponto flutuante IEEE 754 de precisão dupla de 64 bits. Seu intervalo de valores está além do escopo desta discussão, mas é especificado na seção [Tipos, formatos e valores](https://docs.oracle.com/javase/specs/jls/se7/html/jls-4.html#jls-4.2.3) de ponto flutuante da Especificação de linguagem Java. Para valores decimais, esse tipo de dados geralmente é a opção padrão. Conforme mencionado acima, esse tipo de dados nunca deve ser usado para valores precisos, como moeda.

- **boolean** : O `boolean`tipo de dados tem apenas dois valores possíveis: `true`e `false`. Use esse tipo de dados para sinalizadores simples que rastreiam condições verdadeiras/falsas. Esse tipo de dados representa um bit de informação, mas seu "tamanho" não é algo definido com precisão.

- **char** : O `char`tipo de dados é um único caractere Unicode de 16 bits. Tem um valor mínimo de `'\u0000'`(ou 0) e um valor máximo de `'\uffff'`(ou 65.535 inclusive).

  ​

No exemplo abaixo criamos variáveis do tipo **int** *(números inteiros)*;

```Java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        int a;
        int b = 2;
        a = 3;

        int soma = a + b;
        int subtracao = a - b;
        int multiplicacao = a * b;
        int divisao = a / b;

        System.out.println(soma);
        System.out.println(subtracao);
        System.out.println(multiplicacao);
        System.out.println(divisao);
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=59856:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
5
1
6
1 

Process finished with exit code 0
```

**Observe que no caso da divisão apareceu um resultado inesperado: 1 e está errado; porque como a variável declarada é do tipo 'inteiro' o resultado não aceita números decimais, quando o resultado correto seria 1, 5.**

Para corrigir esse problema podemos utilizar 2 modos: 

- mudar todas as variáveis para o tipo `float`; se tivermos muitas linhas de código não é aconselhavél pois, acarretará muito trabalho;

- mudar a variável da divisão para `float` e na atribuição informar que o resultado também é o do tipo `float`, ou seja, casas decimais. Para isso utilizamos a expressão cast, onde escrevo depois do sinal de `atribuição '='`, entre parênteses o tipo da variável declarada: `(float)`; e terei o resultado correto com a casa decimal pedida na divisão: 1,5.

  Ex:

  `float divisão = (float) a / b;`

  ```Java
  package com.example.helloworld;

  public class HelloWorld {
      public static void main(String[] args) {
          int a;
          int b = 2;
          a = 3;

          int soma = a + b;
          int subtracao = a - b;
          int multiplicacao = a * b;
          float divisao = (float) a / b;
        
        	//utilizei o método 'cast' = (float) para informar a variável que o resultado declarado terá casas decimais;

          System.out.println(soma);
          System.out.println(subtracao);
          System.out.println(multiplicacao);
          System.out.println(divisao);
      }
  }

  "C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=59856:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
  5
  1
  6
  1.5

  Process finished with exit code 0
  ```

----

#### Operadores Aritméticos

- soma +
- subtração -
- multiplicação *
- divisão /

----



## Operadores Booleanos|Tabela Verdade

Variáveis que armazenam valores lógicos: verdadeiro ou falso (`true or false`);

Criando um algoritmo para irmos a praia, por exemplo e utilizarmos o operador {**'e'  `&&` (AND)**} teremos a condição esperada abaixo:

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        boolean fimDeSemana = false;
        boolean fazendoSol = false;

        boolean vamosAPraia = fimDeSemana && fazendoSol;
      
      	//Tabela Verdade
        //Operador && (AND)
        //true && true = true
        //true && false = false
        //false && true = false
        //false && false = false
        
        //se todas as condições = true / resultado = true
        //se tiver uma condição = false / todos os resultados = false
      
      	//Operador || (OR = OU) - pipe-pipe
        //true || true = true
        //true || false = true
        //false || true = true
        //false || false = false

        //se tiver uma condição = true / resultado = true
        //se todas condições = false / resultado = false
      
      	//Operador ternário (?) - quando temos duas condições possíveis
        //onde temos uma atribuição condicionado ao valor da variável booleana.
      	//É representando pela "?" (interrogação) e caso contrário ":" (dois pontos),
      	//onde temos 3 termos:
        //primeiro sendo avaliado, por isso a "?": fimDeSemana;
        //segundo o valor caso seja verdadeiro: "É fim de samana";
        //terceiro o valor caso contrário ":" seja falso: "Não é fim de semana";
        
        String mensagem = fimDeSemana ? "É fim de samana" : "Não é fim de semana";
        System.out.println(mensagem);

        System.out.println(vamosAPraia);
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=60582:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
true

Process finished with exit code 0
```

----

#### Tabela Verdade

##### Operador && (AND = E)

```java
true && true = true
true && false = false
false && true = false
false && false = false

se todas as condições = true / resultado = true
se tiver uma condição = false / todos os resultados = false
```

##### Operador || (OR = OU) — pipe-pipe

```java
true || true = true
true || false = true
false || true = true
false || false = false

se tiver uma condição = true / resultado = true
se todas condições = false / resultado = false
```

##### Operador ternário (?) — interrogação / quando temos duas condições possíveis

É um operador utilizando quando temos duas condições possíveis, onde temos uma atribuição condicionado ao valor da variável booleana. É representando pela "**?**" (interrogação) e caso contrário "**:**" (dois pontos), conforme exemplo abaixo onde temos 3 termos:

```java
//representando pela "?" (interrogação) e caso contrário ":" (dois pontos),onde temos 3 termos:
//primeiro sendo avaliado, por isso a "?": fimDeSemana;
//segundo o valor caso seja verdadeiro: "É fim de samana";
//terceiro o valor caso contrário ":" seja falso: "Não é fim de semana";

boolean fimDeSemana = false;

String mensagem = fimDeSemana ? "É fim de samana" : "Não é fim de semana";
System.out.println(mensagem);

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=60687:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Não é fim de semana
false

Process finished with exit code 0
```

----



## Estruturas Condicionais

São estruturas para verificar se uma condição é verdadeira ou falsa.

##### if-else

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        // verificar se aluno aprovado;

        int nota = 70;

        //se nota for maior ou igual a 70, aluno aprovado;
        //utilizamos a condicional if-else;

        if (nota >= 70) {
            System.out.println("Aluno Aprovado!"); //se condição verdadeira: aprovado;
        } else {
            System.out.println("Aluno Reprovado!"); //se não, reprovado;
        }
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=62930:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Aluno Aprovado!

Process finished with exit code 0
---------  
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        // verificar se aluno aprovado;

        int nota = 50;

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=62953:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Aluno Reprovado!

Process finished with exit code 0

```

Quando a condição é falsa, no caso nota **menor que** "`<`", retorna: "`Aluno Reprovado!`"

##### if-else-if-else

Se temos mais de uma condição a ser avaliada usaremos essa opção como forma de avaliação. Criei a `String graduacao;` vazia para ter sua atribuição a medida que as condicionais são avaliadas como `true or false`.

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        // verificar se aluno aprovado;

        int nota = 80;
        String graduacao;

        //condicional if-else-if;
        //notas em graduações: A 80 B 70 C 60 D 0;

        if (nota >= 80) {
            graduacao = "A";
        } else if (nota < 80 && nota >= 70) {
            graduacao = "B";
        } else if (nota < 70 && nota >= 60) {
            graduacao = "C";
        } else if (nota < 60 && nota >= 50) {
            graduacao = "D";
        } else {
            graduacao = ""; //se não for nenhuma condição atender, vazio!
        }
    }
}
```

##### switch

Estrutura que possibilita comparar as condições e imprimir o resultado de acordo com os resultados de `if-else-if-else` em cima do valor da variável `int nota` e a atribuição da variável `String graduacao`. Sempre que o processo é executado, depois de todas as verificações, a cada resultado encontrado que satisfaça o valor da variável int nota, adicionamos um comando `break` (parar) para que interrompa a execução do restante do código e imprima o valor da variável `String graduação` correspondente.

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        // verificar se aluno aprovado;

        int nota = 100;
        String graduacao;

        //condicional if-else-if;
        //notas em graduações: A 80 B 70 C 60 D 0;

        if (nota >= 80) {
            graduacao = "A";
        } else if (nota < 80 && nota >= 70) {
            graduacao = "B";
        } else if (nota < 70 && nota >= 60) {
            graduacao = "C";
        } else if (nota < 60 && nota >= 50) {
            graduacao = "D";
        } else {
            graduacao = ""; //se não for nenhuma condição atender, vazio!
        }

        switch (graduacao) {
            case "A":
            case "B":
                System.out.println("Aluno Aprovado!");
                break; //parar - se verdadeiro, o restante do bloco é interrompido;
            case "C":
            case "D":
                System.out.println("Aluno Reprovado");
                break; //parar - se verdadeiro, o restante do bloco é interrompido;
            default:
                System.out.println("Graduação Inválida!"); //se não mensagem padrão para erro;
        }
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=63280:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Aluno Aprovado!

Process finished with exit code 0
---------  
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        // verificar se aluno aprovado;

        int nota = 60;
        String graduacao;

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=63313:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Aluno Reprovado

Process finished with exit code 0
---------
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        // verificar se aluno aprovado;

        int nota = -1;
        String graduacao;

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=63320:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Graduação Inválida!

Process finished with exit code 0           
```

----



## Manipulação de Strings e Datas

Veremos como podemos manipular as strings e datas dentro do Java, para que a informação seja impressa correta na saída. Ex: `Olá, {nome}. Hoje é {dia-da-semana}, BOM DIA!`

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        //Olá, {nome}. Hoje é {dia-da-semana}, BOM DIA!

        String nome = "Jessé";
        System.out.println(nome.toUpperCase()); //converte para letras maiúsculas;
        System.out.println(nome.toLowerCase()); //converte para letras minúsculas;
        System.out.println(nome.length()); // mostra quantos caracteres tem a string;
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=64304:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
JESSÉ
jessé
5

Process finished with exit code 0
```

No caso acima, algumas do parâmetros que podemos atribuir a uma variável string.

----

Para comparar strings precisamos apenas saber se as iniciais maiúsculas ou minúsculas são relevantes para nosso caso. 

Utilizamos os parâmetro:

- `equals()` - comparar variáveis idênticas;
- `equalsIgnoreCase()` - ignorar as diferenças entre variáveis;

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        //Olá, {nome}. Hoje é {dia-da-semana}, BOM DIA!

        String nome = "Jessé";
        System.out.println(nome.toUpperCase()); //converte para letras maiúsculas;
        System.out.println(nome.toLowerCase()); //converte para letras minúsculas;
        System.out.println(nome.length()); // mostra quantos caracteres tem a string;

        String outroNome = "Jessé";
        System.out.println(nome.equals(outroNome));
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=64430:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
JESSÉ
jessé
5
true

Process finished with exit code 0
---------
String outroNome = "jessé"; //mudei a letra inicial para minúscula;
        System.out.println(nome.equals(outroNome));

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=64430:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
JESSÉ
jessé
5
false

Process finished with exit code 0
---------
String outroNome = "jessé"; //mudei a letra inicial para minúscula;
        System.out.println(nome.equalsIgnoreCase(outroNome));
		//ignora qualquer diferença entre as variáveis;  

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=64430:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
JESSÉ
jessé
5
true

Process finished with exit code 0
```

----

#### Criando o código da frase: 

#### `Olá, {nome}. Hoje é {dia-da-semana}, BOM DIA!`

Para definir a data local, precisamos utilizar propriedade tipo do Java chamada: `LocalDate` que faz parte da **classe** `time`; antes precisamos importar a classe para o nosso código: `import java.time.LocalDate;`

**Forma simples**

```java
package com.example.helloworld;

import java.time.LocalDate;

public class HelloWorld {
    public static void main(String[] args) {
        //Olá, {nome}. Hoje é {dia-da-semana}, BOM DIA!

        String nome = "Jessé";

        //ISO 8601 - padrão de data;
        LocalDate hoje = LocalDate.now(); //importa data local de acordo com a região;
        System.out.println(hoje);
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=64633:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
2022-09-14

Process finished with exit code 0	
```

**Dia da semana padrão inglês**

```java
		LocalDate hoje = LocalDate.now(); //importa data local de acordo com a região;
		System.out.println(hoje.getDayOfWeek()); //importa o dia semana (inglês);

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=64694:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
WEDNESDAY

Process finished with exit code 0
```

**Dia da semana português Brasil**

Para que o dia da semana seja impresso em português, precisamos importar duas classes do Java: `format.TextStyle;` e `Locale;`.

- import java.time.format.TextStyle; — informa o estilo do texto;
- import java.util.Locale; — informa o país;

```java
package com.example.helloworld;

import java.time.LocalDate;
import java.time.format.TextStyle;
import java.util.Locale;

public class HelloWorld {
    public static void main(String[] args) {
        //Olá, {nome}. Hoje é {dia-da-semana}, BOM DIA!

        String nome = "Jessé";

        //ISO 8601 - padrão de data;
        LocalDate hoje = LocalDate.now(); //importa data local de acordo com a região;
        Locale brasil = new Locale("pt", "BR"); //idioma e país;
      	System.out.println(hoje.getDayOfWeek().getDisplayName(TextStyle.FULL, brasil));
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=64834:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
quarta-feira

Process finished with exit code 0
```

**IMPORTANTE:**

![intelliJ7](assets/intelliJ7.jpg)

----

##### Hora local

Para adicionar a hora local, precisamos importar a classe `LocalDateTime` do Java e declarei a *String* `saudacao` sem atribuir valor.

Utilizamos o parâmetro `getHour` para pegar a hora atual e fazemos uma estrutura condicional para comparar a hora e a saudação correta. 

Para saída da frase completa, utilizamos o parâmetro `printf` onde definimos os formatos e os valores a serem impressos:

```java
System.out.printf("Olá, %s. Hoje é %s, %s! %n", nome, diaSemana, saudacao.toUpperCase());
```

**printf** = imprimir em uma única linha, sem quebra; definir os formatos e depois os valores;
**%** = para fazer uma marcação de lugar;
**s** = abreviatura de String;
**%n** = quebra de linha;

```java
Olá, Jessé. Hoje é quarta-feira, BOA TARDE!
```

```java
package com.example.helloworld;

import java.time.LocalDate;
import java.time.LocalDateTime;
import java.time.format.TextStyle;
import java.util.Locale;

public class HelloWorld {
    public static void main(String[] args) {
        //Olá, {nome}. Hoje é {dia-da-semana}, BOM DIA!

        String nome = "Jessé";

        //ISO 8601 - padrão de data;
        LocalDate hoje = LocalDate.now(); //importa data local de acordo com a região;
        Locale brasil = new Locale("pt", "BR"); //language e country (reservadas do IntelliJ);
        //Locale brasil = new Locale("pt", "BR");
        //System.out.println(hoje.getDayOfWeek().getDisplayName(TextStyle.FULL, brasil));

        String diaSemana = hoje.getDayOfWeek().getDisplayName(TextStyle.FULL, brasil);
        String saudacao;

        LocalDateTime agora = LocalDateTime.now();
        if (agora.getHour() >= 0 && agora.getHour() < 12) {
            saudacao = "bom dia";
        } else if (agora.getHour() >= 12 && agora.getHour() < 18) {
            saudacao = "boa tarde";
        } else if (agora.getHour() >= 18 && agora.getHour() < 24) {
            saudacao = "boa noite";
        } else {
            saudacao = "Olá.";
        }
        //printf = imprimir em única linha, sem quebra; definir os formatos e depois os valores;
        //"%" = para fazer uma marcação de lugar;
        //"s" = abreviatura de String;
        //%n = quebra de linha;
        System.out.printf("Olá, %s. Hoje é %s, %s! %n", nome, diaSemana, saudacao.toUpperCase());
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=50525:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Olá, Jessé. Hoje é quarta-feira, BOA TARDE! 

Process finished with exit code 0
```

----



## Laços Numéricos 

***Laços numéricos*** ou ***repetições contadas***, são estruturas onde queremos repetir um trecho do código por uma quantidade repetida de vezes. 

#### for

```java
for (int i = 1; i <= 10; i++) {
	System.out.println(i);
}
```

**int i = 1;** — declarei a variável i e atribui o valor 1;

**i <= 10;** — enquanto i for menor ou igual a 10;

**i++** — "++" incrementar, somar + 1 a i;

**i+=2** — incrementar, somar + 2 a i;

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        // 1 2 3 4 5 6 7 8 9 10;
        // para uma variável que inicia em 1 e vai até 10, mudando 1-por-1, faça:

        /* criei a condição "for" e declarei a variável int i = 1;
        depois declarei que enquanto i é menor ou igual a 10, incrementa "++", soma + 1 */
      
        for (int i = 1; i <= 10; i++) {
            System.out.println(i);
        }
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=50708:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
1
2
3
4
5
6
7
8
9
10

Process finished with exit code 0
```

#### Aninhar laços utilizando for

**IMPORTANTE**: a variável **int i** não pode ser declarada 2x. É comum utilizar as letras do alfabeto sequenciais a **i**, no caso: **j**, **k**, **l**, **m**. Cuidado para não criar ninhos demais e deixar o código complexo.

**TABUADA**

**Laço aninhado**: o valor da variável **i** só mudará depois, que todas a iterações da variável **j** que está dentro dela terminarem.

```java
for (int i = 1; i <= 10; i++) {
    for (int j = 1; j <= 10; j++) {
        System.out.println(j + "x" + i + "=" + j * i);
        //1x1=1
        //2x1=2
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=51034:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
1x1=1
2x1=2
3x1=3
4x1=4
5x1=5
6x1=6
7x1=7
8x1=8
9x1=9
10x1=10
... até 100  
```

----



## Vetores ou Arrays

O Java é uma linguagem fortemente tipada, não podemos misturas tipos dentro de um array. 

**Se declarar um array do tipo string ou inteiro, todos os elementos dentro do array tem q seguir o mesmo tipo declarado.**

**Arrays tem tamanho imutável.** Se declaro um array com 5 elementos, só posso declarar 5 elementos.

São manipulados por **índices** a partir da posição "`0`". 

**Num array o primeiro índice é o "0" e o último é tamanho -1**, ou seja, num array com 10 elementos, o primeiro índice é o **"0"** e o último é **"9"**.

Ex: `[0] [1] [2] [3] [4] [5] [6] [7] [8] [9] `

Para imprimir o elementos de um array, precisamos colocá-los em um **for** (*laço numérico*);

- declarar o início do índice `int i = 0;` 
- informar q enquanto o índice for menor que o tamanho do array `i < numeros.length;`
- incrementa + 1 `i++;`

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        int[] numeros = new int[5];
        //[1] [2] [3] [4] [5]
        numeros[0] = 1;
        numeros[1] = 2;
        numeros[2] = 3;
        numeros[3] = 4;
        numeros[4] = 5;
        for (int i = 0; i < numeros.length; i++) {
            System.out.println(numeros[i]);
        }
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=65275:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
1
2
3
4
5

Process finished with exit code 0
```

Mesma coisa acontece com um array de **String**.

**IMPORTANTE**: todas as declarações precisam ser do tipo `String`.

```Java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        String[] letras = new String[5];
        //[A] [D] [F] [K] [Z]
        letras[0] = "A";
        letras[1] = "D";
        letras[2] = "F";
        letras[3] = "K";
        letras[4] = "Z";

        for (int i = 0; i < letras.length; i++) {
            System.out.println(letras[i]);
        }
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=65391:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld

A
D
F
K
Z

Process finished with exit code 0
```

##### Forma simplificada

Se já soubermos todos os elementos que quero adicionar ao array, podemos usar a notação (entre chaves)  **{ }**. O Java entenderá preciso criar um **array em 5 posições**, qual o **tipo do array** e já **atribui o valor a cada posição**.

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
      	//[A] [D] [F] [K] [Z]
        String[] letras = { "A", "D", "F", "K", "Z" };
        for (int i = 0; i < letras.length; i++) {
            System.out.println(letras[i]);
        }
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=49227:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
A
D
F
K
Z

Process finished with exit code 0
```

##### Forma compacta

Utilizando o parâmetro de impressão e declarando o array, dessa forma não precisamos utilizar o *laço numérico* **for**.

IMPORTANTE: é preciso importar a classe `Arrays` do java antes de declarar.

```java
import java.util.Arrays; //classe do Java
```

O Java estrutura o array de acordo com o parâmetro de impressão `println`, ou seja, **imprime em uma linha**.

```java
System.out.println(Arrays.toString(letras));
```

```java
package com.example.helloworld;

import java.util.Arrays; //classe do Java

public class HelloWorld {
    public static void main(String[] args) {
      	//[A] [D] [F] [K] [Z]
        String[] letras = { "A", "D", "F", "K", "Z" };
        System.out.println(Arrays.toString(letras));
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=49279:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
[A, D, F, K, Z]

Process finished with exit code 0
```

##### Como saber num array: maior elemento, menor elemento e a média entre eles

Como já sabemos os elementos do array, declaramos a variável com atribuição dos valores definidos entre chaves **{ }**: `int[] numeros = { 9, 10, 12, 25, 2 };`

Declarei as variáveis: `maior`, `menor` e `média`; todas com atribuições de índice 0 para o array ter um ponto de partida.

**IMPORTANTE**: a variável média foi declarada com tipo **float**, para resultado com números decimais.

Utilizei *laço numérico* **for** para realizar as comparações; dentro dele criei as condicionais **if** para iterar os elementos e saber qual é o maior e o menor.

Na variável media, somei e atribuí a variável números e seu índice: `media += numeros[i] ;`

(`+=`)  **operador aritmético para somar e atribuir**: `media = media + numeros[i];`

Utilizei o parâmetro `println` para saída dos valores: **Maior**, **Menor** e a **Média**.

Para o resultado da média, fiz a divisão pela soma dos elementos dividido pelo tamanho dos array:

```java
System.out.println("Maior: " + maior);
System.out.println("Menor: " + menor);
System.out.println("Média: " + media/numeros.length); //soma dividido pelo tamanho do array
```
```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
        int[] numeros = { 9, 10, 12, 25, 2 };
        int maior = numeros[0];
        int menor = numeros[0];
        float media = 0; //variável tipo float para resultado com casas decimais;

        for (int i=0; i < numeros.length; i++) {
            if (numeros[i] > maior) {
                maior = numeros[i];
            }
            if (numeros[i] < menor) {
                menor = numeros[i];
            }
            media += numeros[i]; // += somar e atribuir;
        }
        System.out.println("Maior: " + maior);
        System.out.println("Menor: " + menor);
        System.out.println("Média: " + media/numeros.length);
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=51088:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Maior: 25
Menor: 2
Média: 11.6

Process finished with exit code 0
```

----



## Funções

Sempre numa aplicação Java o ponto de partida é o escopo `main`, todo código está escrito dentro dele. As **funções** no Java se chamam **métodos**. 

Criamos a **função** *(método)* fora do escopo `main` porém, a invocação, chamada da **função** *(método)* é dentro dele.

```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) {
       saudacao(); //função(método) sem parâmetros invocada dentro escopo main;
    }
    public static void saudacao() { //função(método) criado fora do escopo main;
        System.out.println("Hello, Jessé");
    }
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=52415:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Hello, Jessé

Process finished with exit code 0
```

##### Escopo de variável

É determinado pelo par de chaves "**{ }**". A variável que está declarada e a função dentro do *escopo* tem que ter o mesmo nome, para manter a coerência. Não existe nenhuma relação entre a variável `nomeOriginal` e a `nomeParametro` pois, estão em *escopos* diferentes.

**Escopo `main`**

```java
public static void main(String[] args) {
       String nomeOriginal = "Let's Code"; 
       saudacao(nomeOriginal);
} //variável e função com o mesmo nome;
```

**Escopo função `saudacao`**

```java
public static void saudacao(String nomeParametro) {
    System.out.println("Hello, " + nomeParametro);
} //função e saída com o mesmo nome;
```
```java
package com.example.helloworld;

public class HelloWorld {
    public static void main(String[] args) { //variável e função com o mesmo nome;
       String nomeOriginal = "Let's Code"; 
       saudacao(nomeOriginal);
    } //escopo main;
  
    public static void saudacao(String nomeParametro) { //função e saída com o mesmo nome;
        System.out.println("Hello, " + nomeParametro);
    } //escopo função saudacao;
}

"C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=52488:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
Hello, Let's Code.

Process finished with exit code 0
```

Podemos definir funções:

- **não recebem parâmetros** —  `saudacao ()`

  ```java
  public static void saudacao() {
      System.out.println("Hello, Jessé");
  }
  ```

- **recebem PARÂMETROS** — `saudacao(String nomeParametro)`

  ```java
  public static void saudacao(String nomeParametro) {
      System.out.println("Hello, " + nomeParametro);
  }
  ```

- **retornam VALORES** — `int soma (int a, int b) {return a + b;}`

  Para retornar valores utilizamos a palavra return no escopo da função;

  ```java
  package com.example.helloworld;

  public class HelloWorld {
      public static void main(String[] args) { //declarei a variável resultado;
         int resultado = soma(2, 3);
          System.out.println(resultado); //resultado da operação no terminal 
      }

    	//criei a função para executar a soma e retornar o valor;
      public static int soma(int a, int b) {
          return a + b;
      }
  }

  "C:\Program Files\Java\jdk-18.0.2.1\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\lib\idea_rt.jar=52569:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.2.1\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath C:\Users\sleep\IdeaProjects\HelloWorld\out\production\HelloWorld com.example.helloworld.HelloWorld
  5

  Process finished with exit code 0
    
  ```

Para definir uma função temos:

- nome: **public static int soma( )** 

- parâmetros entre parênteses `( )`: **public static int soma(int a, int b)**

- chaves `{ }` para determinar o escopo e seu conteúdo:

  **public static int soma(int a, int b) {**

  ​	return a + b;

  **}**

----

