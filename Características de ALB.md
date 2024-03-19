#Development #ALB

Algunas de las características del servicio Application Load Balancer son las siguientes:
- **Un ALB tiene tres posibles tipos de destino: Instancia, IP y Lambda** -> Cuando creas un grupo de destino, especificas el tipo de destino. Después de crear un grupo de destino. no puedes cambiar su tipo de destino. Los siguientes son los posibles tipos de destino:
	1. Instancia: Los destinos son especificados por ID de instancia.
	2. IP: Los destinos son direcciones IP.
	3. Lambda: El destino es una función Lambda.
- **No puedes especificar direcciones IP públicamente enrutadas a un ALB**: Cuando el tipo de destino es una IP, puedes especificar direcciones IP solamente desde bloques CIDR específicos.