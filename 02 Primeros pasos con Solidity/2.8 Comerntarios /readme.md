# 2.8 Comentarios

Es muy importante comentar nuestro código. No solo para nosotros, sino para cualquiera que entre a leer nuestro código. Debemos documentar nuestro código 

Cuando estamos en fase de desarrollo podemos utilizar:

Comentario de una línea
````Solidity
// Soy un comentario de una línea!
````
Comentario multiínea
````Solidity
/*
Soy un 
comentario
multilínea! 
*/
````

Aunque para desarrollar puedes utlizar los comentarios "clásicos" utilizados aquí arriba, debes saber que cuando publiques tu contrato desde adaptarte al estándar de Solidity.

El estandar de comentarios en Solidity utiliza el formato [NatSpec](https://docs.soliditylang.org/en/develop/natspec-format.html)

````Solidity
/// @title <Título de contrato>
/// @autor <Autor del contrato>
/// @notice <Explicar lo que hace el contrato o función>
/// @dev <Detalles adicionales sobre el contrato o función>
/// @param <nombre_parametro> <Describir para qué sirve el valor de retorno de una función>
/// @return <valor_retorno> <Describir para qué sirve el valor de retorno de una función> 

````

Ejemplo con comentarios "clásicos" para utilizar en fases de desarrollo
````Solidity
// Indicamos la versión
pragma solidity >=0.4.0 < 0.7.0;
import "./ERC20.sol";

// Nuestro primer contrato
contract PrimerContrato {
    
    // En esta variable se encuentra la dirección de la persona que despliega el contrato
    address owner;
    ERC20Basic token;

    /*
    Guardamos en la varieble owner la dirección de la persona que despliega el contrato
    inicializamos el número de tokens
    */
    constructor() public {
        owner = msg.sender;
        token = new ERC20Basic(1000);
    }
}

````