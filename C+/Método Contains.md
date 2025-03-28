#### 🔹 **O que é `Contains`em C#?**

verifica seO método **`Contains`**verifica se uma **lista( `List<>`)** ou **string** contém umcontém um determinado **valor** . Ele retorna `true`se o valor estiver presente e `false`caso contrário.

---
#### ✅ **`Contains`com Listas ( `List<T>`)**

Quando usamos `Contains`listas **,** ele verifica se **um determinado elemento** está na lista.

### 🟢 **Exemplo**

`List<string> cores = new List<string> { "Vermelho", "Azul", "Verde" };  
if (cores.Contains("Azul")) 
{    
Console.WriteLine("A cor está na lista!"); 
} 
else 
{    
Console.WriteLine("A cor não está na lista."); 
}`

### 🔹 **Saída**

`A cor está na lista!`

💡 **Explicação**

- A lista `cores`contém `"Azul"`, então `Contains("Azul")`retorna `true`e imprime `"A cor está na lista!"`.

---
#### ✅ **`Contains`com`string`**

Quando usamos `Contains`em **strings** , ele verifica se **um trecho de texto** estáestá dentro da string.

### 🟢 **Exemplo**

`string frase = "Aprender C# é divertido!"; 
if (frase.Contains("C#")) 
{     
Console.WriteLine("A frase menciona C#!"); 
} 
else 
{     
Console.WriteLine("A frase não menciona C#.");
}`

### 🔹 **Saída**

`A frase menciona C#!`

💡 **Explicação**

- Uma string `frase`contém `"C#"`, então `Contains("C#")`retorna `true`.

---
#### ✅ **Usando `Contains`no seu código**

Não é seu código de **calculadora**de, usamos `Contains`para verificar **se o operador digitado é válido** .

### 🔹 **Trecho do seu código**

`string[] operadorPermitidos = { "+", "-", "*", "/" };  
if (operadorPermitidos.Contains(operador)) 
{     
Console.WriteLine("Operação válida!"); 
} 
else
{     
Console.WriteLine("Operação inválida!"); 
}`

💡 **Explicação**

- `operadorPermitidos`é uma matriz com os operadores aceitos.
    
- `Contains(operador)`verifique se o operador digitado pelo usuário está na lista.
    
- Se você estiver na lista ( `true`), o código segue normalmente. Se não ( `false`), exibe `"Operação inválida!"`.

---
### **Resumo**

→ Ver → Verifique se um texto contém outro texto .✅ **`Contains`em Listas** → Verifique se um elemento está presente.  
✅ **`Contains`em Strings** → Verifique se um texto contém outro texto.  
✅ **Usado sem código** → Para→ Para validar operadores da calculadora.