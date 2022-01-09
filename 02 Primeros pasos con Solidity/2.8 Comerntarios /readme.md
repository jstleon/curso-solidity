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

Más adelante veremos otra maneras de comentar nuestros contratos.

Estandar de comentarios en Solidity
Solidity utiliza el formato [NatSpec](https://docs.soliditylang.org/en/develop/natspec-format.html)

````Solidity
/// @title <Título de contrato>
/// @autor <Autor del contrato>
/// @notice <Explicar lo que hace el contrato o función>
/// @dev <Detalles adicionales sobre el contrato o función>
/// @param <nombre_parametro> <Describir para qué sirve el valor de retorno de una función>
/// @return <valor_retorno> <Describir para qué sirve el valor de retorno de una función> 

````