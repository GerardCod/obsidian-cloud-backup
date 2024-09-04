#GCP #Infrastructure

**IaaS** is a cloud computing service model that delivers on-demand infrastructure resources to organizations via the cloud, such as compute, storage, networking, and virtualization. Customers don’t have to manage, maintain, or update their own data center infrastructure, but they are responsible for the operating system, middleware, VMs, and any apps or data.

The development of IaaS and accessing infrastructure over the internet was also very significant for technology teams. Cloud providers began to offer virtualization as a service, where they would provide the physical infrastructure components of a data center over the internet as a service.

Their clients would still be able to interact with the environment and manage it from a server design and operation system level but all of the physical, real-world complexities were abstracted away. If you needed a new server of a specific size in a specific location, the configuration and deployment of that server were now a few clicks away.

Much of the pain and stress from managing your infrastructure comes from all the potential points of failure across the technology stack. Whenever an application goes offline at peak demand, there are many reasons as to why that might happen.

There may have been a networking failure, whether it was caused by a misconfiguration, a recent patch, or a cable issue. Perhaps the code base was the problem, or not enough hardware was provisioned to handle the load.

While these issues still exist when using cloud providers, the organization can trust that the cloud provider will have specific capabilities for managing the physical components of the infrastructure. 

One of the big benefits of leveraging public cloud is that outages are publicly reported, which creates a culture of accountability while also incentivizing global downtime minimization. While organizations shouldn’t rely exclusively on these providers and still build fault tolerance into their infrastructure, this significantly reduces the cost and complexity of managing technology infrastructure. 

Another benefit is that the regulatory frameworks specific to the physical components of the infrastructure apply to the cloud provider and therefore propagate to their customers. 

IaaS cloud customers are still responsible for configuring the infrastructure platform itself and therefore oversee the virtualized infrastructure across **identity and access management** (**IAM**), operating systems (selection, versioning, and management), the configurations and provisioning of **virtual machines** (**VMs**), their associated applications and the data in those applications.