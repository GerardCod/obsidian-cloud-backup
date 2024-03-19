#Troubleshooting_and_Optimization #Networking 

Una forma sencilla para visualizar los logs de una VPC y poder dar solución a algún problema de conexión o comunicación con un subred es través de VPC Flow Logs.

Es una característica de las VPC que permite capturar información acerca del tráfico de red entrante y generado por las interfaces de red en una VPC. La información sobre los logs del tráfico de red pueden ser publicados en Amazon CloudWatch Logs o en S3.

Si se crea un flow log para una subred o una VPC todas las interfaces de red en en esa subred o VPC son monitoreadas.

Para crear un flow log, se tiene que especificar:
- El recurso para el que se crea el Flow Log.
- El tipo de tráfico a capturar (aceptado, rechazado, o todo el tráfico).
- Los destinos a los que deseas publicar los logs.

## Ejemplo
Una compañía está usando una conexión de AWS VPN basada en `Border Gateway Protocol (BGP)` para enlazar su centro de datos on-premise con instancias de EC2 en una subred A pero es incapaz de acceder a una instancia EC2 que se encuentra en una subred B dentro de la misma VPC.

¿Cuáles logs pueden ser usados para verificar el trafico que alcanza a la subred B?

- BGP Logs.
- VPC Flow Logs.
- Subnet Logs.
- VPN Logs.

	En la pregunta anterior la respuesta correcta es VPC Flow Logs por la explicación sobre VPC Flow Logs que se encuentra más arriba.