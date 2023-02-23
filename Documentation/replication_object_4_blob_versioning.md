# Blob versioning

Object replication requires that blob versioning is enabled on both the source and destination accounts. When a replicated blob in the source account is modified, a new version of the blob is created in the source account that reflects the previous state of the blob, before modification. The current version in the source account reflects the most recent updates. Both the current version and any previous versions are replicated to the destination account.

If your storage account has object replication policies in effect, you cannot disable blob versioning for that account. You must delete any object replication policies on the account before disabling blob versioning.
