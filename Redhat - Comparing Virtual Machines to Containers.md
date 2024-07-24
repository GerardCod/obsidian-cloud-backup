#Redhat #Development #Containers 

Containers generally serve a similar role to _virtual machines_ (VMs), where an application resides in a self-contained environment with virtualized networking for communication. Although this use case initially seems to be the same, containers have a smaller footprint, and start and stop faster than a virtual machine. For both memory and disk usage, VMs are often measured in gigabytes, whereas containers are measured in megabytes.

A VM is useful when an additional full computing environment is required, such as when an application requires specific, dedicated hardware. Additionally, a VM is preferable when an application requires a non-Linux operating system or a different kernel from the host.

## Virtual Machines vs Containers
Virtual machines and containers use different software for management and functionality. Hypervisors, such as KVM, Xen, VMware, and Hyper-V, are applications that provide the virtualization functionality for VMs. The container equivalent of a hypervisor is a container engine, such as Podman.

|                                 | Virtual machines               | Containers                                 |
| :------------------------------ | :----------------------------- | :----------------------------------------- |
| **Machine-level functionality** | Hypervisor                     | Container engine                           |
| **Management**                  | VM management interface        | Container engine or orchestration software |
| **Virtualization level**        | Fully virtualized environment  | Only relevant parts                        |
| **Size**                        | Measured in gigabytes          | Measured in megabytes                      |
| **Portability**                 | Generally only same hypervisor | Any OCI-compliant engine                   |

You can manage hypervisors with additional management software, which can be included with the hypervisor, or be external, such as Virtual Machine Manager with KVM. In contrast, you can manage containers directly through the container engine itself. Additionally, you can use container orchestration tools, such as Red Hat OpenShift Container Platform (RHOCP) and Kubernetes, to run and manage containers at scale. RHOCP manages both containers and virtual machines from a common interface.

With VMs, interoperability is uncommon. A VM that runs on one hypervisor is usually not guaranteed to run on a different hypervisor. In contrast, containers that follow the OCI specification do not require a particular container engine to function. Many container engines can function as drop-in replacements for each other.

## Deployment at Scale

Both containers and VMs can work well at various scales. Because a container requires considerably fewer resources than a VM, containers have performance and resource benefits at a larger scale. A common method in large-scale environments is to use containers that run inside VMs. This configuration takes advantage of the strong points in each technology.