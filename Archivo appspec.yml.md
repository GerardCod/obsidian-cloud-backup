#CodeDeploy #AppSpec
Usos del archivo appspec:
- Mapea los archivos fuente de tu aplicación para los destinos en la instancia.
- Especifica permisos personalizados para los archivos desplegados.
- Especifica scripts para ejecutar en cada instancia en varias fases del proceso de implementación.

Durante la implementación, el agente de CodeDeploy busca el nombre del evento actual en la sección de hooks en el archivo AppSpec. Si el evento no es encontrado, el agente de CodeDeploy se mueve al siguiente paso. Si el evento es encontrado el agente CodeDeploy regresa la lista de scripts a ejecutar.

Los scripts se ejecutan secuencialmente en el orden en que aparecen en el archivo, el estatus de cada script es mostrado en el archivo log del agente CodeDeploy en la instancia.

Dicho archivo se puede usar para 