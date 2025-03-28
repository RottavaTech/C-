#### 🧠**Explicação Completa sobre o Método`.Count`** 🧠📚

O método `.Count`é usado em coleções (como listas, arrays e outros tipos de coleções em C#) para retornar a quantidade de elementos armazenados nelas. Em resumo, ele **conta quantos itens existem dentro da estrutura de dados** .

---
#### 🛠 **Como funciona `.Count`em uma`List<T>`**

Em C#, quando você tem um `List<T>`, o método `.Count`é **uma propriedade** que retornaque retorna o número total de elementos da lista.
#### 🔹 **Exemplo Simples**

`List<int> numeros = new List<int> { 5, 10, 15, 20 }; Console.WriteLine(numeros.Count); // Saída: 4`

🔹 A lista contém **4 números** , então `numeros.Count`retorna **4** .
#### 🔹 **Exemplo: Lista vazia**

Se uma lista estiver vazia, o `.Count`retorna **0** :

`List<int> numeros = new List<int>(); // Lista vazia Console.WriteLine(numeros.Count); // Saída: 0`

---
#### **⚡ Diferença entre `.Count`e`.Length`**

#### 🔹 **`.Count`→ Usado para coleções (Lista, Dicionário, etc.)**

`List<int> lista = new List<int> { 1, 2, 3 }; Console.WriteLine(lista.Count); // Saída: 3`

---
#### 🔹 **`.Length`→ Usado para Arrays**

`int[] array = { 1, 2, 3 }; Console.WriteLine(array.Length); // Saída: 3`

✅ `.Count`é para **listas**  
✅ `.Length`é para **matrizes**

---
#### **📌 Como usamos `.Count`na sua calculadora RPN?**

No seu código, usamos `.Count`para verificar **quantos números estão empilhados na pilha** , antes de realizar operações matemáticas.

#### **🚨 Importante: Evitar erro ao desempilhar**

Se tentarmos desempilhar um número sem ter pelo menos **dois** na pilha, o código daria erro. Por isso, usamos:

`if (pilha.Quantidade() < 2) {     Console.WriteLine("Erro: Operação inválida, não há elementos suficientes na pilha.");     return; }`

Essa verificação acontece com o método `.Quantidade()`, que na verdade retorna `.Count`da lista:

`public int Quantidade() {     return Lista_Decimais.Count; // Retorna o número total de elementos na pilha }`

---
#### **🚀 Exemplo Completo usando`.Count`**

Aqui está um exemplo prático de como `.Count`pode ser útil:

`List<string> nomes = new List<string> { "Ana", "Bruno", "Carlos" };`  

`Console.WriteLine($"Total de nomes: {nomes.Count}");  // Saída: 3`  

`// Removendo um nome` 
`nomes.Remove("Ana");`  

`Console.WriteLine($"Agora temos {nomes.Count} nomes na lista."); // Saída: 2`

A lista está vazia:

`nomes.Clear(); // Remove tudo Console.WriteLine(nomes.Count); // Saída: 0`