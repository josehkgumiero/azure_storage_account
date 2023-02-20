# Networking
######
- Configure the minimum required version of Transport Layer Security (TLS) for a storage account.
- Require that clients use a more secure version of TLS to make requests against an Azure Storage account by configuring the minimum version of TLS for that account. 
######
- Enable the Secure transfer required option on all of your storage accounts
- When you enable the Secure transfer required option, all requests made against the storage account must take place over secure connections. Any requests made over HTTP will fail. 
######
- Enable firewall rules
- Configure firewall rules to limit access to your storage account to requests that originate from specified IP addresses or ranges, or from a list of subnets in an Azure Virtual Network (VNet).
######
- Allow trusted Microsoft services to access the storage account
- Turning on firewall rules for your storage account blocks incoming requests for data by default, unless the requests originate from a service operating within an Azure Virtual Network (VNet) or from allowed public IP addresses. Requests that are blocked include those from other Azure services, from the Azure portal, from logging and metrics services, and so on. You can permit requests from other Azure services by adding an exception to allow trusted Microsoft services to access the storage account.
######
- Use private endpoints
- A private endpoint assigns a private IP address from your Azure Virtual Network (VNet) to the storage account. It secures all traffic between your VNet and the storage account over a private link.
######
- Use VNet service tags
- A service tag represents a group of IP address prefixes from a given Azure service. Microsoft manages the address prefixes encompassed by the service tag and automatically updates the service tag as addresses change.
######
- Limit network access to specific networks
- Limiting network access to networks hosting clients requiring access reduces the exposure of your resources to network attacks.
######
- Configure network routing preference
- You can configure network routing preference for your Azure storage account to specify how network traffic is routed to your account from clients over the Internet using the Microsoft global network or Internet routing. 
