# Data Protection
######
- Use the Azure Resource Manager deployment model
- Create new storage accounts using the Azure Resource Manager deployment model for important security enhancements, including superior Azure role-based access control (Azure RBAC) and auditing, Resource Manager-based deployment and governance, access to managed identities, access to Azure Key Vault for secrets, and Azure AD-based authentication and authorization for access to Azure Storage data and resources. If possible, migrate existing storage accounts that use the classic deployment model to use Azure Resource Manager.
######
- Enable Microsoft Defender for all of your storage accounts
- Microsoft Defender for Storage provides an additional layer of security intelligence that detects unusual and potentially harmful attempts to access or exploit storage accounts. Security alerts are triggered in Microsoft Defender for Cloud when anomalies in activity occur and are also sent via email to subscription administrators, with details of suspicious activity and recommendations on how to investigate and remediate threats.
######
- Turn on soft delete for blobs
- Soft delete for blobs enables you to recover blob data after it has been deleted.
######
- Turn on soft delete for containers
- Soft delete for containers enables you to recover a container after it has been deleted.
######
- Lock storage account to prevent accidental or malicious deletion or configuration changes
- Apply an Azure Resource Manager lock to your storage account to protect the account from accidental or malicious deletion or configuration change. Locking a storage account does not prevent data within that account from being deleted. It only prevents the account itself from being deleted.
######
- Store business-critical data in immutable blobs
- Configure legal holds and time-based retention policies to store blob data in a WORM (Write Once, Read Many) state. Blobs stored immutably can be read, but cannot be modified or deleted for the duration of the retention interval.
######
- Require secure transfer (HTTPS) to the storage account
- When you require secure transfer for a storage account, all requests to the storage account must be made over HTTPS. Any requests made over HTTP are rejected. Microsoft recommends that you always require secure transfer for all of your storage accounts.
######
- Limit shared access signature (SAS) tokens to HTTPS connections only
- Requiring HTTPS when a client uses a SAS token to access blob data helps to minimize the risk of eavesdropping.