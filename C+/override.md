#### **🔹 O que é `override`em C#?**

Esta **`override`**é uma palavra-chave usada em C# para **sobrescrever** métodos de uma classe base.

📌 **Isso significa que podemos modificar o comportamento de um método herdado de uma classe pai.**

---
#### **📌 Exemplo Simples de`override`**

`class Animal` 
`{`     
`public virtual void FazerSom()`    
	`{` 
	`Console.WriteLine("O animal faz um som...");`    
	`}` 
`}`  

`class Cachorro : Animal`
`{`     
`public override void FazerSom() // Sobrescrevendo o método da classe base`    
`{`         
`Console.WriteLine("O cachorro late: Au au!");`     
`}` 
`}`  

`class Program`
`{`     
`static void Main()`     
`{         Animal meuAnimal = new Cachorro();`          
`meuAnimal.FazerSom(); // Chama a versão sobrescrita`    
`}` 
`}`

🔹 **Saída:**

`O cachorro late: Au au!`

📌 O método `FazerSom`da classe `Cachorro` **substituiu** o da classe `Animal`por causa do `override`.

---
#### **📌 `override`no Nosso Código de Frações**

No código da `Fracao`, usamos `override`para sobrescrever o método `ToString()`.

`public override string ToString() {     return $"{Numerador}/{Denominador}"; }`

✅ **Sem `override`:**  
O método `ToString()`vira da classe `Object`e retornaria algo genérico como `Fractions.Fracao`.

✅ **Com `override`:**  
O método `ToString()`foi sobrescrito para exibir uma fração corretamente, como `3/4`, `-5/2`, etc.

📢 **Conclusão:**

- `long`é um tipo de dado que armazena números inteiros muito grandes.
    
- `override`é usado para modificar um método herdado de outra classe.