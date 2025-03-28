#### **Por que `CalcularMDC` é `private` e `Simplificar` é `public`?**

- **`private` (privado)** → Significa que só **essa classe** pode usar a função.
    
    - `CalcularMDC(long a, long b)` é **um detalhe interno** da classe Fracao, então não precisa ser acessado por quem usa a classe.
        
- **`public` (público)** → Pode ser chamado de **fora da classe**.
    
    - `Simplificar()` é **uma funcionalidade que o usuário da classe pode chamar**, então é `public`.
        

💡 **Resumindo:**

- `private` → Função **auxiliar**, usada apenas dentro da classe.
    
- `public` → Método **disponível para quem usa a classe**.