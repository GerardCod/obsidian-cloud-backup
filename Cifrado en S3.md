#Security #S3 #KMS 

Dentro de S3 se tienen las siguientes opciones para cifrar la información en reposo.

- Cifrado del lado del servidor - Solicita a Amazon S3 cifrar tu objeto antes de guardarlo en los discos de sus centros de datos y luego descifrarlos cuando descargas los objetos.
- Cifrado del lado del cliente - Cifra la información del lado del cliente y sube los datos cifrado a Amazon S3. En este caso, tu gestionas el proceso de cifrado, las claves de cifrado y otras herramientas relacionadas.

Cuando se usa el cifrado del lado del servidor con AWS KMS (SSE-KMS), puedes usar las CMK por defecto gestionada por AWS, o puedes especificar una CMK gestionada por el usuario que ya hayas creado.

Crear tu propia CMK gestionada por el cliente te da mayor flexibilidad y control sobre la CMK. Por ejemplo puedes crear, rotar, o deshabilitar CMKs. También puedes definir controles de acceso y auditar las CMKs gestionadas por el usuario que se usan para proteger la información.