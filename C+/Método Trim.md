O método `Trim` remove da cadeia de caracteres atual todos os caracteres de espaço em branco à esquerda e à direita. Cada operação de corte à esquerda e à direita é interrompida quando um caractere de espaço não branco é encontrado. Por exemplo, se a cadeia de caracteres atual for " abc xyz ", o método `Trim` retornará "abc xyz". Para remover caracteres de espaço em branco entre palavras em uma cadeia de caracteres, use [expressões regulares do .NET](https://learn.microsoft.com/pt-br/dotnet/standard/base-types/regular-expressions).

 Observação

Se o método `Trim` remover quaisquer caracteres da instância atual, esse método não modificará o valor da instância atual. Em vez disso, retorna uma nova cadeia de caracteres na qual todos os caracteres de espaço em branco à esquerda e à direita encontrados na instância atual são removidos.

Se a cadeia de caracteres atual for igual a [Empty](https://learn.microsoft.com/pt-br/dotnet/api/system.string.empty?view=net-8.0#system-string-empty) ou todos os caracteres na instância atual consistirem em caracteres de espaço em branco, o método retornará [Empty](https://learn.microsoft.com/pt-br/dotnet/api/system.string.empty?view=net-8.0#system-string-empty).

Caracteres de espaço em branco são definidos pelo padrão Unicode. O método `Trim` remove todos os caracteres à esquerda e à direita que produzem um valor retornado de `true` quando são passados para o método [[Método IsNullOr WhiteSpace & Empty]]] .