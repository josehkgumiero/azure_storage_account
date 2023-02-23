# Replication status

You can check the replication status for a blob in the source account.

If the replication status for a blob in the source account indicates failure, then investigate the following possible causes:

- Make sure that the object replication policy is configured on the destination account.
- Verify that the destination account still exists.
- Verify that the destination container still exists.
- Verify that the destination container is not in the process of being deleted, or has not just been deleted. Deleting a container may take up to 30 seconds.
- Verify that the destination container is still participating in the object replication policy.
- If the source blob has been encrypted with a customer-provided key as part of a write operation, then object replication will fail. For more information about customer-provided keys, see Provide an encryption key on a request to Blob storage.
- Check whether the source or destination blob has been moved to the Archive tier. Archived blobs cannot be replicated via object replication. For more information about the Archive tier, see Hot, Cool, and Archive access tiers for blob data.
- Verify that destination container or blob is not protected by an immutability policy. Keep in mind that a container or blob can inherit an immutability policy from its parent. For more information about immutability policies, see Overview of immutable storage for blob data.
