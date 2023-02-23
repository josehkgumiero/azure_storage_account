# Immutable blobs

Immutability policies for Azure Blob Storage include time-based retention policies and legal holds. When an immutability policy is in effect on the destination account, object replication may be affected.

If a container-level immutability policy is in effect for a container in the destination account, and an object in the source container is updated or deleted, then the operation on the source container may succeed, but replication of that operation to the destination container will fail.

If a version-level immutability policy is in effect for a blob version in the destination account, and a delete or update operation is performed on the blob version in the source container, then the operation on the source object may succeed, but replication of that operation to the destination object will fail.