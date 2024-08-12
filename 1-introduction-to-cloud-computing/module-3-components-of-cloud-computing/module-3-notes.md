## Components of Cloud Computing

Lesson 1

Overview

Computing:
    Virtual servers
    Bare Metal Servers
    Serverless

Storage
    All kinds

Networking
    provides
        routers
        switches
    for
        provisioning
        configuration
        management
    need or offer
        IP addresses
        subnets
        security groups
        ACLs
        VLANs 
        VPCs
        VPNs
        firewalls
        load balancers
        gateways
        traffic analyzers
        CDNs

Virtualization and VM
    Feasible by Hypervisor:
        Pull resources from the physical to the virtual
            Type 1
                Directly on top or bare metal.
                    More used, more secure, less latency. HyperV or Oepnsource Kvm
            Type 2
               Also called hosted. Includes a layer of Host OS between host and HV. Oracle, VMWare, higher latency.
    VM
        Are
            Software based computer run among others in the same hardware.
            Extremely portable.
            Also called virtual servers, virtual instances, instances
        Types
            Shared or public cloud / Multitenant
                pre-defined sizes and configurations. Sometimes personalized
                charged by hours, monthly or even seconds
            Transient or Spot VMs
                can be retaken by the provider
                Used for testing and statless workloads and testing scalability with low cosr
            Reserver virtual server instances
                resources guaranteed for future by a lower price
            Dedicated Host
                Only your VM uses the underline hardware
                maximum control over workload
    Bare Metal Servers
        single-tenant dedicatet physical server
        cloud provider manages up to the OS
        The rest is configured by customer
        custom or preconfigured
        Can include GPUs
        can take longer to provision, from minutes to hours
        more expensive than VMs
        Only offered by some cloud providers
        demanding environments
        high-performance compute HPC
        highly secure, isolated
    ERP, CRM, AI, DeepLearning, Custom Virtualizacion, Business Analytics
    Best for I/O intensive workloads  
    Added management and operational overhead

Networking in cloud vs On Premise
    Logical instances vs physical devices
    networking functions as service instead of rack networking devices
    Cloud uses VPC than can be divided in subnets providing scalability and security
    Security Groups provide virtual secure instances VSI 
    Use of load balancers ensure application responsiveness

Containers
    Are
        Applicationc code packages with dependencies and libraries to execute on desktop, traditional IT and cloud
        unlike VM they don't need an OS in every instance because they leverage OS
    Example comparison
        Node.js app
            VM
                Hypervisor and host included consuming resources.
                VM with linux and libs setup way bigger than the node.js consuming resources
                more VMs needed to scaled
            Container
                requires a Manifest, then create image and finally container
                A host is needed along with a runtime engine
                The containers itself have libs and js app
                shared resources, 

Lesson 1 Summary: Cloud Infrastructure

In this lesson, you have learned:

    Cloud infrastructure consists of data centers, storage, networking components, and computing resources.

    Virtualization is the process of creating a software-based version of physical resources, made possible by hypervisors. 

    A few different types of Virtual Machines can be provisioned on the cloud. These include:

        Shared or Public Cloud VMs that are provider-managed, multi-tenant deployments that can be provisioned on-demand with predefined sizes

        Transient or Spot VMs that take advantage of unused capacity in a cloud data center

        Reserved VMs that allow you to reserve capacity and guarantee resources for future deployments 

        Dedicated hosts that offer single-tenant isolation

    Bare metal servers are single-tenant physical servers that are dedicated to a single customer. Bare metal servers fulfill the demanding needs of high-performance computing (HPC) and data-intense applications. They are ideal for applications that have a high degree of security or compliance requirements.

    Networking capabilities in the cloud are delivered as a service rather than in the form of rack-mounted devices. Cloud resources such as VMs (or VSIs), storage, network connectivity, and load balancers are deployed into subnets within Virtual Private Clouds (VPCs). Using private and public subnets allows users to deploy multi-tier enterprise applications securely. Load balancers distribute the traffic and allow applications to be responsive.

    Containers are executable units of software in which application code, its libraries, and its dependences are packaged in a common way, so that it can be run anywhere, from desktops, traditional IT, to the cloud. Containers are more lightweight and consume fewer resources than Virtual Machines, helping streamline the development and deployment of cloud native applications. 

