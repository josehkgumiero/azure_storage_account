# Identity And Access Management
######
- Use Azure Active Directory (Azure AD) to authorize access to blob data
- Azure AD provides superior security and ease of use over Shared Key for authorizing requests to Blob storage.
######
- Keep in mind the principle of least privilege when assigning permissions to an Azure AD security principal via Azure RBAC
- When assigning a role to a user, group, or application, grant that security principal only those permissions that are necessary for them to perform their tasks. Limiting access to resources helps prevent both unintentional and malicious misuse of your data.
######
- Use a user delegation SAS to grant limited access to blob data to clients
- A user delegation SAS is secured with Azure Active Directory (Azure AD) credentials and also by the permissions specified for the SAS. A user delegation SAS is analogous to a service SAS in terms of its scope and function, but offers security benefits over the service SAS.
######
- Secure your account access keys with Azure Key Vault
- Microsoft recommends using Azure AD to authorize requests to Azure Storage. However, if you must use Shared Key authorization, then secure your account keys with Azure Key Vault. You can retrieve the keys from the key vault at runtime, instead of saving them with your application.
######
- Regenerate your account keys periodically
- Rotating the account keys periodically reduces the risk of exposing your data to malicious actors.
######
- Disallow Shared Key authorization
- When you disallow Shared Key authorization for a storage account, Azure Storage rejects all subsequent requests to that account that are authorized with the account access keys. Only secured requests that are authorized with Azure AD will succeed.
######
- Keep in mind the principle of least privilege when assigning permissions to a SAS
- When creating a SAS, specify only those permissions that are required by the client to perform its function. Limiting access to resources helps prevent both unintentional and malicious misuse of your data.
######
- Have a revocation plan in place for any SAS that you issue to clients
- If a SAS is compromised, you will want to revoke that SAS as soon as possible. To revoke a user delegation SAS, revoke the user delegation key to quickly invalidate all signatures associated with that key. To revoke a service SAS that is associated with a stored access policy, you can delete the stored access policy, rename the policy, or change its expiry time to a time that is in the past. 
######
- If a service SAS is not associated with a stored access policy, then set the expiry time to one hour or less
- A service SAS that is not associated with a stored access policy cannot be revoked. For this reason, limiting the expiry time so that the SAS is valid for one hour or less is recommended.
######
- Disable anonymous public read access to containers and blobs
- Anonymous public read access to a container and its blobs grants read-only access to those resources to any client. Avoid enabling public read access unless your scenario requires it. 