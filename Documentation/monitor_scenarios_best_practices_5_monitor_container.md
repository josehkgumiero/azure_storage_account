# Monitor the use of a container

If you partition your customer's data by container, then can monitor how much capacity is used by each customer. You can use Azure Storage blob inventory to take an inventory of blobs with size information. Then, you can aggregate the size and count at the container level.

You can also evaluate traffic at the container level by querying logs.

- Here's a query to get the number of read transactions and the number of bytes read on each container.
```
StorageBlobLogs
| where OperationName  == "GetBlob"
| extend ContainerName = split(parse_url(Uri).Path, "/")[1]
| summarize ReadSize = sum(ResponseBodySize), ReadCount = count() by tostring(ContainerName)
```

- The following query uses a similar query to obtain information about write operations.
```
StorageBlobLogs
| where OperationName == "PutBlob" or
  OperationName == "PutBlock" or
  OperationName == "PutBlockList" or
  OperationName == "AppendBlock" or
  OperationName == "SnapshotBlob" or
  OperationName == "CopyBlob" or
  OperationName == "SetBlobTier"
| extend ContainerName = split(parse_url(Uri).Path, "/")[1]
| summarize WriteSize = sum(RequestBodySize), WriteCount = count() by tostring(ContainerName)
```