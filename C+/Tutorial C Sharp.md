### Variáveis, Métodos, Classes e Operadores de Comparação, Lógicos e Aritméticos

#### 🔹 1. Variáveis ​​em C

##### O que é uma variável ?

Uma variável é **um espaço na memória do computador que armazena um valor** .  
Ela tem:

- **Um tipo** ((por exemplo: `int`, `string`, `decimal`).
    
- **Um nome** ((por exemplo: `numero`, `resultado`).
    
- **Um valor armazenado** (ex: `10`, `"Olá"`).

#### **📌 Exemplo no seu Código**

`bool nm1Valido = decimal.TryParse(partes[0], out decimal nm1); bool nm2Valido = decimal.TryParse(partes[1], out decimal nm2);`

Aqui temos:

- `nm1Valido`: uma **variável do tipo`bool`** (guarda `true`ou `false`).
    
- `nm1`: uma **variável do tipo`decimal`** (números de loja com casas decimais).
    
- `nm2Valido`: verifica se a conversão deu certo ( `true`) ou falhou ( `false`).
    
- `nm2`: guarda o segundo número digitado.

---

#### 🔹 2. O que é um Método?**

Um **método** é um bloco de código que executa uma tarefa específica. Ele pode:

- Receber valores de entrada ( **parâmetros** ).
    
- Retornar um valor como resposta.
    
- Ser chamado quantas vezes for necessário.

#### **📌 Exemplo prático**

`static decimal Somar(decimal a, decimal b)  {     return a + b; }`

- O método `Somar`recebe **dois números** ( `a`e `b`).
    
- Ele **retorna a soma** deles com `return a + b;`.

#### **📌 Como usar o código?**

`decimal resultado = Somar(10, 5); // resultado = 15`

---
#### 🔹 3. O que é uma Classe?**

Uma **classe** é um **modelo** para criar objetos. Ela agrupa **métodos e variáveis** .

#### **📌 No seu código**

`class Calculadora {     static void Main()     {         // Código aqui     } }`

Aqui, `Calculadora`é uma classe que contém o método `Main()`.  
Ela **organiza o código** e pode armazenar métodos como `Somar()`.

---
#### 🔹 4. Lista de Operadores C#**

Aqui estão os operadores básicos que você encontrará em C#.

#### **🔸 Operadores de Comparação**

|Operador|Significado|
|---|---|
|`==`|Igual|
|`!=`|Diferente|
|`>`|Maior que|
|`<`|Menor que|
|`>=`|Maior ou|
|`<=`|Menor|

#### **🔸 Operadores Lógicos**

| Operador | Significado    |
| -------- | -------------- |
| `&&`     | E              |
| `!`      | Negação lógica |

#### **🔸 Operadores Aritméticos**

|Operador|Significado|
|---|---|
|`+`|Soma|
|`-`|Subtração|
|`*`|Multip*|
|`/`|Divisão|
|`%`|Módulo (restante da|

---

#### **📌 Resumo Final**

✅ **Variáveis** ​​armazenadas em valores e tipos ( `int`, `string`, `decimal`).  
✅ **Métodos** que executam ações e podem retornar valores ( `return`).  
✅ **Classes** organizam código e contêm métodos.  
✅impedir **`?.`**erro se a variável for `null`.  
✅ **`Length`**conte quantos elementos existem em um array ou string.  
✅ **`IndexOf`**encontra a posição de um caractere dentro de uma string.  
✅ **Operadores** realizam comparações, cálculos e verificações lógicas.