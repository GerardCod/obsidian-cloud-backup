#Development #Kinesis 

## Contexto
Kinesis Firehose es un servicio autoadministrado para enviar un flujo de datos en tiempo real a destinos como Amazon S3, Amazon Redshift, Amazon Elasticsearch Service, y Splunk. Con este servicio solo se configuran los producers para enviar datos a Firehose y entregar la información en el destino especificado.

Los únicos sink types soportados por el servicio Kinesis Firehose son:
1. Amazon Elasticsearch Service con un respaldo opcional de la información hacia S3.
2. Amazon S3 como destino directo.
3. Amazon Redshift con Amazon S3.