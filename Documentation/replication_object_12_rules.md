# Replication rules

Replication rules specify how Azure Storage will replicate blobs from a source container to a destination container. You can specify up to 1000 replication rules for each replication policy. Each replication rule defines a single source and destination container, and each source and destination container can be used in only one rule, meaning that a maximum of 1000 source containers and 1000 destination containers may participate in a single replication policy.

When you create a replication rule, by default only new block blobs that are subsequently added to the source container are copied. You can specify that both new and existing block blobs are copied, or you can define a custom copy scope that copies block blobs created from a specified time onward.

You can also specify one or more filters as part of a replication rule to filter block blobs by prefix. When you specify a prefix, only blobs matching that prefix in the source container will be copied to the destination container.

The source and destination containers must both exist before you can specify them in a rule. After you create the replication policy, write operations to the destination container aren't permitted. Any attempts to write to the destination container fail with error code 409 (Conflict). To write to a destination container for which a replication rule is configured, you must either delete the rule that is configured for that container, or remove the replication policy. Read and delete operations to the destination container are permitted when the replication policy is active.

You can call the Set Blob Tier operation on a blob in the destination container to move it to the archive tier.