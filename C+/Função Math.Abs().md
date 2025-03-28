#### **O que é `Math.Abs(a)`?**

`Math.Abs(a)` é **uma função** que vem da classe `Math` em C#. A função **`Abs`** significa **"valor absoluto"**. O valor absoluto de um número é o número sem o sinal negativo.

🔹 **Exemplo de valor absoluto:**

- `Math.Abs(10)` → **10** (porque já é positivo)
    
- `Math.Abs(-10)` → **10** (porque ele transforma o negativo em positivo)
    
- `Math.Abs(0)` → **0** (zero não muda)

#### **Onde estamos usando isso?**

Na função do **MDC (Máximo Divisor Comum)**, ao final do cálculo, pode ser que o valor de `a` seja **negativo** (isso depende de como os números são divididos). O **MDC** deve sempre ser **positivo**, então a gente usa `Math.Abs(a)` para garantir que o resultado não tenha sinal negativo.

#### **Por que o MDC deve ser positivo?**

Quando falamos de frações, o **MDC** é usado para simplificar as frações, e uma fração simplificada deve ter um numerador e denominador positivos, ou então o sinal deve ser colocado no **numerador**. A ideia é ter um valor padrão sem sinal negativo.

---
#### **Resumindo:**

`Math.Abs(a)` vai garantir que o número que você está calculando seja **sempre positivo**, mesmo que o valor de `a` seja negativo.