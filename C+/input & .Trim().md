#### **O que é `input` e para que ele serve?**

O **input** é qualquer dado que um programa recebe do usuário ou de outra fonte. No seu código, `Console.ReadLine()` está sendo usado para capturar **input do usuário** no terminal.

🔹 **Exemplo de input:**  
O usuário digita:

10/5

O programa lê essa entrada e pode processá-la.

📌 **Usamos `input` para**:

- Pedir dados ao usuário (números, textos, comandos).
    
- Processar informações com base no que foi digitado.

#### **O que é `.Trim()` e por que usar?**

O `.Trim()` é um método que remove **espaços em branco do início e do fim de uma string**. Isso evita problemas caso o usuário digite espaços acidentais antes ou depois do valor.

🔹 **Exemplo sem `.Trim()`**

`string input = "  10/5  "; // Tem espaços extras Console.WriteLine($"Sem Trim: '{input}'");`


💡 A string contém espaços antes e depois, que podem atrapalhar comparações.

🔹 **Exemplo com `.Trim()`**

`string input = "  10/5  ".Trim(); Console.WriteLine($"Com Trim: '{input}'");`


✅ Agora `input` será `"10/5"` sem espaços extras.

📌 **Usamos `.Trim()` para**:

- Evitar erros ao comparar strings (`if (input == "sair")`).
    
- Melhorar a experiência do usuário.
    

💡 Existe também:

- `.TrimStart()` → Remove apenas os espaços do **início**.
    
- `.TrimEnd()` → Remove apenas os espaços do **final**.