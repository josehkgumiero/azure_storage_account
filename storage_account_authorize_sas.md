# Delegate access by using a shared access signature
######
A shared access signature (SAS) is a URI that grants restricted access rights to Azure Storage resources. You can provide a shared access signature to clients who shouldn't be trusted with your storage account key but who need access to certain storage account resources. By distributing a SAS URI to these clients, you can grant them access to a resource for a specified period of time, with a specified set of permissions.
######
The URI query parameters that compose the SAS token incorporate all of the information necessary to grant controlled access to a storage resource. A client who has the SAS can make a request against Azure Storage by using just the SAS URI. The information in the SAS token is used to authorize the request.