#Development #S3 

La replicación en S3 es una funcionalidad para asegurar la disponibilidad de los objetos en S3 entre varias regiones de AWS.

Algunas características de esta funcionalidad son:

- **Las acciones del ciclo de vida S3 no se replican**: Con replicación de S3 (CRR y SRR) puedes establecer reglas de replicación para crear copias de tus objetos en alguna otra clase de almacenamiento (`storage class`), en la misma o en una región distinta. Las acciones de ciclo de vida no son replicadas y si deseas tener la misma configuración del ciclo de vida de los objetos tanto en el bucket fuente como destino, habilita la misma configuración de ciclo de vida en ambos buckets.

- **Same-Region Replication y Cross-Region Replication pueden ser configuradas a nivel de bucket S3, a nivel de prefijo compartido, o a nivel de objeto usando etiquetas de S3**: Amazon S3 Replication es configurado a nivel de bucket S3, a nivel de prefijo compartido, o a nivel de objeto usando etiquetas de S3. Para añadir una configuración de replicación en tu bucket fuente debes especificar un bucket destino en la misma o en una región AWS distinta para la replicación.