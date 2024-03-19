#Development #Kinesis 

Tomando en cuenta el siguiente escenario:

Tienes creado un recurso en Amazon Kinesis Data Stream con 10 shards, y desde las métricas, estás muy por debajo del uso de 10MB por segundo para enviar información. Mandas 3MB por segundo de información y sigues recibiendo frecuentemente errores del tipo ProvisionedThroughputExceededException.

¿Cuál podría ser la causa de esto?

**La clave de partición que elegiste no está suficientemente distribuida**

Amazon Kinesis Data Stream te permite construir aplicaciones personalizadas que procesan o analizan flujos de datos para necesidades especializadas.

Amazon Kinesis Data Stream es un conjunto de fragmentos (shards). Un fragmento es una secuencia únicamente identificada de registros de información en un flujo. Un flujo está compuesto de uno o más fragmentos, cada uno de los cuales provee una unidad fija de capacidad.

La clave de partición es utilizada por Amazon Kinesis Data Stream para distribuir información entre fragmentos. Kinesis Data Streams segrega los registros de información que pertenecen a un flujo en múltiples fragmentos, usando la clave de partición asociada con cada registro de datos para determinar el fragmento al que el registro de información pertenece.

![[Pasted image 20240310184328.png]]
Para el caso de uso dado, como la clave de partición no está suficientemente distribuida, toda la información está siendo enviada a unos cuantos fragmentos específicos y no aprovecha todo el cluster de fragmentos.

También puedes usar métricas para determinar cuáles son los fragmentos fríos y calientes, es decir, los fragmentos que están recibiendo más, o menos datos de lo esperado.
