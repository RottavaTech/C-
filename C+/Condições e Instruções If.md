C# suporta as condições lógicas usuais da matemática:

- Menor que: a < b
- Menor ou igual a: a <= b
- Maior que: a > b
- Maior ou igual a: a >= b
- Igual a a == b
- Não é igual a: a != b

Você pode usar essas condições para executar ações diferentes para decisões diferentes.

C# tem as seguintes instruções condicionais:

- Use `if`para especificar um bloco de código a ser executado, se uma condição especificada for verdadeira
- Use `else`para especificar um bloco de código a ser executado, se a mesma condição for falsa
- Use `else if`para especificar uma nova condição a ser testada, se a primeira condição for falsa
- Use `switch`para especificar muitos blocos alternativos de código a serem executados

## if (se)
Use a `if`instrução para especificar um bloco de código C# a ser executado se uma condição for `True`.

Sintaxe

```csharp
if (condition) 
{
  // block of code to be executed if the condition is True
}
```

No exemplo abaixo, testamos dois valores para descobrir se 20 é maior que 18. Se a condição for `True`, imprima algum texto:

Exemplo 1

```csharp
if (20 > 18) 
{
  Console.WriteLine("20 is greater than 18");
}
```
Também podemos testar variáveis:

Exemplo 2

```csharp
int x = 20;
int y = 18;
if (x > y) 
{
  Console.WriteLine("x is greater than y");
}
```



## else (se não)

Use a `else`instrução para especificar um bloco de código a ser executado se a condição for `False`.

Sintaxe

```csharp
if (condition)
{
  // block of code to be executed if the condition is True
} 
else 
{
  // block of code to be executed if the condition is False
}
```

Exemplo

```csharp
int time = 20;
if (time < 18) 
{
  Console.WriteLine("Good day.");
} 
else 
{
  Console.WriteLine("Good evening.");
}
// Outputs "Good evening."
```

Exemplo explicado:

No exemplo acima, o tempo (20) é maior que 18, então a condição é `False`. Por isso, passamos para a `else`condição e imprimimos na tela "Boa noite". Se o tempo fosse menor que 18, o programa imprimiria "Bom dia".