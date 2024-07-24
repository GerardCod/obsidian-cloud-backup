#Redhat #Development #Containers 

Containers can be split into two similar but distinct ideas: _container images_ and _container instances_. A _container image_ contains effectively immutable data that defines an application and its libraries. You can use container images to create _container instances_, which are executable versions of the image that include references to networking, disks, and other runtime necessities.

You can use a single container image multiple times to create many distinct container instances. You can also run these instances across multiple hosts. The application within a container is independent of the host environment.

`OCI container images are defined by the `image-spec` specification, whereas OCI container instances are defined by the `runtime-spec` specification.`

`Another way to think about _container images_ versus _container instances_ is that an instance relates to an image as an object relates to a class in object-oriented programming.`

