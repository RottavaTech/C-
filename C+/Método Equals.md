#### **O que é o método `Equals` em C#?**

O método `Equals` é usado para **comparar dois objetos** e verificar se eles são **iguais**. Ele pode ser usado para comparar **valores primitivos** (como `int`, `double`, `string`) e também objetos de classes personalizadas.

#### **Exemplo 1: Comparando Tipos Primitivos**

Para tipos básicos como `int`, `string` ou `bool`, o `Equals` verifica se os valores são iguais:

`int num1 = 10;`
`int num2 = 10;`

`bool saoIguais = num1.Equals(num2); // Retorna true`
`Console.WriteLine(saoIguais); // Exibe: True`

Isso funciona porque `int` é um **tipo de valor** e, nesses casos, o `Equals` compara diretamente os valores.

#### **Exemplo 2: Comparando Strings**

O `Equals` também pode ser usado para comparar strings:

`string texto1 = "Hello";`
`string texto2 = "hello";`

`bool comparacao1 = texto1.Equals(texto2); // Retorna false, porque C# diferencia maiúsculas de minúsculas.`
`bool comparacao2 = texto1.Equals(texto2, StringComparison.OrdinalIgnoreCase); // Retorna true, ignora diferença de maiúsculas.`

`Console.WriteLine(comparacao1); // False`
`Console.WriteLine(comparacao2); // True`

#### **Exemplo 3: Comparando Objetos de uma Classe**

Quando você cria sua própria classe, o `Equals` normalmente verifica se os dois objetos são **a mesma instância na memória**, não se os valores dentro deles são iguais.

`class Pessoa`
`{`
    `public string Nome { get; set; }`

    `public Pessoa(string nome)`
    `{`
        `Nome = nome;`
    `}`
`}`

`Pessoa p1 = new Pessoa("Maria");`
`Pessoa p2 = new Pessoa("Maria");`

`Console.WriteLine(p1.Equals(p2)); // Retorna false, porque são objetos diferentes na memória.`

Isso acontece porque, por padrão, `Equals` compara **a referência do objeto na memória**, e não os valores internos.

#### **Exemplo 4: Sobrescrevendo (`override`) o `Equals`**

Se quisermos que dois objetos sejam considerados iguais quando tiverem o mesmo nome, podemos **sobrescrever** o método `Equals` dentro da classe:

`class Pessoa`
`{`
    `public string Nome { get; set; }`

    `public Pessoa(string nome)`
    `{`
        `Nome = nome;`
    `}`

    `public override bool Equals(object obj)`
    `{`
        `if (obj is Pessoa outraPessoa)`
        `{`
            `return this.Nome == outraPessoa.Nome; // Compara os valores do nome`
        `}`
        `return false;`
    `}`
`}`

`Pessoa p1 = new Pessoa("Carlos");`
`Pessoa p2 = new Pessoa("Carlos");`

`Console.WriteLine(p1.Equals(p2)); // Retorna true, porque agora comparamos os nomes.`

---
### **Resumindo**

- `Equals` é um método que compara se dois valores ou objetos são iguais.
    
- Para **tipos primitivos** (`int`, `double`, `string`), ele verifica diretamente se os valores são iguais.
    
- Para **objetos**, por padrão, ele compara a referência na memória, mas podemos sobrescrevê-lo (`override`) para comparar os valores internos.