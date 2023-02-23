# Object replication policies and rules

When you configure object replication, you create a replication policy that specifies the source storage account and the destination account. A replication policy includes one or more rules that specify a source container and a destination container and indicate which block blobs in the source container will be replicated.

After you configure object replication, Azure Storage checks the change feed for the source account periodically and asynchronously replicates any write or delete operations to the destination account. Replication latency depends on the size of the block blob being replicated.