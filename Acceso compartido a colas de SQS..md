#Security #SQS 

Tomando en cuenta el siguiente escenario: 
Una cola de AWS Simple Queue Service (SQS) tiene que ser configurada en dos cuentas AWS para un uso compartido a la cola.
La cuenta A de AWS tiene la cola SQS creada y la cuenta B tiene que tener acceso a la cola de la cuenta A.

Las medidas a tomar en cuenta para cumplir con el requerimiento son las siguientes:
- El administrador de la cuenta A crea un rol de IAM y le agrega una política de permisos.
- El administrador de la cuenta A agrega una trust policy al rol que identifica a la cuenta B como el principal que puede asumir el rol.
- El administrador de la cuenta B delega el permiso para asumir el rol a cualquier usuario en la cuenta B.