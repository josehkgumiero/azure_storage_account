# Storage Account Authorization Operations

# Azure Blobs

- Shared Key
- Shared Access Signature
- Azure Active Directory
- Anonymous public read access (Not recommended)
- Storage local users (only SFTP)

# Azure Files (SMB)

- Shared Key
- Azure Active Directory
- On-premises Active Directory Domain Services

# Azure Files (REST)

- Shared Key
- SHared access signature

# Azure Queue

- Shared Key
- Shared Access Signature
- Azure Active Directory

# Azure Tables

- Shared Key
- Shared Access Signature
- Azure Active Directory


######

Shared Key authorization for blobs, files, queues, and tables. A client using Shared Key passes a header with every request that is signed using the storage account access key. For more information, see Authorize with Shared Key.

Microsoft recommends that you disallow Shared Key authorization for your storage account. When Shared Key authorization is disallowed, clients must use Azure AD or a user delegation SAS to authorize requests for data in that storage account.

######

Shared access signatures for blobs, files, queues, and tables. Shared access signatures (SAS) provide limited delegated access to resources in a storage account via a signed URL. The signed URL specifies the permissions granted to the resource and the interval over which the signature is valid. A service SAS or account SAS is signed with the account key, while the user delegation SAS is signed with Azure AD credentials and applies to blobs only. 

######

Azure Active Directory (Azure AD) integration for authorizing requests to blob, queue, and table resources. Microsoft recommends using Azure AD credentials to authorize requests to data when possible for optimal security and ease of use.

You can use Azure role-based access control (Azure RBAC) to manage a security principal's permissions to blob, queue, and table resources in a storage account. You can also use Azure attribute-based access control (ABAC) to add conditions to Azure role assignments for blob resources.

######

Azure Active Directory Domain Services (Azure AD DS) authentication for Azure Files. Azure Files supports identity-based authorization over Server Message Block (SMB) through Azure AD DS. You can use Azure RBAC for granular control over a client's access to Azure Files resources in a storage account. 

######

On-premises Active Directory Domain Services (AD DS, or on-premises AD DS) authentication for Azure Files. Azure Files supports identity-based authorization over SMB through AD DS. Your AD DS environment can be hosted in on-premises machines or in Azure VMs. SMB access to Files is supported using AD DS credentials from domain joined machines, either on-premises or in Azure. You can use a combination of Azure RBAC for share level access control and NTFS DACLs for directory/file level permission enforcement. 

######

Anonymous public read access for blob data is supported, but not recommended. When anonymous access is configured, clients can read blob data without authorization. We recommend that you disable anonymous access for all of your storage accounts.

######

Storage Local Users can be used to access blobs with SFTP or files with SMB. Storage Local Users support container level permissions for authorization.


