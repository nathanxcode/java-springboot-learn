# Inversão de Controle

## A inversão de controle é um princípio na engenharia de software que transfere o controle de um objeto para um container ou framework. O IoC pega o controle do fluxo do programa e faz chamadas para nosso próprio código costumizado. Para permitir isso, o framework usa abstrações com comportamentos adicionais incorporados.

# Injeção de Dependências

## DI é um padrão que podemos usar para implementar o IoC, onde o controle invertido está definindo a dependência do objeto. Conectar ou "injetar" objetos dentro de outros objetos, é feito por um assembler ao invés do próprio objeto.


### Como seria feito normalmente: 

```
public class Store {
    private Item item;

    public Store(){
        item = new ItemImpl1();
    }
}
```
### Aqui precisamos instanciar uma implementação da interface item.

### Agora com DI: 
```
public class Store{
    private Item item;
    public Store(Item item){
        this.item = item;
    }
}
```