# Authorize with Shared Key

Every request made against a storage service must be authorized, unless the request is for a blob or container resource that has been made available for public or signed access. One option for authorizing a request is by using Shared Key, described in this article.
######
Tip
- Azure Storage supports integration with Azure Active Directory for fine-grained control over access to storage resources. Azure AD integration is supported for the Blob and Queue services. Because Azure AD provides identity management, you can authorize access to storage resources without storing your account access keys in your applications, as you do with Shared Key. For more information, see Authorize with Azure Active Directory.
######
The Blob, Queue, Table, and File services support the following Shared Key authorization schemes for version 2009-09-19 and later (for Blob, Queue, and Table service) and version 2014-02-14 and later (for File service):

- Shared Key for Blob, Queue, and File Services. Use the Shared Key authorization scheme to make requests against the Blob, Queue, and File services. Shared Key authorization in version 2009-09-19 and later supports an augmented signature string for enhanced security and requires that you update your service to authorize using this augmented signature.

- Shared Key for Table Service. Use the Shared Key authorization scheme to make requests against the Table service using the REST API. Shared Key authorization for the Table service in version 2009-09-19 and later uses the same signature string as in previous versions of the Table service.

- Shared Key Lite. Use the Shared Key Lite authorization scheme to make requests against the Blob, Queue, Table, and File services.