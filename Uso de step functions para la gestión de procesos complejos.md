#StepFunctions
A company wants to automate its order fulfillment and inventory tracking workflow. Starting from order creation to updating inventory to shipment, the entire process has to be tracked, managed and updated automatically.

Una compañía quiere automatizar su llenado de ordenes y flujo de seguimiento de inventario. Comenzando desde la creación de las órdenes hasta la actualización del inventario al envío, el proceso completo tiene que ser rastreado, gestionado y actualizado automáticamente.

Para este caso de uso es recomendable usar **Step functions** por las siguientes razones.
- Orquesta de manera sencilla una secuencia de funciones Lambda y de servicios AWS en aplicaciones críticas para el negocio.
- Por medio de una interfaz visual es posible crear y ejecutar una serie de flujos de trabajo dirigidos por eventos que mantienen el estado de la aplicación.
- La salida de una fase es la entrada de la siguiente. Cada fase o paso se ejecuta en orden de acuerdo a la lógica de negocio que se implemente.
- Cada paso puede ejecutar una función lambda o un contenedor con lógica para actualizar una base de datos DynamoDB o para enviar un mensaje por medio de SQS.
## Ventajas de Step Functions
- **Construye y actualiza aplicaciones rápidamente**: AWS Step Functions te permite construir flujos de trabajo visuales para la rápida transformación de requerimientos del negocio en requerimientos técnicos.
- **Mejora la resiliencia**: AWS Step Functions gestiona el estado, controla y realiza reinicios por ti para asegurar que las aplicaciones se ejecutan en el orden esperado.
- Escribe menos código: AWS Step Functions gestiona la lógica de tu aplicación por ti e implementa primitivas básicas como la bifurcación (condicionales), ejecución paralela, y tiempos límite.