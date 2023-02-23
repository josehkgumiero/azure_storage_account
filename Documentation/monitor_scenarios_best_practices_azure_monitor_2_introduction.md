# Introduction to Storage insights

Before diving into the experience, you should understand how it presents and visualizes information. Whether you select the Storage feature directly from a storage account or from Azure Monitor, Storage insights presents a consistent experience.

Combined it delivers:

- At scale perspective showing a snapshot view of their availability based on the health of the storage service or the API operation, utilization showing total number of requests that the storage service receives, and latency showing the average time the storage service or API operation type is taking to process requests. You can also view capacity by blob, file, table, and queue.

- Drill down analysis of a particular storage account to help diagnose issues or perform detailed analysis by category - availability, performance, failures, and capacity. Selecting any one of those options provides an in-depth view of metrics.

- Customizable where you can change which metrics you want to see, modify or set thresholds that align with your limits, and save as your own workbook. Charts in the workbook can be pinned to Azure dashboard.

This feature does not require you to enable or configure anything, the storage metrics from your storage accounts are collected by default. If you are unfamiliar with metrics available on Azure Storage, view the description and definition in Azure Storage metrics by reviewing Azure storage metrics.