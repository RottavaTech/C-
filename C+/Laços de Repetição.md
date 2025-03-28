As instruções de iteração executam uma instrução ou um bloco de instruções repetidas vezes. A [instrução `for`](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/statements/iteration-statements#the-for-statement) executa o bloco correspondente enquanto uma expressão booliana especificada é avaliada como `true`. A [instrução `foreach`](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/statements/iteration-statements#the-foreach-statement) enumera os elementos de uma coleção e executa o bloco correspondente para cada elemento dessa coleção. A [instrução `do`](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/statements/iteration-statements#the-do-statement) executa condicionalmente o bloco correspondente uma ou mais vezes. A [instrução `while`](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/statements/iteration-statements#the-while-statement) executa condicionalmente o bloco correspondente zero ou mais vezes.

A qualquer momento dentro do corpo da instrução de iteração, interrompa o loop usando a [instrução `break`](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/statements/jump-statements#the-break-statement). Você pode passar para a próxima iteração no loop usando a [instrução `continue`](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/statements/jump-statements#the-continue-statement).

## for
A instrução `for` executa uma instrução ou um bloco de instruções enquanto uma expressão booliana especificada é avaliada como `true`. O seguinte exemplo mostra a instrução `for` que executa o corpo dela enquanto um contador inteiro é menor que três:

`for (int i = 0; i < 3; i++)`
`{`
    `Console.Write(i);`
`}`

`// Output:`
`// 012`

O exemplo anterior mostra os elementos da instrução `for`:

- A seção _inicializador_ é executada apenas uma vez, antes de entrar no loop. Normalmente, você declara e inicializa a variável local do loop nessa seção. A variável declarada não pode ser acessada de fora da instrução `for`.
    
    A seção _inicializador_ do exemplo anterior declara e inicializa a variável do contador inteiro: `int i = 0` e verifica se o valor do contador é menor que três `i < 3`

A principal diferença entre os loops for e while em C# é que o for é usado quando se sabe o número de iterações, enquanto o while é usado quando não se sabe.
## foreach
#### 🔹 **O que é `foreach`?**

O **`foreach`**é uma estrutura de repetição usada para percorrer **coleções** de dados de forma simplificada. Ele percorre **cada elemento** da coleção e executa um bloco de código para cada um.

#### ✅ **Exemplo simples de`foreach`**

`string[] frutas = { "Maçã", "Banana", "Laranja" };  
foreach (string fruta in frutas) 
{     
Console.WriteLine(fruta); 
}`

#### 🟢 **Saída**

`Maçã 
Banana 
Laranja`

💡 **Explicação**

- Olhe **`foreach`**cada item da lista `frutas`.
    
- A variável `fruta`assume o valor do **elemento atual** em cada iteração.
    
- O código dentro do `foreach`é executado para cada item da lista.
## while

A instrução `while` executa uma instrução ou um bloco de instruções enquanto uma expressão booliana especificada é avaliada como `true`. Como essa expressão é avaliada antes de cada execução do loop, um loop `while` é executado zero ou mais vezes. Esse loop `while` é diferente do [loop `do`](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/statements/iteration-statements#the-do-statement), que é executado uma ou mais vezes.

O seguinte exemplo mostra o uso da instrução `while`:

`int n = 0;`
`while (n < 5)`
`{`
    `Console.Write(n);`
    `n++;`
`}`

`// Output:`
`// 01234`
## switch
#### 🔹 **Explicação do `switch-case`em C# com comparação ao seu código**

O `switch-case`é uma estrutura de controle de fluxo em C# usada para executar diferentes blocos de código com base no valor de uma variável. Ele funciona como uma alternativa ao `if-else`, tornando o código mais organizado e legível quando há várias condições a serem avaliadas.

---
#### ✅ **Sintaxe básica do`switch-case`**

`switch (variavel)`
`{`
    `case "opcao1":`
        `// Código para opção 1`
        `break;`
    `case "opcao2":`
        `// Código para opção 2`
        `break;`
    `default:`
        `// Código para qualquer outra opção`
        `break;`
`}`

- A **variável** entre paisentre parênteses ( `switch (variavel)`) será comprovado.
    
- O **`case`**compare se a variável tem o valor especificado.
    
- O **`break`**encerra a execução do bloco do `case`, evitando que o código continue para os próximos `case`.
    
- O **`default`**funciona como um "plano B", sendo executado se nenhum dos `case`correspondentes.

---
#### 📌 **Comparação com seu código**

Vamos analisar como o `switch-case`está sendo usado em sua calculadora e o que ele faz.

#### 🔎 **Trecho do seu código que usa`switch-case`**

`decimal resultado = operador switch`
`{`
    `"+" => soma(numero1, numero2),`
    `"-" => sub(numero1, numero2),`
    `"*" => mult(numero1, numero2),`
    `"/" => div(numero1, numero2),`
    `_ => 0 // Nunca chega aqui, pois já validamos o operador antes`
`};`

tradicional ,🚀 **Aqui, ao invés do uso `switch-case`tradicional, seu código usa o "switch expression", um recurso moderno do C# 8.0.**  
💡 O "switch expression" substitui o `switch-case`tradicional, deixando o código mais compacto e legível.

#### 🔄 **Comparação entre `switch expression`e `switch-case`tradicional**

#### 🔹 **Usando `switch expression`(seu código)**

`decimal resultado = operador switch`
`{`
    `"+" => soma(numero1, numero2),`
    `"-" => sub(numero1, numero2),`
    `"*" => mult(numero1, numero2),`
    `"/" => div(numero1, numero2),`
    `_ => 0`
`};`

✅ **Vantagens:**

- Código mais curto e direto.
    
- .Menos repetições de `break`.
    
- Fácil de entender para operações simples.

#### 🔸 **Usando `switch-case`tradicional**

Se o código fosse escrito no formato `switch-case`, ficaria assim:

`decimal resultado;`
`switch (operador)`
`{`
    `case "+":`
        `resultado = soma(numero1, numero2);`
        `break;`
    `case "-":`
        `resultado = sub(numero1, numero2);`
        `break;`
    `case "*":`
        `resultado = mult(numero1, numero2);`
        `break;`
    `case "/":`
        `resultado = div(numero1, numero2);`
        `break;`
    `default:`
        `resultado = 0;`
        `break;`
`}`

✅ **Vantagens do `switch-case`tradicional:**

- Mais flexível, pois permite incluir mais lógica em cada `case`.
    
- ,Fácil de depurar, pois cada um `case`pode ter várias linhas de código.
    
- Mais intuitivo para iniciantes em C#.