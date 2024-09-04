#GCP #Infrastructure 

### Total cost of ownership (TCO)

From a technology perspective, IaaS environments may be more cost-efficient from a hardware and infrastructure perspective but often, when you take into consideration the TCO across licensing and headcount, among other factors, it has the highest total cost. An organization that migrates from on-premises environments to an IaaS provider may not adopt architecture best practices for cloud environments and therefore bring much of the cost burdens of the on-premises assets with them to the cloud. This often includes existing contracts and licensing with software manufacturers for operating systems, databases, and more. This approach still has several benefits as it shifts the large capital expenditures of managing a data center to operating expenditures, offloads security and compliance responsibilities to the cloud provider, and empowers teams to quickly provision infrastructure.

### Flexibility

IaaS is the most flexible model out of the three core cloud computing models. Infrastructure teams have complete control over the infrastructure above the virtualization layer. They can select machine types, even the types and amount of cores that may be assigned to a VM, giving them granular control over the servers that will be running their applications. This also means that they are less restricted by the platform relative to the other models. However, there are still some limitations – for example, other cloud providers may force you into certain pre-built machine types based on what they’ve procured and what capacity is available. Google offers pre-configured machine types but customers are also free to define their own, custom machine sizes to maximize cost-to-performance ratios.

### Shared responsibilities

Within the IaaS model, the cloud provider is specifically responsible for the hardware and virtualization layer of the infrastructure. They procure server and networking hardware, manage the land, cooling, and power associated with the hardware, and are also responsible for the physical security of the location. They make their infrastructure available through virtualization over the internet, allowing clients to spin up VMs on their infrastructure.

Meanwhile, the IaaS customer is responsible for everything above the virtualization layer. Let’s break this down very clearly:

- IaaS vendor responsibilities:
    - Hardware
    - Virtualization
- IaaS customer responsibilities:
    - Operating system
    - Runtime
    - Scaling
    - Application
    - Data and configuration

### Management level

IaaS environments are the most involved from a management perspective given that technology teams directly oversee and control significant portions of the technology stack. They are responsible for securing the data in that environment and also need to implement disaster recovery and fault tolerance into their systems. This often includes tasks such as managing database backups, running parallel **hot-hot** or **hot-cold** environments as a means of reducing the risk of critical failures, and minimizing the impact breaches or outages.

Hot-hot refers to having multiple, redundant data centers that can pick up the traffic for another should one of them fail. In a hot-cold environment, you have a primary data center that hosts production workloads while your backup cold data center is used mainly for storage and archival. Effectively, it’s not a replica of the hot data center nor intended to handle production traffic.

### Staffing and expertise

Organizations leveraging IaaS services require a specific set of skills not only across the cloud platform itself but also across all of the systems and applications being used to host the applications. This means that team members will need to have exposure and familiarity with managing VMs and operating systems. Although this is a common skill set, it doesn’t provide a lot of value to the organization other than maintaining operations. Teams will often hire database administrators and infrastructure or virtualization experts and spend a significant amount of time micromanaging and overseeing the infrastructure. They’ve essentially shifted the on-premises working model to a cloud environment and retained the need for many of the skills associated with those environments.

IaaS offerings can essentially be thought of as virtualization as a service, where the cloud provider is responsible for the virtualization layer itself and everything else underneath that layer of infrastructure while the client is responsible for everything above that layer. It includes spinning up VMs and sizing them, as well as installing operating systems and patching them. The shift to PaaS abstracts away some of that fine-grained control over infrastructure to simplify the usage of developer tools and applications.