Um campo `const` só pode ser inicializado na declaração do campo.
Use a palavra-chave `const` para declarar um campo constante ou uma constante local. Campos e locais constantes não são variáveis e não podem ser modificados. As constantes podem ser números, valores boolianos, cadeias de caracteres ou uma referência nula. Não crie uma constante para representar informações que você espera alterar a qualquer momento. Por exemplo, não use um campo constante para armazenar o preço de um serviço, um número de versão do produto ou o nome da marca de uma empresa. Esses valores podem ser alterados ao longo do tempo e, como os compiladores propagam constantes, outros códigos compilados com suas bibliotecas precisarão ser recompilados para ver as alterações. Por exemplo:

```
const int X = 0;
public const double GravitationalConstant = 6.673e-11;
private const string ProductName = "Visual C#";
```

cadeias de caracteres interpoladas podem ser constantes, se todas as expressões usadas também forem cadeias de caracteres constantes. Esse recurso pode melhorar o código que cria cadeias de caracteres constantes:

```
const string Language = "C#";
const string Platform = ".NET";
const string FullProductName = $"{Platform} - Language: {Language}";
```

#### Observações

O tipo de uma declaração constante especifica o tipo dos membros que a declaração apresenta. O inicializador de uma constante local ou um campo constante deve ser uma expressão constante que pode ser convertida implicitamente no tipo de destino.

Uma expressão constante é uma expressão que pode ser totalmente avaliada em tempo de compilação. Portanto, os únicos valores possíveis para constantes de tipos de referência são cadeias de caracteres e uma referência nula.

A declaração constante pode declarar várias constantes, como:

```
public const double X = 1.0, Y = 2.0, Z = 3.0;
```

O modificador de `static` não é permitido em uma declaração constante.

Uma constante pode participar de uma expressão constante, da seguinte maneira:

```
public const int C1 = 5;
public const int C2 = C1 + 100;
```