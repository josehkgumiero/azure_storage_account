# Prerequisites

Before you configure object replication, create the source and destination storage accounts if they don't already exist. The source and destination accounts can be either general-purpose v2 storage accounts or premium block blob accounts.

Object replication requires that blob versioning is enabled for both the source and destination account, and that blob change feed is enabled for the source account.

To configure an object replication policy for a storage account, you must be assigned the Azure Resource Manager Contributor role, scoped to the level of the storage account or higher. 