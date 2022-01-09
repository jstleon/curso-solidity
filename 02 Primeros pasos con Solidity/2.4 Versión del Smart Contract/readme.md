# 2.4 Versión del Smart contract


Todo contrato debe empezar especificando la versión que debe usar el compilador

````Solidity
pragma solidity ^0.4.0;

````

Existen dos maneras de expecificar la versión. Cómo lo estás viendo aquí arriba, donde nuestro contrato sólo funcionará en la versión que se ha declarado.

Otra manera es una poner un rango de versiones.

````Solidity
pragma solidity >=0.4.0 <0.7.0;

````


