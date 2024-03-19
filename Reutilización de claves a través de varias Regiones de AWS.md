#Security

Para poder usar un par de claves por ejemplo SSH entre varias instancias EC2 a lo largo de varias Regiones de AWS se tiene que seguir el siguiente procedimiento.

- Genera una clave pública SSH a partir de la clave SSH private, luego importa la clave en cada una de las regiones de AWS.