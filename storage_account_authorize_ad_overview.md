# Azure AD For Blobs Overview

When a security principal (a user, group, or application) attempts to access a blob resource, the request must be authorized, unless it's a blob available for anonymous access. With Azure AD, access to a resource is a two-step process:

1. First, the security principal's identity is authenticated and an OAuth 2.0 token is returned. The authentication step requires that an application request an OAuth 2.0 access token at runtime. If an application is running from within an Azure entity such as an Azure VM, a virtual machine scale set, or an Azure Functions app, it can use a managed identity to access blob data.

2. Next, the token is passed as part of a request to the Blob service and used by the service to authorize access to the specified resource. The authorization step requires that one or more Azure RBAC roles be assigned to the security principal making the request. 