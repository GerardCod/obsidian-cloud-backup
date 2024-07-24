#Redhat #Networking #Containers 

When you use the default Podman network, the domain name system (DNS) for other containers in that network is disabled. To enable DNS resolution between containers, create a Podman network and connect your containers to that network.

When using a network with DNS enabled, a container's hostname or alias is the name assigned to the container. For example, if a container is started with the following command, then the other containers on the `test-net` network can make requests to the first container by using the `basic-container` hostname. The `basic-container` hostname resolves to the current IP address of the `basic-container` container.

```bash
[user@host ~]$ podman run --net test-net --name basic-container example-image
```

### Connecting Containers

You can connect containers to one or more Podman networks. After a container connects to a network, the container can communicate with other containers on that network. However, even though the containers are reachable to one another, other components might prevent connections. For example, firewall rules might block a connection coming from another container. By default, a container is available within any network that the container connects to.

For example, consider a running container called `nginx-host` that uses the `example-net` network. The container exposes an HTTP server on port 8080. Within another container that uses the `example-net` network, the following `curl` command resolves to the root of the HTTP server.

```bash
[user@host ~]$ curl http://nginx-host:8080
```
