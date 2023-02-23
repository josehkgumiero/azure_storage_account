# Replication policies

When you configure object replication, you create a replication policy on the destination account via the Azure Storage resource provider. After the replication policy is created, Azure Storage assigns it a policy ID. You must then associate that replication policy with the source account by using the policy ID. The policy ID on the source and destination accounts must be the same in order for replication to take place.

A source account can replicate to no more than two destination accounts, with one policy for each destination account. Similarly, an account may serve as the destination account for no more than two replication policies.

The source and destination accounts may be in the same region or in different regions. They may also reside in the same subscription or in different subscriptions. Optionally, the source and destination accounts may reside in different Azure Active Directory (Azure AD) tenants. Only one replication policy may be created for each source account/destination account pair.