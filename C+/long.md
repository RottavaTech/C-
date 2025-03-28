#### **🔹 O que é `long`em C#?**

em CO tipo `long`em C# é um tipo de dado numérico **inteiro** que pode armazenar valores **muito** **grandes** .que pode armazenar valores **muito grandes** .

#### 📌 **Características do `long`:**

✅ Armazena **números inteiros**✅ Ocupação **8**(sem casas decimais).  
✅ Ocupa **8 bytes** ( 64 bits ) de memória . ✅ Apoie valores de(64 bits) de memória.  
✅ Suporta valores de **-9.223.372.036.854.775.808** até **9.223.372.036.854.775.807** .

#### **📌 Diferença entre `int`e`long`**

|Tipo|Tamanho|Intervalo de valores|
|---|---|---|
|`int`|4 bytes (32 bits)|-2.147.483.648 até 2.147|
|`long`|8 bytes (64 bits)|-9.223.372.036.854.775.808 até 9.223.372.036|

📌 **Use `long`quando precisar armazenar números muito grandes.**  
📌 **Use `int`quando os valores forem menores e você quiser economizar memória.**

### **Exemplo de `long`em C#:**

`long populacaoMundial = 8000000000; // 8 bilhões Console.WriteLine($"A população mundial é: {populacaoMundial}");`

✅ Isso funciona porque `8000000000`cabe no intervalo de `long`.  
❌ Se fosse `int`, **daria erro** , pois `8000000000`é maior que `int`suporte.