Um método static em C# é um método que pertence a um tipo, e não a um objeto específico. Para acessá-lo, basta usar o nome do tipo, e não é necessário instanciar a classe. 

Vantagens

- Não é necessário instanciar a classe para usar o método 
- Pode ser útil para conter métodos que operam apenas em parâmetros de entrada 

Como usar

- O modificador static pode ser adicionado a métodos, propriedades, operadores, eventos, construtores, campos e classes 
- Para acessar os membros de uma classe estática, use o nome da classe 
- Por exemplo, se houver uma classe estática chamada UtilityClass com um método público chamado MethodA, para chamar o método use-se: UtilityClass.MethodA(); 

Construtores estáticos 

- Um construtor estático é chamado automaticamente antes da primeira instância ser criada ou de qualquer membro estático ser referenciado
- Uma classe ou struct só pode ter um construtor estático
- Não podem ser herdados ou sobrecarregados

Por Exemplo=

com o metodo estático:
Fracao.Simplificador()

sem o metodo:

Fracao objfracao = new Fracao()
objfracao.Simplificador()

