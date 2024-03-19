#Development #SQS 

## Casos de uso
Algunos escenarios donde es conveniente usar una Dead Letter Queue son los siguientes:
- **Un evento falla en todos sus intentos de procesamiento**: Una Dead Letter Queue actúa como un destino en caso de fallas que es usada cuando un evento fracasa en todos los intentos de procesamiento o expira sin ser procesado.
- **La invocación de una función Lambda es asíncrona**: Cuando un evento de invocación asíncrona excede su tiempo de vida máximo o falla todos los reintentos, Lambda lo descarta o lo envía a una DLQ (`Dead Letter Queue`) en caso de que la tengas configurada.
