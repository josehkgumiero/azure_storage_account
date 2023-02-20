# Destination Limitations

The following limitations apply only to monitoring Azure Storage accounts.

- You can't send logs to the same storage account that you are monitoring with this setting.
    - This would lead to recursive logs in which a log entry describes the writing of another log entry. You must create an account or use another existing account to store log information.

- You can't set a retention policy.
    - If you archive logs to a storage account, you can manage the retention policy of a log container by defining a lifecycle management policy. To learn how, see Optimize costs by automating Azure Blob Storage access tiers.

    - If you send logs to Log Analytics, you can manage the data retention period of Log Analytics at the workspace level or even specify different retention settings by data type. 
