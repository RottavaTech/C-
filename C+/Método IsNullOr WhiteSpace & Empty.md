## WhiteSpace

- Verifica se uma string é nula, vazia ou contém apenas espaços em branco 
- Retorna true se a string for nula, vazia ou conter apenas espaços em branco, e false caso contrário

O código abaixo verifica se o usuário **não digitou nada** ou apenas espaços em branco antes de processar a entrada:

`if (string.IsNullOrWhiteSpace(entrada)) {     Console.WriteLine("Entrada inválida! Tente novamente.");     continue; }`

### **🛠 O que esse código faz?**

1. **`string.IsNullOrWhiteSpace(entrada)`verifica se a entrada está vazia ou contém apenas espaços.**
    
    - Se `entrada`for `null`, estiver vazio ( `""`), ou contiver apenas espaços ( `" "`), a condição será **verdadeira** .
        
2. Se a condição for verdadeira:
    
    - Mostra a mensagem`"Entrada inválida! Tente novamente."`
        
    - O `continue;`faz o programa **voltar para o início do`while`** , sem processar o restante do código.
        

---

### **📌Quando essa mensagem aparece?**

Ela será exibida se o usuário: ✅ **Abrir apenas "Enter" sem digitar nada**  
✅ **Digitar apenas espaços e iniciar "Enter"**

**Exemplos de entrada inválida:**

`(pressionar Enter sem digitar nada)`

`(pressionar espaço algumas vezes e depois Enter)`

Isso impede que o programa tente processar uma entrada vazia e evitar erros.
## Empty
### **🔹 `string.IsNullOrEmpty()`– O que é?**

O método `string.IsNullOrEmpty(variável)`é usado para verificar **se uma string está vazia ( `""`) ou é`null`** .

Ele retorna:

- **`true`**se uma string para **`null`ou`""`** (vazia).
    
- **`false`**se uma string tiver qualquer valor.
    

📌 **Forma de uso:**

c sustenido

CopiarEditar

`bool resultado = string.IsNullOrEmpty(texto);`

Aqui, **você**`resultado` estará **vazio ou for** .`true` **`texto``null`**

---

#### **🔹 Como funciona no seu código?**

No seu código, temos esta parte:

`if (string.IsNullOrWhiteSpace(entrada)) {     Console.WriteLine("Entrada inválida! Tente novamente.");     continue; }`

Esse código verifica se **`entrada`está vazio ou só contém espaços** .

Podemos substituir `string.IsNullOrWhiteSpace(entrada)`por `string.IsNullOrEmpty(entrada)`, mas com uma diferença:

- **`IsNullOrEmpty()`**→ só detecta **`null`ou`""`** (vazio).
    
- **`IsNullOrWhiteSpace()`**→ detecta **`null`, `""`, `" "`(espaços em branco)** .
    

Se no seu código um usuário digitar **apenas espaços** , `IsNullOrEmpty()` **não impediria isso** , mas `IsNullOrWhiteSpace()`sim.

---

#### **🔹 Exemplos Práticos**

#### ✅ **Exemplo 1 – Verificando Strings**

`string texto1 = null; string texto2 = ""; string texto3 = "Olá";  Console.WriteLine(string.IsNullOrEmpty(texto1)); // true (é null) Console.WriteLine(string.IsNullOrEmpty(texto2)); // true (é "") Console.WriteLine(string.IsNullOrEmpty(texto3)); // false (tem valor "Olá")`

#### ✅ **Exemplo 2 – Aplicação no seu código**

Se o usuário não digitar nada e apertar `Enter`, o programa detecta que a entrada está vazia:

`string entrada = Console.ReadLine(); if (string.IsNullOrEmpty(entrada)) {     Console.WriteLine("Entrada inválida! Tente novamente."); }`

---

#### **🔹 Diferença entre `IsNullOrEmpty()`e`IsNullOrWhiteSpace()`**

|Método|Retorna `true`quando...|Retorna `false`quando...|
|---|---|---|
|`IsNullOrEmpty()`|String é `null`ou ``""`(vazia)|String tem`" "`|
|`IsNullOrWhiteSpace()`|String é `null`, ``""`ou só tem espaços`" "`|String tem pelo menos um caractere vis|

📌 **Exemplo prático comparando os dois:**

`string teste = "   ";  Console.WriteLine(string.IsNullOrEmpty(teste)); // false (tem espaços) Console.WriteLine(string.IsNullOrWhiteSpace(teste)); // true (só tem espaços)`

---

#### **📌 Resumo Final**

✅ **`string.IsNullOrEmpty(variável)`verifica se uma string é `null`ou `""`(vazia).**  
✅ **Se precisar detectar espaços em branco também, use `string.IsNullOrWhiteSpace(variável)`.**  
✅ **No seu código, `IsNullOrWhiteSpace()`é mais útil para evitar entradas inválidas.**