Lesson 2 Basics of Cloud Storage
    cloud providers
        Host
        Secure
        Manage
        Mantain
    are
        Scalable
    types
        direct attached
            or local storage
            within smae server or rack
            fast
            use for OS
            ephemeral, not shared and non-resilient
        file storage
            NFS storage, network file system
            slower, low cost, mounted or used on multiple servers at once
        block storage
            faster, can be mounted as volumes but in one at a time, IOPS, I/O operations per second measure it, don't require persistence after the compute node is terminated, allow snapshots
        object storage
            not attached to a compute node, slowest but accessible trough an API,  "infinite" in size, least expensive, pay per use
    file storage
        generally
            file storage need to be attached to a NFS or Network Attached Storage, are less expensive, more resilient, less disk maanagement and maintenance, provision much larger amounts
        IOPS
            Can become a bottleneck
    Block storage
        basically
            breaks files into blocks
            stores them with unique address
            must be attached to compute node
            resilient to failure, more secure data and easily mounted
            perfect for workloads with low latency and high speed
            not for server shared storage
   
    Block and file storage is taken from appliances which are mantained by the service provider, borh are highly available and resilient, often include data encryption at rest and in transit.
    
            

### Object Storage

Not connected to a particular compute node, it uses a particular server instance and uses an api.

Less expensive than other cloud storage options. Cents per month. 

It's effectively infinite.

Used for storing large amounts of unstructured data (not hierachical folder or directory structure)

Objects are stored in buckets, including metadata to locate, access the object, also time stamps

sizing information is not needed, can hold up to petabytes, adding data slowly or quickly.

it's resilient, possibly in more than one data center

Used when data is static and where fast reading and write speeds are not necessary like:
text
audio
video
IoT data
VM
backups
Data archives

Tiers
Buckets have Tiers or Classes depending on how much they are accessed. 
Standard is frequently accessed and costly
Vault is accessed once of twice a month
Cold Vault accessed once or twice a year
Automatic archiving rules can be setup to move storage tier 

does not come with IOPS and are slower than block storage, in cold vaults it can take hours. I tcan have other costs related to the data

API
S3 API is a standard based on the S3 object storage offered by AWS. HTTP based RESTful API or RESTful web server. PUT, GET.

backup and recovery
replacement for offside backups
geographical redundancy

### CDN Content Delivery Network
Distributed Server Network that stores copies of website content based on the user geolocation. 


Course Summary 

Lesson 2 Summary: Cloud Storage and Content Delivery Networks

In this lesson, you have learned:

    Cloud storage is available in four main types–Direct Attached, File, Block, and Object Storage. These storage types differ in how they can be accessed, the capacity they offer, how much they cost, the types of data they are best suited to store, and their read-write speed.

    Direct Attached (or Local) Storage is storage that is presented directly to a cloud-based server and is effectively either within the host server chassis or within the same rack.

    File Storage is typically presented to compute nodes as a Network File System (NFS), which means that the storage is connected to compute nodes over a standard ethernet network.

    Block Storage is presented to compute nodes using high-speed fiber connections, typically provisioned in volumes, which are mounted onto a compute node.  

    Object Storage is accessed via an API and doesn’t need an underlying compute node. 

    Object Storage offers infinite capacity as you can keep adding files to it and just pay for what you use. Compared to the other storage types, object storage is slowest in terms of read and write speeds. 

    A Content Delivery Network (CDN) is a distributed server network that accelerates internet content delivery by delivering temporarily stored or cached copies of website or media content to users based on their geographic location. 

    