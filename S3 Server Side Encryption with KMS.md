#Development #S3 #KMS

Para proteger los datos en reposo en S3 tenemos tres opciones para el cifrado del lado del servidor:
1. SSE-S3 -> Son claves gestionadas por el mismo servicio de S3 por lo que no es necesaria alguna acción adicional.
2. SS3-KMS -> Son claves gestionadas por KMS por lo que requiere mayor acción del cliente para gestionar el ciclo de vida de las claves, rotación, etc.
3. SS3-C -> Son claves completamente gestionadas por el usuario porque lo que la responsabilidad de la gestión recae en el cliente.

Cuando se usa SS3-KMS AWS gestiona las claves pero tienes que gestionar la CMK (Customer Master Key) en AWS KMS. Puedes elegir entre una CMK personalizada o la que gestiona AWS para el servicio S3 en tu cuenta.

Si eliges usar una CMK personalizada los servicios de KMS y de S3 realizarán lo siguiente.

1. Amazon S3 solicita la clave en texto plano una copia de la clave encriptada bajo la CMK especificada.
2. AWS KMS genera una data key, la cifra con la CMK y envía tanto la data key en texto plano como la data key cifrada a Amazon S3.
3. Amazon S3 cifra la información usando la data key y elimina la clave en texto plano de la memoria tan pronto como sea posible luego de usarla.
4. Amazon S3 guarda la data key cifrada como metadata con la información cifrada.

Por lo que si eliges este tipo de cifrado es necesario que en las políticas de permisos de AWS se agregue la acción `kms:GenerateDataKey` para que al momento de enviar un archivo a S3, nuestro bucket pueda ejecutar las acciones necesarias para cifrar la información enviada.