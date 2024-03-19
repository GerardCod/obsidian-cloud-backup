#Security #S3 #Cognito

Un caso de uso especial en el que se involucran los servicios de Amazon Cognito y S3 es que a través de ellos se restrinja a la carpeta de usuarios a acceder únicamente a una carpeta dentro de un bucket S3 que corresponda con el usuario.

Para lograr dicho objetivo se puede realizar lo siguiente.

	Usar una política de IAM para con el prefijo de identidad de       Amazon Cognito para restringir a los usuarios a usar su propio     folder en Amazon S3.

**¿Por qué funcionaría esto?**
Amazon Cognito identity pools te permite crear identidades únicas para tus usuarios y federarlos con proveedores de identidad. Con un `identity pool` puedes obtener credenciales de AWS temporales y con privilegios limitados para acceder a otros servicios de AWS.

Amazon Cognito identity pools soporta los siguientes proveedores de identidad:
- Proveedores públicos: Login con Amazon (identity pools), Login con Facebook (identity pools), Login con Google (identity pools), Sign in con Apple (identity pools).
- Amazon Cognito User pools.
- SAML Identity providers (identity pools).
- Identidades de desarrollador autenticado (identity pools).

Puedes crear una política basada en identidades que permita a los usuarios de Amazon Cognito acceder a objetos en un bucket S3 específico. Dicha política solo permite acceder a objetos con un nombre que incluya «Cognito», el nombre de la aplicación y el nombre del usuario federado, representado por la variable `${cognito-identity.amazonaws.com:sub}` 

![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt3-q26-i2.jpg)
