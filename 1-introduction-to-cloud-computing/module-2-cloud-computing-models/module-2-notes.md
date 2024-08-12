### Service models
SaaS application
Software wihtout installing. User: anyone
In addition to the PaaS and IaaS, it manages applications and data

PaaS platform
Mix of both. User: developer
Cloud provider manages the platform infrastructure: OS, dev tools, db, business analytics.

IaaS infrastructure
Provides compute, networking and storage resources,  to consumers on-demand, over the internet on a pay-as-you-go basis. User: Sys admin
Cloud provider manages data centers, cooling, power, network and security, servers and storage

Infrastructure as a Service IaaS
VMs include an Hypervisor managing OSs inside wich is the data, apps and middleware.
Have:
Physical data centers: experienced but not in contact
Compute: memory, storage, VM
network: virtualizacion and APIs
Storage: object, file, block

Used to test and develop faster, abstracting low level components
Business continuity and disaster recovery less expensive
Faster deployment and scaling
High performance computing accessible
Big Data Analysis economically viable

Storage is used as backups and worloads too

Track and monitor usage and performance

Object storage is the most common mode of storage in the cloud, 

Platform as a service PaaS
Develop, deploy and run applications
Mainly includes servers, networkds, storage, os, app runtimes, APIs, Middleware, Databases

In addition to managing physical site, storage and networking and security, it manages hypervisors and OS, dev tools and runtimes, databases and analytics
High level of abstraction
Simplify dev job
executes code accordint to policies
deploy, run and scale apps, efficiently
support a range of application infrastruture capabilities (middleware)

Used for: API, IoT, Business analytics/intelligence, Business Process Management (BPM), Master Data Management (MDM)

Provide scalability, faster time to market, greater agility and innovation without investing in resources needed

Key offerings
AWS Elastic Beanstalk
CloudFoundry
IBM cloud Paks
Azure
Openshift
Magento
force.com
apache Stratos

Risks
IS threaths
dependency on service providers infrastructure
lack of control over changes in strategy, service offerings or tools

Software as a Service SaaS
provides access to a service cloud software

Email and collaboration
Customer Relationship Management
Human Resource Management
Financial Management
Billing and Collaboration

Key characteristics
Multitenant Architecture
Manage Privileges and Monitor Data
Security, Compliance, Maintenance
Customize Applications
Subscription model
Scalable resources

Lesson 1 Summary 

In this lesson, you have learned the following:

    With IaaS, the cloud provider manages physical resources. 

    With PaaS, the provider manages the platform infrastructure. 

    In the SaaS model, the provider hosts and manages the applications and data.

    Infrastructure-as-a-Service is a form of cloud computing that delivers fundamental computer, network, and storage resources to consumers on-demand, over the network, on a pay-as-you-go basis. 

    The key components of cloud infrastructure are:

        Physical data centers

        Compute

        Network

        Storage

    Platform-as-a-Service is a cloud computing model that provides customers with a complete platform—hardware, software, and infrastructure. 

    The high level of abstraction, support services, runtime environments, rapid deployment mechanisms, and middleware capabilities distinguishes PaaS clouds.

     PaaS advantages are:

        Scalability

        Faster time to market products and services.

        Greater agility and innovation

    Software-as-a-Service is a cloud offering that provides users with access to a service provider’s cloud-based software. 

    SaaS characteristics are:

        Multitenant architecture 

        Security, compliance, and maintenance

        Customization of applications

        Subscription model

        Scaling

    SaaS advantages are:

        Direct procurement of solutions

        Improved workforce productivity and efficiency

        Enable distribution of software costs

Cloud models

Public Cloud Deployment model
Resources distributed on an as-needed service

On-demand resources
significant economies of scale
Highly available

Concerns
Security
Data sovereignty compliance

Use cases
1.teams can focus on building and testing apps, reducing time-to-market 
2. businesses wit fluctuating capacity and resourcing needs
3. build secondary infrastructures for disaster recovery, data protection and business continuity
4. greater accesibility, easy distribution and backing up
5. IT departments outsourcing management of less critical and standardized business platforms

Private cloud model
Exclusive use, exist on premises
internal or external
VPC Virtual Private Cloud

It adds control.
internal control by IT
Reduced costs
better scalability
controlled access and security
greater agility

Common uses
1. Modernize and unify in-house and legacy apps
2. Build applications anywhere & move them without compromising
3. Full control of security and compliance issues.


Hybrid cloud
Flexibility
Workloads move freely
Leverage public and private clouds with cloud bursting

Interoperable, scalable, portable


By how many and how it is deployed:

Hybrid monocloud

Hybrid multicloud

Composite multicloud

 It allows security and compliance
 scalability and resilience
 resource optimization
 cost-saving

 Uses:
 SaaS integration
 Data and AI integration
 Enhancing legacy apps
 VMware migration


“Cloud infrastructure [that] is provisioned for exclusive use by a specific community of consumers from organizations that have shared concerns (e.g., mission, security requirements, policy, and compliance considerations). It may be owned, managed, and operated by one or more of the organizations in the community, a third party, or some combination of them, and it may exist on or off premises.”
Why community cloud?

Community cloud approach is used by organizations for the following reasons:

    The community cloud members work under the same set of security controls.

    The approach provides the members the same attributes like citizenship and authorization controls while giving limited physical and/or logical access to resources.

    It also supports data localization and some data sovereignty requirements based on the location of the community cloud’s data centers. 

    The approach defines a perimeter security model encompassing the community cloud. 

Implementation of software-defined community cloud 

To establish a security perimeter, most legacy community clouds depend on physical separation from other clouds. However, this implementation could not meet the advanced security, manageability, or compliance requirements of the industry.

In the modern architecture, a software-defined community cloud is designed to deliver the required benefits. Google Cloud is a software-defined approach that provides security and compliance assurances without the strict physical infrastructure constraints of legacy approaches. The Google community clouds use a combination of technologies referred to as “assured clouds” that can:

    Define communities around common projects, security and compliance requirements, and policy.

    Separate shared community projects from other projects.

    Modify capabilities of a community’s boundary based on policy-controlled and audited configuration changes.

    Lesson 2 Summary: Deployment Models

In this lesson, you have learned:

    Deployment models indicate where the infrastructure resides, who owns and manages it, and how cloud resources and services are made available to users. There are four main deployment models available on the cloud—public, private, hybrid, and community.

    In the public cloud model, the service provider owns, manages, provisions, and maintains the physical infrastructure such as data centers, servers, networking equipment, and storage, with users accessing virtualized computing, networking and storage resources as services.

    In the private cloud model, the provider provisions the cloud infrastructure for exclusive use by a single organization. The private cloud infrastructure can be internal to the organization and run or on-premises. Or it can be on a public cloud, as in the case of Virtual Private Clouds (VPC), and be owned, managed, and operated by the cloud provider.

    In the hybrid cloud model, an organization’s on-premise private cloud and a third-party, public cloud are connected as a single, flexible infrastructure that leverages the features and benefits of both Public and Private clouds.

    In the community cloud model, the provider provisions the cloud infrastructure for use by a community of organizations with shared concerns. One or more of the organizations in the community, a third-party provider, or both are responsible for the ownership, management, and operation of this infrastructure.