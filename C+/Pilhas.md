#### ✅ **Criando uma aula de Pilha em C#**

Vamos construir uma classe `Pilha`, que terá:

- **Uma lista privada** para armazenar os números ( `List<decimal>`)
    
- **O método`Push(decimal valor)`** → Para empilhar um número.
    
- **O método`Pop()`** → Para desempilhar e retornar o último número adicionado.
    

---

#### 📌 **Código da classe`Pilha`**

`using System;`
`using System.Collections.Generic;`

`class Pilha`
`{`
    `private List<decimal> elementos = new List<decimal>(); // Lista privada para armazenar os números`

    `// Método para empilhar (adicionar um número na pilha)`
    `public void Push(decimal valor)`
    `{`
        `elementos.Add(valor);`
        `Console.WriteLine($"Empilhado: {valor}");`
    `}`

    `// Método para desempilhar (remover o último número da pilha)`
    `public decimal Pop()`
    `{`
        `if (elementos.Count == 0) // Verifica se a pilha está vazia`
        `{`
            `throw new InvalidOperationException("A pilha está vazia!"); // Erro caso não tenha elementos`
        `}`

        `decimal ultimo = elementos[elementos.Count - 1]; // Pega o último elemento`
        `elementos.RemoveAt(elementos.Count - 1); // Remove o último elemento da lista`
        `Console.WriteLine($"Desempilhado: {ultimo}");`
        `return ultimo; // Retorna o número removido`
    `}`
`}`

---
#### 📌 **Explicação do Código**

#### 🔎 **Atributo privado**

`private List<decimal> elementos = new List<decimal>();`

- Criamos uma **lista privada** ( `List<decimal>`) para armazenar os valores da pilha.
    
- Ela é **privada** , então **não pode ser acessada diretamente de fora da aula** .

---

#### 🔎 **Método `Push(decimal valor)`→ Empilhar um número**

`public void Push(decimal valor)`
`{`
    `elementos.Add(valor);`
    `Console.WriteLine($"Empilhado: {valor}");`
`}`

- O método recebe um número `decimal`como parâmetro.
    
- Esse número é **adicionado à lista ( `elementos.Add(valor)`)** , ficando no topo da pilha.

---

#### 🔎 **Método `Pop()`→ Desempilhar um número**

`public decimal Pop()`
`{`
    `if (elementos.Count == 0) // Verifica se a pilha está vazia`
    `{`
        `throw new InvalidOperationException("A pilha está vazia!");`
    `}`

    `decimal ultimo = elementos[elementos.Count - 1]; // Pega o último número adicionado`
    `elementos.RemoveAt(elementos.Count - 1); // Remove o último número da lista`
    `Console.WriteLine($"Desempilhado: {ultimo}");`
    `return ultimo; // Retorna o número removido`
`}`

- **Verifique se a pilha está vazia** antes de remover ( `if (elementos.Count == 0)`).
    
- Se não estiver vazio:
    
    - **Pega o último número** ( `elementos[elementos.Count - 1]`).
        
    - **Remova esse número da lista** ( `elementos.RemoveAt(elementos.Count - 1)`).
        
    - **Retorna o número removido** .

---
#### ✅ **Criando um Teste para a Pilha**

Agora, vamos testar nossa classe `Pilha`dentro do `Main()`, empilhando e desempilhando valores.

`class Program`
`{`
    `static void Main()`
    `{`
        `Pilha minhaPilha = new Pilha(); // Criamos uma pilha`

        `Console.WriteLine("Testando a Pilha...\n");`

        `minhaPilha.Push(10); // Empilha 10`
        `minhaPilha.Push(20); // Empilha 20`
        `minhaPilha.Push(30); // Empilha 30`

        `minhaPilha.Pop(); // Remove o último número (30)`
        `minhaPilha.Pop(); // Remove o último número (20)`

        `minhaPilha.Push(40); // Empilha 40`
        `minhaPilha.Pop(); // Remove o último número (40)`
    `}`
`}`

---

#### 📌O **que vai acontecer ao executar esse código?**

`Testando a Pilha...  Empilhado: 10 Empilhado: 20 Empilhado: 30 Desempilhado: 30 Desempilhado: 20 Empilhado: 40 Desempilhado: 40`

✔️ **Funcionamento correto da pilha!**

---
#### 📌 **Comparação com seu código original**

🔹O **que já tem seu código?**

- Você já usa **métodos ( `soma`, `sub`, `mult`, `div`)** , o que mostra que entende bem a estrutura de classes e métodos.

🔹 **Novidade para você aqui:**

- **Uso de uma lista privada ( `List<decimal>`)**
    
- **Manipulação de estrutura de dados ( `Push`e `Pop`)**
    
- **Validação para evitar erros ao tentar remover uma pilha vazia**

---
#### ✅ **Resumo**

|Método|O que faz?|Como funciona?|
|---|---|---|
|`Push(decimal valor)`|Adiciona um número na pilha|`elementos.Add(valor);`|
|`Pop()`|Remova o último número e retorna ele|`elementos.RemoveAt(elementos.Count - 1);`|
|`Count`|Retorna o número de elementos na pilha|`elementos.Count`|
