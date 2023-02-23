# Object replication for block blobs

Object replication asynchronously copies block blobs between a source storage account and a destination account. Some scenarios supported by object replication include:

- Minimizing latency. Object replication can reduce latency for read requests by enabling clients to consume data from a region that is in closer physical proximity.
- Increase efficiency for compute workloads. With object replication, compute workloads can process the same sets of block blobs in different regions.
- Optimizing data distribution. You can process or analyze data in a single location and then replicate just the results to additional regions.
- Optimizing costs. After your data has been replicated, you can reduce costs by moving it to the archive tier using life cycle management policies.

