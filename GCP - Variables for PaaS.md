#GCP #Platform 

### TCO

PaaS customers might feel like their cloud bills are more expensive than if they were running their infrastructure but this is typically not the case when you look at it from a TCO perspective. Although they might spend more on technology, they no longer have to spend a significant amount of money and headcount on managing the infrastructure itself. Teams leveraging PaaS solutions no longer need to pay for the cost and management of the underlying infrastructure, allowing them to avoid large, multi-year licensing contracts for operating systems, for example as PaaS platforms have abstracted it away. PaaS solutions have a lower TCO than IaaS solutions but higher than SaaS solutions.

### Flexibility

Teams building on top of PaaS technologies will find themselves more restricted than when using IaaS cloud solutions. Because they don’t manage the underlying infrastructure of the platforms, they won’t be able to freely choose and adapt those components. Platforms will be restricted to what the cloud provider can support through their technology. Examples of this are that specific PaaS hosting platforms may only support specific runtime environments, programming languages, or versions of programming languages. Support of new releases for a specific programming language, for example, may take some time to translate to a production-grade release by the PaaS provider.

### Shared responsibilities

When offering PaaS solutions to clients, the cloud provider is responsible for the hardware, virtualization layer, operating systems, and runtime environment. Everything above those layers is the responsibility of the PaaS client. This includes scaling the platform, the application code running in the environment, the data, and the associated configuration. Let’s break this down, similar to the previous subsection:

- PaaS vendor responsibilities:
    - Hardware
    - Virtualization
    - Operating system
    - Runtime
- PaaS customer responsibilities:
    - Scaling
    - Application
    - Data and configuration

### Management level

PaaS environments require significantly less time and resources to manage relative to IaaS environments. Much of the technical complexity of configuring and managing infrastructure is abstracted away so that data and development teams can focus on deriving value from the platform rather than keeping the platform running, secure, and reliable. There are still components that need to be managed, such as scaling, but this is often relatively easy to do through the platform, and new capabilities are typically offered, such as canary deployments and traffic splitting with App Engine ([https://cloud.google.com/appengine/docs/legacy/standard/python/splitting-traffic](https://cloud.google.com/appengine/docs/legacy/standard/python/splitting-traffic)). **Traffic splitting** is where you deploy a new version of the application and only funnel a percentage of the traffic to the new version to validate that there are no issues that may cause an outage. Building out this sort of production testing infrastructure and managing the traffic from an IaaS perspective would take much more time and effort, while with PaaS solutions, it can be achieved with a few clicks of a button.

### Staffing and expertise

Teams that choose to leverage PaaS solutions are empowered to specialize their teams around things such as development, data science, and ML. Rather than having folks split expertise across infrastructure and development or data engineering and data science, they abstract away management of the infrastructure and focus them on revenue-generating activities. These teams focus on developing skills that are focused more on enabling the business to move faster and maximizing productivity, which is a very different mentality relative to the traditional, IaaS approach to infrastructure.

Now that we have a better understanding of the PaaS model, let’s shift even more to the right in the shared responsibility model as we abstract away infrastructure management to focus more on the application itself. SaaS solutions are typically geared toward end users, with administrators living within the application itself and managing the data in the application exclusively, as well as those who have access to the data and permission to execute specific workflows within the application.