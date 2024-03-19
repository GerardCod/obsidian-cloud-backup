#Deployment #Containers #Lambda 

Para que un contenedor de Docker pueda ser usado como una función lambda se debe tomar en cuenta los siguientes puntos:
- La imagen del contenedor debe implementar el Lambda Runtime API.
- El servicio AWS Lambda no da soporte a funciones que usen imágenes para contenedor multi-arquitectura: Esto es porque aunque Lambda provee de imágenes base multi-arquitectura la imagen que subas debe implementar únicamente una arquitectura.

## Otros tips
- Lambda solo soporta container images basadas en Linux.
- Se pueden probar los contenedores localmente usando el Lambda Runtime Interface Emulator.
- Puedes subir una container image con un tamaño máximo de 10GB.

