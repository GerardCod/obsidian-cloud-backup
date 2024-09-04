#GCP #Infrastructure 

The Google Cloud IaaS service is referred to as **Compute Engine**. Compute Engine allows customers to spin up VMs and manage applications in the same way that they would through a virtualization service. 

Technology teams can select the machine’s size, either through one of the pre-selected configurations or even build their own, custom VM, and select which operating system to use. From there, they install applications on those systems, connect them to a network, and make them available for others to access, similar to other virtualization services. 

They are also responsible for network configuration, monitoring, and other components. Google Cloud also provides additional value with **Managed Instance Groups** (**MIGs**). 

MIGs allow you to make VM-based infrastructure more reliable and scalable through automation by offering services such as autoscaling, autohealing, distributed deployments, and automatic updates.

This can be very valuable for organizations that experience inconsistent traffic patterns for their applications. A gaming company, for example, can leverage MIGs to dynamically scale their infrastructure and ensure that they can handle large influxes of gamers without the backend infrastructure collapsing.

It also optimizes for cost given that instance groups can also scale down assuming traffic tapers off. (You can read more here: [https://cloud.google.com/compute/docs/instance-groups](https://cloud.google.com/compute/docs/instance-groups).)