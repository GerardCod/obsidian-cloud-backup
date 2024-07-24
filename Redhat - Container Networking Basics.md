#Redhat #Networking #Containers 

Podman comes with a network called `podman`. By default, containers are attached to this network and can use it to communicate with one another.

However, you might need to create a new Podman network to better suit the increased communication needs of most applications. For example, the containers running an application API and database can use a separate Podman network to isolate their communication from other containers. Similarly, that same API container can use yet another network to isolate communication with a third container that hosts the application UI.

|                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------- |
| ![](https://rol.redhat.com/rol/static/static_file_cache/do188-4.14/basics/networking/assets/images/basics/networking/isolated-networking.svg) |
|                                                                                                                                               |
In the preceding example diagram, the UI and API containers are attached to the `ui-network` Podman network. The API and database containers are attached to the `api-network` Podman network.