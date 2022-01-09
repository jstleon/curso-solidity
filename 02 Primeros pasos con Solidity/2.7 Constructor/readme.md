# 2.6 Contructor

Se especifican las propiedades que definen el contrato.

Se puede definir un contrato sin constructor, cuando suceda esto, el compilador creará uno por defecto. En contratos simples, sencillos, no será necesario definir un contructor. 

Cuando tengamos proyectos más complejos, será conveniente crear uno.

````Solidity

constructor() public {

}

````

Es una función opcional, que inicializa las variables de estado del contrato. Las variables de estado son las variables que se guardan que se guardan en una parte del contrato, que se conoce como el storage del contrato, la memoria del contrato.

