#Development #DynamoDB 

Una unidad de capacidad de lectura representa una lectura fuertemente consistente por segundo de un elemento de hasta 4KB de tamaño. Si necesitas leer un elemento mayor a 4KB DynamoDB consumirá unidades de capacidad de lectura adicionales.

Por ejemplo si en un proyecto donde se está utilizando una base de datos NoSQL, uno de los requerimientos es que el software soporte 10 lecturas por segundo fuertemente consistentes de 6KB cada una.

Entonces en el escenario de arriba y tomando en cuenta el tamaño de lecturas de las unidades de capacidad de lectura, el cálculo sería el siguiente.

6KB / 4KB = 1.5 unidades de capacidad de lectura, redondeando son 2.

Por lo que tomando en cuenta 10 lecturas de 6KB cada una tenemos en total 60KB.

Pero respetando el cálculo por cada lectura cada objeto necesita 2 unidades de capacidad de lectura.

El resultado es 20 unidades de capacidad de lectura.