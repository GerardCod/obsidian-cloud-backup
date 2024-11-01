#Redhat #Linux 

Red Hat Enterprise Linux (RHEL) is Red Hat's production-ready, commercially supported Linux distribution. In the computing industry, RHEL is acknowledged as the leading platform for open source computing. RHEL is extensively tested and has a worldwide ecosystem of support partners for hardware and software certifications, consulting services, training, and multi-year support and maintenance guarantees.

Red Hat builds RHEL major releases directly from the CentOS Stream continuous development project, which is sourced from Fedora. In contrast to the previous RHEL development model, the releases were constructed internally with less transparency, and the source was provided only for building as CentOS Linux after the RHEL release. Now the new CentOS Stream development model is open and available to all, for feedback and contribution, and the code is prepared to be the next major RHEL release.

RHEL uses a subscription-based support model, and does not charge license fees for open-source software. Red Hat support subscriptions provide product support, maintenance, updates, security patches, and access to the Customer Portal Knowledgebase, utilities, and downloadable releases of Red Hat products.

The following table lists some key differences between Fedora, CentOS Stream, and RHEL.

|                           | Fedora       | CentOS Stream | RHEL     |     |     |
| :------------------------ | :----------- | :------------ | :------- | --- | --- |
| Expected lifecycle        | 12-18 months | 5 years       | 10 years |     |     |
| Software vendor certified | No           | Usually not   | Yes      |     |     |
| Documentation provided by | Community    | Community     | Red Hat  |     |     |
| Expert support available  | No           | No            | Yes      |     |     |
| Product security team     | No           | No            | Yes      |     |     |
| Security certifications   | No           | No            | Yes      |     |     |
| No-cost options           | Yes          | Yes           | Yes      |     |     |
| Management tools          | No           | No            | Yes      |     |     |

#### RHEL for Edge

RHEL for Edge is an image-based variant of RHEL, with a different deployment mechanism. RHEL provides the ability to create purpose-built operating system images through a tool called Image Builder. With this mechanism, IT teams can build, deploy, and maintain these RHEL images in less time over the life of the system. Image-based deployments are optimized for various edge architectures, but are customizable for specific edge deployments.

The Edge features in RHEL include secure management and scaling capabilities, including zero-touch provisioning, system health visibility, and quick security remediations from within a single interface.

#### Red Hat CoreOS

RHEL CoreOS (RHCOS) is not a stand-alone operating system, but it is built from RHEL components, and is then released, upgraded, and managed as part of the Red Hat OpenShift Container Platform (RHOCP) for cloud-native applications. RHCOS is fundamentally an image-based RHEL container host, which uses the Container Runtime Interface (CRI-O)-compliant container engine that is integrated in RHOCP. To learn more about Red Hat CoreOS, begin by becoming familiar with OpenShift and containers.

#### Red Hat Universal Base Image

A Red Hat Universal Base Image (UBI) is essentially a freely redistributable derivative of RHEL. UBI is designed to be a foundation for cloud-native and web application use cases that are developed in containers. All UBI content is a subset of RHEL, with packages sourced from secure RHEL channels, and UBI is supported similar to RHEL when run on a Red Hat supported platforms such as OpenShift and RHEL hosts.

With UBI, developers can focus their efforts on their application in the container image. UBI is a set of base images, and a set of application images (such as python, ruby, node.js, httpd, or nginx). UBI also consists of a set of RPM repositories, from which you can update any UBI base image to include the package dependencies that your application requires.

#### Red Hat Enterprise Linux Continuous Development

In the Fedora upstream community, Fedora Rawhide is the continuous development environment for a regular cadence of public Fedora releases. The community tests and prepares new Linux kernel versions, device drivers, utilities, and applications for the next Fedora distribution. Major RHEL release development begins with selection of the latest Fedora release as the base for the current CentOS Stream continuous development distribution.

Before a package is formally introduced to CentOS Stream, it undergoes rigorous testing to meet the standards for packages to be included in RHEL. Updates that are posted to CentOS Stream are the same as to those updates that are posted to the unreleased minor version of RHEL in development.

|                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------- |
| ![](https://rol.redhat.com/rol/static/static_file_cache/rh124-9.3/getstarted/whatislinux/images/getstarted/redhat-fedora-centos-releases.svg) |

Figure 1.2: Red Hat Enterprise Linux continuous development

As shown in the figure, Fedora 34 is the original code base for RHEL 9 and for CentOS Stream 9. As packages are updated, they are then pushed into CentOS Stream and the nightly build of RHEL. The solid lines indicate distributions or builds that are available for public use.

Similar to the relationship between Fedora Rawhide and Fedora, CentOS Stream is the continuous development environment for preparing the next minor-version RHEL release. Red Hat performs extensive hardware, integration, dependency, and performance testing before releasing the next public RHEL distribution.