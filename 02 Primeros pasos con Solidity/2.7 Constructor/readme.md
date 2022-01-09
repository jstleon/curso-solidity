# 2.6 Contructor

Se especifican las propiedades que definen el contrato.

Se puede definir un contrato sin constructor, cuando suceda esto, el compilador creará uno por defecto. En contratos simples, sencillos, no será necesario definir un contructor. 

Cuando tengamos proyectos más complejos, será conveniente crear uno.

````Solidity

constructor() public {

}

````

Es una función opcional, que inicializa las variables de estado del contrato. Las variables de estado son las variables que se guardan que se guardan en una parte del contrato, que se conoce como el storage del contrato, la memoria del contrato.

Dentro se especifican detalles como la dirección de la persona que ha desplegado el contrato, y depende de qué funciones, podemos definir, por ejemplo, que solo las pueda ejecutar la persona que ha desplegado el contrato, etc.

````Solidity

pragma solidity >=0.4.0 < 0.7.0;

contract PrimerContrato {
    
    address owner;

    constructor() public {
        owner = msg.sender;
    }
}

````

*El contructor sólo se ejecuta una vez, cuando se inicializa el contrato*


````Solidity

pragma solidity >=0.4.0 < 0.7.0;
import "./ERC20.sol";

contract PrimerContrato {
    
    address owner;
    ERC20Basic token;

    constructor() public {
        owner = msg.sender;
        token = new ERC20Basic(1000);
    }
}

````

En el ejemplo de aquí arriba estamos importando otro archivo de solidity, ERC20.sol, que es el archivo que usamos para crear tokens.

````Solidity
import "./ERC20.sol";
````

Luego se crea una instancia a la que llamamos token

````Solidity
ERC20Basic token;
````

Por último creamos 1000 Tokens.

````Solidity
token = new ERC20Basic(1000);
````

