#### **O que é `temp`?**

`temp` é uma variável temporária que guarda o valor antigo de `b`. Isso acontece porque logo depois alteramos `b` e não queremos perder o valor original dele.

🔹 **Sem `temp`, perderíamos o valor antigo de `b` e não conseguiríamos atualizar `a` corretamente.**

#### **O que é MDC (Máximo Divisor Comum)?**

O **Máximo Divisor Comum (MDC)** de dois números é o maior número que divide ambos **sem deixar resto**.

🔹 **Exemplo:**  
MDC de **18** e **24** → Os divisores são:

- 18 → 1, **2**, 3, **6**, 9, 18
    
- 24 → 1, **2**, 3, **6**, 8, 12, 24

✅ O maior número comum entre eles é **6**, então **MDC(18, 24) = 6**.

A função `CalcularMDC(long a, long b)` usa o **Algoritmo de Euclides** para calcular isso rapidamente.

---
#### **Como funciona o Algoritmo de Euclides?**

O **Algoritmo de Euclides** usa divisões sucessivas para encontrar o MDC.

💡 Regra principal:

`MDC(a, b) = MDC(b, a % b)`

Ou seja, substituímos `a` pelo `b` e `b` pelo **resto da divisão de `a / b`**, até que `b` seja **zero**.

🔹 **Passo a passo para MDC(18, 24):**  
1️⃣ `a = 18, b = 24`  
2️⃣ `temp = b` (temp = 24, guardamos o valor antigo de `b`)  
3️⃣ `b = a % b` → `b = 18 % 24` → `b = 18`  
4️⃣ `a = temp` → `a = 24`  
5️⃣ Repetimos até `b = 0`

Quando `b = 0`, o valor de `a` é o MDC.