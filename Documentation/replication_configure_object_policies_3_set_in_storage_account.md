# Configure object replication with access to both storage accounts

If you have access to both the source and destination storage accounts, then you can configure the object replication policy on both accounts.

When you configure object replication in the Azure portal, you only need to configure the policy on the source account. The Azure portal automatically creates the policy on the destination account after you configure it for the source account.

To create a replication policy in the Azure portal, follow these steps:

- Navigate to the source storage account in the Azure portal.

- Under Data management, select Object replication.

- Select Set up replication rules.

- Select the destination subscription and storage account.

- In the Container pairs section, select a source container from the source account, and a destination container from the destination account. You can create up to 10 container pairs per replication policy from the Azure portal.

- If desired, specify one or more filters to copy only blobs that match a prefix pattern. For example, if you specify a prefix b, only blobs whose name begin with that letter are replicated. You can specify a virtual directory as part of the prefix. You can add a maximum of up to five prefix matches. The prefix string doesn't support wildcard characters.

- By default, the copy scope is set to copy only new objects. To copy all objects in the container or to copy objects starting from a custom date and time, select the change link and configure the copy scope for the container pair.

- By default, the copy scope is set to copy only new objects. To copy all objects in the container or to copy objects starting from a custom date and time, select the change link and configure the copy scope for the container pair.