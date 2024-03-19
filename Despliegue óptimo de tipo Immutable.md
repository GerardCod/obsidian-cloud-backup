#ElasticBeanstalk #Deployment
Elastic Beanstalk es un servicio de AWS que permite implementar aplicaciones sin la necesidad de saber como configurar la infraestructura subyacente. Una de las ventajas es que te brinda la opción de implementar aplicación con diferentes políticas de implementación.

Por ejemplo para el siguiente caso: El equipo de desarrollo en una compañía de comercio electrónico completó la ultima implementación de su aplicación con una capacidad reducida por su política de implementación. La aplicación llega a un pico de rendimiento por un pico de trafico debido a una venta entrante.

> Para este caso en específico la mejor opción de implementación es una política Inmutable porque crea nuevas instancias con la versión de la aplicación más reciente en lugar de actualizar la aplicación en las instancias EC2 existentes. Además de contar con un rollback seguro en caso de que falle el despliegue de la aplicación.

`Nota: Cuando ocurre una **Immutable update** un nuevo ELB es creado y procesa el tráfico de peticiones junto con la versión anterior de la aplicación hasta que todos los healthchecks de la nueva aplicación pasen, en caso contrario las instancias EC2 son terminadas para evitar algún impacto.`