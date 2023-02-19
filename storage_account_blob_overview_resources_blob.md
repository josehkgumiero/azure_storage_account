# Blobs
- Azure Storage supports three types of blobs:
    - Block blobs store text and binary data. Block blobs are made up of blocks of data that can be managed individually. Block blobs can store up to about 190.7 TiB.
    - Append blobs are made up of blocks like block blobs, but are optimized for append operations. Append blobs are ideal for scenarios such as logging data from virtual machines.
    - Page blobs store random access files up to 8 TiB in size. Page blobs store virtual hard drive (VHD) files and serve as disks for Azure virtual machines. For more information about page blobs, see - Overview of Azure page blobs

- The URI for a blob is similar to:
    - https://myaccount.blob.core.windows.net/mycontainer/myblob
    - https://myaccount.blob.core.windows.net/mycontainer/myvirtualdirectory/myblob

- Follow these rules when naming a blob:
    - A blob name can contain any combination of characters.
    - A blob name must be at least one character long and cannot be more than 1,024 characters long, for blobs in Azure Storage.
    - Blob names are case-sensitive.
    - Reserved URL characters must be properly escaped.
    - The number of path segments comprising the blob name cannot exceed 254. A path segment is the string between consecutive delimiter characters (e.g., the forward slash '/') that corresponds to the name of a virtual directory.