# Assign Azure roles for access rights
######
Azure Active Directory (Azure AD) authorizes access rights to secured resources through Azure RBAC. Azure Storage defines a set of built-in RBAC roles that encompass common sets of permissions used to access blob data. You can also define custom roles for access to blob data.
######
An Azure AD security principal may be a user, a group, an application service principal, or a managed identity for Azure resources. The RBAC roles that are assigned to a security principal determine the permissions that the principal has for the specified resource. 
######
In some cases you may need to enable fine-grained access to blob resources or to simplify permissions when you have a large number of role assignments for a storage resource. You can use Azure attribute-based access control (Azure ABAC) to configure conditions on role assignments. You can use conditions with a custom role or select built-in roles. 