#CloudFormation #ResourceAutomation  
Cuando se intenta automatizar el proceso de creación de recursos en diferentes regiones de AWS sin necesidad de escribir código lo más recomendable es configurar una plantilla de CloudFormation para definir los recursos y usar el comando **create-stack-set** de la `CLI de AWS` para crear un stack set en las regiones deseadas.. 

Por ejemplo un caso de uso es que una empresa de e-commerce requiere realizar un proceso de geographic load testing de su API de procesamiento de ordenes y se necesita la implementación de recursos cloud en las múltiples regiones de AWS para soportar la prueba de carga.

