# Specify full resource IDs for the source and destination accounts

When you create the policy definition file, specify the full Azure Resource Manager resource IDs for the sourceAccount and destinationAccount entries, as shown in the example in the previous section. The full resource ID is in the following format:

```
/subscriptions/<subscriptionId>/resourceGroups/<resource-group>/providers/Microsoft.Storage/storageAccounts/<storage-account>
```

The policy definition file previously required only the account name, instead of the full resource ID for the storage account. With the introduction of the AllowCrossTenantReplication security property in version 2021-02-01 of the Azure Storage resource provider REST API, you must now provide the full resource ID for any object replication policies that are created when cross-tenant replication is disallowed for a storage account that participates in the replication policy. Azure Storage uses the full resource ID to verify whether the source and destination accounts reside within the same tenant. 

While providing only the account name is still supported when cross-tenant replication is allowed for a storage account, Microsoft recommends always providing the full resource ID as a best practice. All previous versions of the Azure Storage resource provider REST API support using the full resource ID path in object replication policies.