# Azure DNS Zone Endpoints
- When you create an Azure Storage account with Azure DNS zone endpoints (preview), Azure Storage dynamically selects an Azure DNS zone and assigns it to the storage account when it is created. The new storage account's endpoints are created in the dynamically selected Azure DNS zone.
- An Azure DNS zone service endpoint in Azure Storage includes the protocol (HTTPS is recommended), the storage account name as the subdomain, and a domain that includes the name of the service and the identifier for the DNS zone. 
DNS Zone endpoint:
- Blob Storage:	https://<storage-account>.z[00-99].blob.storage.azure.net
- Static website (Blob Storage): https://<storage-account>.z[00-99].web.storage.azure.net
- Data Lake Storage Gen2: https://<storage-account>.z[00-99].dfs.storage.azure.net
- Azure Files: https://<storage-account>.z[00-99].file.storage.azure.net
- Queue Storage: https://<storage-account>.z[00-99].queue.storage.azure.net
- Table Storage: https://<storage-account>.z[00-99].table.storage.azure.net