# Storage Account Endpoints

#####

A Storage account provides a uique namespacein Azure for your data. Every object that you store in Azure Storage has a URL address that includes your unique account name. The combination ofthe account name and the service endpoint forms the endpoint for your storage account.

#####

There are two types of endpoint services availables for a storage account:
- Standard: you can create up to 250 per region.
- DNS Zone: you can create up to 5000 per region.

#####

Standard endpoint:
- blob storage: https://< storage account >.blob.core.windows.net
- website: https://< storage account >.web.core.windows.net
- data lake: https://< storage account >.dfs.core.windows.net
- files: https://< storage account >.file.core.windows.net
- queue: https://< storage account >.queue.core.windows.net
- table: https://< storage account >.table.core.windows.net

#####

DNS Zone endpoint:
- Blob Storage:	https://<storage-account>.z[00-99].blob.storage.azure.net
- Static website (Blob Storage): https://<storage-account>.z[00-99].web.storage.azure.net
- Data Lake Storage Gen2: https://<storage-account>.z[00-99].dfs.storage.azure.net
- Azure Files: https://<storage-account>.z[00-99].file.storage.azure.net
- Queue Storage: https://<storage-account>.z[00-99].queue.storage.azure.net
- Table Storage: https://<storage-account>.z[00-99].table.storage.azure.net