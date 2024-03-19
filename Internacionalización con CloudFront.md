#Development #CloudFront

Tomando en cuenta el siguiente escenario:

Una compañía alojó su sitio web de reseñas de restaurantes en una instancia EC2. El sitio web soporta varios lenguajes y el lenguaje preferido es agregado como un parámetro query string a la petición.

La estructura de directorios y nombres de archivos es la misma para todas las versiones del sitio web. El sitio web responde con la versión de lenguaje preferida cuando es accedido directamente.

Sin embargo, cuando el sitio es accedido a través de la distribución CloudFront configurada, establece por defecto un solo lenguaje.

¿Cómo se puede arreglar este escenario?

**Crea una nueva política de cache para la distribución CloudFront y establece el comportamiento de cache a `Query string forwarding and caching`. En la whitelist del campo Query string incluye la cadena «Language». Actualiza la distribución CloudFront para usar la nueva política de cache.**

CloudFront puede guardar en cache diferentes versiones de tu sitio dependiendo de los valores de los parámetros query string.

Forward all, cache based on whitelist option should be chosen if your origin server returns different versions of your objects based on one or more query string parameters. Then specify the parameters that you want CloudFront to use as a basis for caching in the Query string whitelist field.

![[Internacionalización con CloudFront 2024-03-11 14.02.52.excalidraw]]