#Deployment #CloudFormation 

Los parámetros o «Parameters» es una sección de las plantillas de `CloudFormation` que permiten una mayor personalización.
Con Parameters puedes ingresar valores personalizados a tu plantilla cada vez que creas o actualizar una stack.

![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt3-q57-i2.jpg)

`AllowedValues` es un arreglo que contiene una lista de valores permitidos para el parámetro.
Cuando se aplica a un valor de tipo String, el valor ingresado debe ser igual a alguno de los valores permitidos.
Cuando se aplica a un valor de tipo `CommaDemilitedList` cada uno de los valores de la lista debe ser uno de los valores permitidos.