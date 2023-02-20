# Storage Account Types

- Standard
- General-Purpose V2
- Blob Storage, Data Lake, Queue, Table, Files
- LRS, ZRS, GRS, RA-GRS, GZRS, RA-GZRS
- Standard storage account type for blobs, file shares, queues, and tables. Recommended for most scenarios using Azure Storage. If you want support for network fule system (NFS) n Azure Files, use the the premium file shares account type

######

- Premium
- Block Blob
- Blob Storage, Data Lake
- LRS, ZRS
- Premium storage accout type for block blobs and append blob. Recommended for scenarios with high transaction rates or that use smaller objects or require consistently low storage latency.

######

- Premium
- File shares
- LRS, ZRS
- Premium storage account type for file shares only. Recommended for enterpriseor high-performance scale applications. Use this account type if you want a storage accountthat suports both Server Message Block (SMB) and NFS FIle Shares.

######

- Premium
- Page blob
- Page blob only
- LRS
- Premium storage account typefor page blob nly

######
