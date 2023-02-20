##### Data Services
- Azure Blobs: A massively scalable object store for text and binary data. Also includes support for big data analytics through Data Lake Storage Gen2.
    - Allows unstructured data to be stored and accessed at a massive scale in block blobs.
    - Also supports Azure Data Lake Gen2 for enterprise big data analytics solutions.
    - You want your application to support streaming abd random access scenarios.
    - You want to be able to access application data from anywhere.
    - You want to build an enterprise data lake on azure and perform big data analytics.
- Azure Files: Managed file shares for cloud or on-premises deployments.
    - Offers fully managed cloud file shares that you can access from anywhere via the industry standard Server Message Block (SMB), Network File System (NFS) and Azure Files REST API.
    - You can mount Azure files shares from cloud or on-premises deployments of Windows, Linux and macOS.
    - You want to "lift and shift" an application to the cloud that already uses the native file system APIs tho share data between it and other applications running in Azure.
    - You wantto replace or supplement on-premises file servers or NAS device.
    - You want to store development and debbuging tools that needto be accessed from many virtual machines.
- Azure Queues: A messaging store for reliable messaging between application components.
    - Allows for asynchronous message queueing between application components.
    - You want to decouple application components and use asynchronous messaging to communicate between them.
- Azure Tables: A NoSQL store for schemaless storage of structured data.
    - Allows you to store structured NoSQL data in the cloud, providing a key/attribute store with a schemaless design.
    - You want to store flexible datasets like user data for web application, address books, device information, or other types of metadata your service requires.
- Azure Disks: Block-level storage volumes for Azure VMs.
    - Allows data to be persistently stored and accessed from an attached virtual hard disk.
    - You want to "lift and shift" applications that use native file system APIs to read and write data to persistent disks.
    - You want to store data that is not required to be accessed from outside the virtual machine to which the disk is attached.

##### Blob Storage Resources
- Blob Storage offers three types of resource:
    - Storage Account
        - provides a unique namespace in Azure.
        - Every object inside the storage account has the unique namespace,
        - The default blob storage endpoint: http://< storage account >.blob.core.winows.net
        - Types of storage account:
            - Standard, General purpose V2, Standard storage account type for blobs, file shares, queues, and tables. Recommended for most scenarios using Blob Storage or one of the other Azure Storage services.
            - Premium, block blob, Premium storage account type for block blobs and append blobs. Recommended for scenarios with high transaction rates or that use smaller objects or require consistently low storage latency. 
            - Premium, page blobs, Premium storage account type for page blobs only.
    - Container
        - A container organizes a set of blobs, similar to a directory in a file system. A storage account can include an unlimited number of containers, and a container can store an unlimited number of blobs.
        - A container name must be a valid DNS name, as it forms part of the unique URI (Uniform resource identifier) used to address the container or its blobs. Follow these rules when naming a container:
            - Container names can be between 3 and 63 characters long.
            - Container names must start with a letter or number, and can contain only lowercase letters, numbers, and the dash (-) character.
            - Two or more consecutive dash characters aren't permitted in container names.
        - The URL: https://< storage account >.blob.core.windows.net/< blob >
    - Blob
        - Azure Storage supports three types of blobs:

            - Block blobs store text and binary data. Block blobs are made up of blocks of data that can be managed individually. Block blobs can store up to about 190.7 TiB.
            - Append blobs are made up of blocks like block blobs, but are optimized for append operations. Append blobs are ideal for scenarios such as logging data from virtual machines.
            - Page blobs store random access files up to 8 TiB in size. Page blobs store virtual hard drive (VHD) files and serve as disks for Azure virtual machines. For more information about page blobs, see Overview of Azure page blobs

        - For more information about the different types of blobs, see Understanding Block Blobs, Append Blobs, and Page Blobs.

        - The URI for a blob is similar to: https://myaccount.blob.core.windows.net/mycontainer/myblob

##### Provision in Azure Console
- Set Subscription
- Set Resource goup
- Set storage account name
    - Must be unique, hav between 3 and 24 letters, must have only lowercase number nd letters.
- Set region
- Set Performance
    - Standard
    - Premium
- Set Redundancy
    - LRS
    - ZRS
    - GRS
    - GZRS
- Enable require secure transfer for REST API operation.
- Enable allow public acccess on containers.
- Enable authorize Azure active directory to access blobs, queues and table.
- Set the minimum TLS version to access your storage account.
- Set permitted scope for copy operations to any storage account, to same ad tenant or private linkin the same network.
- Set enable Data Lake Gen 2
- Set access tier
    - hot
    - cool
- Set network access
    - public access to all networks
    - public access from selected virtual networks and ip addresses
    - disable public access and use private access
- Set networking routing
    - microsoft
    - internet
- set enable point-in-ime restore
- set enable soft delete to blob
- set enable soft delete to container
- set enable soft delete to files shares
- set enable versioning
- set enable blob change feed
- set encryption type
    - microsoft-managed key
    - customer-managed key
        - blobs and files only
        - all service
- enable infrastructure encryption
- Tags

##### Redundancy
Multiple copies of data are stored. THis helps to protect against planned and unplanned -trasient, hardware failures, network or power outages. So in such events, there are different redundancy options to check.
- LRS: against server hack failure. Three copies of date is made in one datacenter. Three synchronous   copies of data in the same data center.
- ZRS: against data-center failures. The data is replicated synchronously across three azure availability. Three synchronous copies of data in three availability zone.
- GRS: failover in second region. The data is replicated to other region. AFter the primary goes down, so the second region is available to access. Three synchronous copy in he same data center and asynchronous copy to secondary region.
- GZRS: LRS+ZRS
- Read-GRS: both primary and second region is available to read.
- Read-GZRS: both primary and second region is available to read.


##### Authorization

##### Security

##### Scalability

##### Access Tier
Organize your data based on attirbutes like frequency of access and planned retention period.
- Hot
    - frequently accessed data and day-to-day usage scenarios.
    - low latency
    - higher access cost
- Cool
    - infrequently accessed data and backup scenarios. The data is stored at least 30 days.
    - high latency
    - lower cost
    - stored for at least 30 days
- Archive: 
    - you have o rehydrate the file to access the file. It takes time to rehydrate the file. The data is stored at least 180 days.
    - rarely accessed data
    - highest access time and access cost
    - latency in hours
    - Stored for at least 180 days
