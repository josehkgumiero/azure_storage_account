# Prerequisites and caveats for object replication

Object replication requires that the following Azure Storage features are also enabled:

- Change feed: Must be enabled on the source account.
- Blob versioning: Must be enabled on both the source and destination accounts. 

Enabling change feed and blob versioning may incur additional costs.

Object replication is supported for general-purpose v2 storage accounts and premium block blob accounts. Both the source and destination accounts must be either general-purpose v2 or premium block blob accounts. Object replication supports block blobs only; append blobs and page blobs aren't supported.

Object replication is supported for accounts that are encrypted with either microsoft-managed keys or customer-managed keys. 

Object replication isn't supported for blobs in the source account that are encrypted with a customer-provided key. 

Customer-managed failover isn't supported for either the source or the destination account in an object replication policy.
