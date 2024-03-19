#Development #DynamoDB 

Con transacciones de Amazon DynamoDB transactions,  puedes agrupar múltiples operaciones y enviarlas como una operación de tipo todo o nada (`TransactWriteItems` o `TransactGetItems`).

`TransactWriteItems` is a synchronous and idempotent write operation that groups up to 25 write actions in a single all-or-nothing operation. These actions can target up to 25 distinct items in one or more DynamoDB tables within the same AWS account and in the same Region. The aggregate size of the items in the transaction cannot exceed 4 MB. The actions are completed atomically so that either all of them succeed or none of them succeeds.

You can optionally include a client token when you make a TransactWriteItems call to ensure that the request is idempotent. Making your transactions idempotent helps prevent application errors if the same operation is submitted multiple times due to a connection time-out or other connectivity issue.