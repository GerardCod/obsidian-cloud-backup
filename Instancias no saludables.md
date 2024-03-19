#ELB #Networking #EC2
Cuando se tiene un Elastic Load Balancer con un target group con todas las instancias EC2 asociadas con un estado no saludable pero al acceder a la IP de las instancias se puede ver nuestras aplicaciones es debido a las siguientes razones.

1. El grupo de seguridad de las instancias EC2 no permiten el tráfico entrante desde el grupo de seguridad del Elastic Load Balancer.
2. **La ruta para el health check no está configurada correctamente**: Se debe asegurar de que los puertos listener y health check puedan comunicarse con el load balancer. Cada vez que se realice una actualización a los listener del balanceador de carga o al puerto healthcheck de un grupo de destino usado por el load balancer se debe validar que los grupos asociados permiten el trafico en el nuevo puerto en ambas direcciones.
