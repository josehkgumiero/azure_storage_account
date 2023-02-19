# Storage Account Creating

## Basics

- Subscription: select the subscription for the new storage account.
- Resource group: create new resource group or select an existing one.
- Storage account name: choose a unique name. It must be between 3 and 2 characters in length and may contain lowercase letters and numbers.
- Region: select the appropriate region for your storage account.
- Perormance: select standard for the general-purpose v2, it is for most scenarios. Or select premium for scenarios requiring low latency.
- Redundancy: select the desired redundacy configuration.

# Advanced

- Require secure transfer for REST API operations: Require secure transfer to ensure that incoming requests to this storage account are made only via HTTPS (default). 
- Allow enabling public access on containers: When enabled, this setting allows a user with the appropriate permissions to enable anonymous public access to a container in the storage account (default). Disabling this setting prevents all anonymous public access to the storage account.
- Enable storage account key access: When enabled, this setting allows clients to authorize requests to the storage account using either the account access keys or an Azure Active Directory (Azure AD) account (default). Disabling this setting prevents authorization with the account access keys.
- Default to Azure Active Directory authorization in the Azure portal: When enabled, the Azure portal authorizes data operations with the user's Azure AD credentials by default. If the user does not have the appropriate permissions assigned via Azure role-based access control (Azure RBAC) to perform data operations, then the portal will use the account access keys for data access instead. 
- Minimum TLS version: Select the minimum version of Transport Layer Security (TLS) for incoming requests to the storage account. The default value is TLS version 1.2. When set to the default value, incoming requests made using TLS 1.0 or TLS 1.1 are rejected.
- Enable hierarchical namespace: To use this storage account for Azure Data Lake Storage Gen2 workloads, configure a hierarchical namespace.
- Enable SFTP: Enable the use of Secure File Transfer Protocol (SFTP) to securely transfer of data over the internet.
- Enable network file system (NFS) v3: NFS v3 provides Linux file system compatibility at object storage scale enables Linux clients to mount a container in Blob storage from an Azure Virtual Machine (VM) or a computer on-premises.
- Allow cross-tenant replication: By default, users with appropriate permissions can configure object replication across Azure AD tenants. To prevent replication across tenants, deselect this option.
- Access tier: Blob access tiers enable you to store blob data in the most cost-effective manner, based on usage. Select the hot tier (default) for frequently accessed data. Select the cool tier for infrequently accessed data.
- Enable large file shares: Available only for standard file shares with the LRS or ZRS redundancies.

## Networking

- Network access: By default, incoming network traffic is routed to the public endpoint for your storage account. You can specify that traffic must be routed to the public endpoint through an Azure virtual network.
- Endpoint type: Azure Storage supports two types of endpoints: standard endpoints (the default) and Azure DNS zone endpoints (preview).
- Routing preference: The network routing preference specifies how network traffic is routed to the public endpoint of your storage account from clients over the internet. By default, a new storage account uses Microsoft network routing. You can also choose to route network traffic through the POP closest to the storage account, which may lower networking costs.

## Data Protection

- Enable point-in-time restore for containers: Point-in-time restore provides protection against accidental deletion or corruption by enabling you to restore block blob data to an earlier state. Enabling point-in-time restore also enables blob versioning, blob soft delete, and blob change feed. These prerequisite features may have a cost impact.

- Enable soft delete for blobs: Blob soft delete protects an individual blob, snapshot, or version from accidental deletes or overwrites by maintaining the deleted data in the system for a specified retention period. During the retention period, you can restore a soft-deleted object to its state at the time it was deleted.

- Enable soft delete for containers: Container soft delete protects a container and its contents from accidental deletes by maintaining the deleted data in the system for a specified retention period. During the retention period, you can restore a soft-deleted container to its state at the time it was deleted.

- Enable soft delete for file shares: Soft delete for file shares protects a file share and its contents from accidental deletes by maintaining the deleted data in the system for a specified retention period. During the retention period, you can restore a soft-deleted file share to its state at the time it was deleted.

- Enable blob change feed: The blob change feed provides transaction logs of all changes to all blobs in your storage account, as well as to their metadata.

- Enable version-level immutability support: Enable support for immutability policies that are scoped to the blob version. If this option is selected, then after you create the storage account, you can configure a default time-based retention policy for the account or for the container, which blob versions within the account or container will inherit by default.

## Encryption

- Encryption type: By default, data in the storage account is encrypted by using Microsoft-managed keys. You can rely on Microsoft-managed keys for the encryption of your data, or you can manage encryption with your own keys.

- Enable support for customer-managed keys:  	By default, customer managed keys can be used to encrypt only blobs and files. Set this option to All service types (blobs, files, tables, and queues) to enable support for customer-managed keys for all services. You are not required to use customer-managed keys if you choose this option.

- Enable infrastructure encryption: By default, infrastructure encryption is not enabled. Enable infrastructure encryption to encrypt your data at both the service level and the infrastructure level. 