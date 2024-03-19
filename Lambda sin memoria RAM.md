#Development #Lambda 

Tomando en cuenta el siguiente escenario:

Subiste un archivo .zip a AWS Lambda que contiene archivos de código escrito en Node JS. Cuando tu función es ejecutada recibes el siguiente mensaje , 'Error: Memory Size: 10,240 MB Max Memory Used'.

¿Cuál es la causa del problema?

**Tu función Lambda se quedó sin memoria RAM**
AWS Lambda te permite ejecutar código sin provisionar o gestionar servidores. Pagas solo por el tiempo de procesamiento que consumes.
![[Pasted image 20240310185909.png]]
La cantidad máxima de memoria disponible para una función Lambda en tiempo de ejecución es de 10 240 MB. Tu función Lambda fue implementada con 10 240 MB de RAM, pero parece que el código solicitó o usó más de esa cantidad, así que la función Lambda falló.
