# Analyzing Logs

######
You can access resource logs either as a blob in a storage account, as event data, or through Log Analytics queries.

######
All resource logs in Azure Monitor have the same fields followed by service-specific fields. The common schema is outlined in Azure Monitor resource log schema. The schema for Azure Blob Storage resource logs is found in Azure Blob Storage monitoring data reference.

######
To get the list of SMB and REST operations that are logged, see Storage logged operations and status messages.

######
Log entries are created only if there are requests made against the service endpoint. For example, if a storage account has activity in its file endpoint but not in its table or queue endpoints, only logs that pertain to the Azure Blob Storage service are created. Azure Storage logs contain detailed information about successful and failed requests to a storage service. This information can be used to monitor individual requests and to diagnose issues with a storage service. Requests are logged on a best-effort basis.

######
The Activity log is a type of platform log located in Azure that provides insight into subscription-level events. You can view it independently or route it to Azure Monitor Logs, where you can do much more complex queries using Log Analytics.

When you view a storage account in the Azure portal, the operations called by the portal are also logged. For this reason, you may see operations logged in a storage account even though you have not written any data to the account.