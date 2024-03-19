#Troubleshooting_and_Optimization #EC2 #Internet_Gateway 

Cuando existan problemas de comunicación entre un grupo de instancias EC2 con un Internet Gateway para establecer conexión con Internet es necesario revisar los siguientes puntos.

- Las ACL's de red asociadas con la subred debe tener reglas de entrada y salida del tráfico.
- La tabla de enrutamiento en la subred de la instancia EC2 debería tener una ruta hacia el servicio Internet Gateway.

