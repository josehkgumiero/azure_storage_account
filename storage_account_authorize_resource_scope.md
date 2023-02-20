# Resource scope

######

Before you assign an Azure RBAC role to a security principal, determine the scope of access that the security principal should have. Best practices dictate that it's always best to grant only the narrowest possible scope. Azure RBAC roles defined at a broader scope are inherited by the resources beneath them.

######

You can scope access to Azure blob resources at the following levels, beginning with the narrowest scope:

- An individual container. At this scope, a role assignment applies to all of the blobs in the container, and to the container properties and metadata.
- The storage account. At this scope, a role assignment applies to all containers and their blobs.
- The resource group. At this scope, a role assignment applies to all of the containers in all of the storage accounts in the resource group.
- The subscription. At this scope, a role assignment applies to all of the containers in all of the storage accounts in all of the resource groups in the subscription.
- A management group. At this scope, a role assignment applies to all of the containers in all of the storage accounts in all of the resource groups in all of the subscriptions in the management group.
