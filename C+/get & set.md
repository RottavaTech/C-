#### **O que são `get`e `set`em C#?**

Em C#, `get`e `set`são usados ​​em **propriedades** dentro de uma classe.  
Eles são úteis para **obter ( `get`)** ou **definir ( `set`)** o valor de um campo (variável de classe).

Isso permite **encapsulamento** , ou seja, controlar como os dados são acessados ​​e modificados.

---
#### **Exemplo básico de `get`e`set`**

`class Pessoa`
`{`
    `private string nome; // Campo privado (não pode ser acessado diretamente)`

    `public string Nome  // Propriedade pública com get e set`
    `{`
        `get { return nome; } // Retorna o valor do campo "nome"`
        `set { nome = value; } // Define o valor do campo "nome" com o valor passado`
    `}`
`}`

Como usar essa classe no`Main()`

`Pessoa pessoa = new Pessoa();`
`pessoa.Nome = "Carlos";  // Usando o set para definir um valor`
`Console.WriteLine(pessoa.Nome);  // Usando o get para obter o valor`

📌 **Explicação:**

- `set`recebe um valor e armazena na variável `nome`. O `value`representa o valor que estamos passando.
    
- `get`retorna o valor da variável `nome`.

---
#### **Exemplo com validação no`set`**

Podemos colocar regras dentro do `set`para evitar valores errados:
`class Produto`
`{`
    `private decimal preco;`
    `public decimal Preco`
    `{`
        `get { return preco; }` 
        `set` 
        `{` 
            `if (value < 0) // Impede preços negativos`
            `{`
                `Console.WriteLine("O preço não pode ser negativo!");`
            `}`
            `else`
            `{`
                `preco = value;`
            `}`
        `}`
    `}`
`}`

Usando essa aula não`Main()`
`Produto produto = new Produto();`
`produto.Preco = -50;  // Mensagem de erro: "O preço não pode ser negativo!"`
`produto.Preco = 100;`  
`Console.WriteLine(produto.Preco);  // Retorna 100`

📌 **Aqui o `set`impede valores inválidos** , garantindo que o `preco`nunca será negativo.

#### **Versão simplificada usando propriedades automáticas**

Se não precisar de lógica dentro do `get`e `set`, podemos simplificar assim:
`class Carro`
`{`
    `public string Modelo { get; set; }  // Propriedade automática`
`}`

#### **Usando não`Main()`**

`Carro carro = new Carro();`
`carro.Modelo = "Fusca";  // Define diretamente`
`Console.WriteLine(carro.Modelo);  // Retorna "Fusca"`

📌 **Aqui o C# cria automaticamente o campo privado** e gerenciado `get`e `set`sem precisar escrever tudo manualmente.

#### **Resumo Rápido**

✅ **`get`**→ Serve para **retornar** um valor.  
✅ **`set`**→ Serve para **beber** um valor.  
✅ **Encapsulamento** → Protege os dados e controla como são alterados.  
✅ **Propriedades automáticas** → Quando não precisamos de regras, podemos simplificar usando `{ get; set; }`.