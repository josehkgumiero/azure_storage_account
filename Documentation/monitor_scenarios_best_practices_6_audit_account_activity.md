# Audit account activity

In many cases, you'll need to audit the activities of your storage accounts for security and compliance. Operations on storage accounts fall into two categories: Control Plane and Data Plane.

A control plane operation is any Azure Resource Manager request to create a storage account or to update a property of an existing storage account. 

A data plane operation is an operation on the data in a storage account that results from a request to the storage service endpoint. For example, a data plane operation is executed when you upload a blob to a storage account or download a blob from a storage account. 

