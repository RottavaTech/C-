# Desenvolvimento de Calculadora RPN de Frações em Console
## Parte 1: Leitura de Operações
[[Laços de Repetição]]
[[Condições e Instruções If]]
[[Método ToLower & ToUpper]]
[[Método IsNullOr WhiteSpace & Empty]]
[[Método Split]]
[[Método TryParse]]

`//----------------------------------------------------------------------------------
`using System;`
`using System.Linq;`

`class Calculadora`
`{`

    `static void Main()`
    `{`
        `Console.WriteLine("Calculadora RPN de Frações em Console");`
        `Console.WriteLine("Parte 1 Leitura de Operações\n");`
            
        `string inicio;`
        `string[] partes;`
        `decimal numero1;`
        `decimal numero2;`
        `string[] operadorPermitidos = { "+", "-", "/", "*" };`
        `string operador = "";`



        `while (true)`
        `{`
            `Console.WriteLine("Coloque dois numeros decimais e uma operação\n");`

            `inicio = Console.ReadLine();`

            `if (!string.IsNullOrEmpty(inicio.Trim()))`
            `{`
                `partes = inicio.Split(' ');`
                `if (partes.Length == 3)`
                `{`
                    `if (decimal.TryParse(partes[0], out decimal n1) && decimal.TryParse(partes[1], out decimal n2))`
                    `{`
                        `numero1 = n1;`
                        `numero2 = n2;`
                        `operador = partes[2];`
                        `if (operadorPermitidos.Contains(operador))`
                        `{`
                            
                            `break;`
                        `}`
                    `}`

                `}`

            `}`
            `Console.WriteLine("Operação Invalida! Tente Novamente");`
        `}`
        `decimal resultado = 0;`
        `switch (operador)`
        `{`
            `case "+":`
            `resultado = soma (numero2, numero1);`
            `break;`
            `case "-":`
            `resultado = sub(numero2, numero1);`
            `break;`
            `case "/":`
            `resultado = div(numero2, numero1);`
                `if (resultado == 0)`
                `{`
                    `Console.WriteLine("Erro informando que não pode se dividir por zero.");`
                `}`
            `break;`
            `case "*":`
            `resultado = mult(numero2, numero1);`
            `break;`
        `}`
        `Console.WriteLine(resultado);`
    `}`



    `static decimal soma (decimal nm1, decimal nm2)`
    `{`
        `return nm1 + nm2;`

    `}`
    `static decimal sub(decimal nm1, decimal nm2)`
    `{`
        `return nm1 - nm2;`

    `}`
    `static decimal div(decimal nm1, decimal nm2)`
    `{`
        `//if (nm1 == 0 || nm2 == 0)`
        `//{`
        `//    return 0;`
        `//}`
        `return nm1 / nm2;`

    `}`
    `static decimal mult(decimal nm1, decimal nm2)`
    `{`
        `return nm1 * nm2;`

    `}`

`}`

## Parte 2: Pilha
[[Pilhas]]
## Parte 3: Sistema que Empilha e Desempilha Valores e Operações
