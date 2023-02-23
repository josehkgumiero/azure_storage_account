# Overview workbook

On the Overview workbook for the selected subscription, the table displays interactive storage metrics and service availability state for up to 5 storage accounts grouped within the subscription. You can filter the results based on the options you select from the following drop-down lists:

- Subscriptions - only subscriptions that have storage accounts are listed.

- Storage Accounts - by default, 5 storage accounts are pre-selected. If you select all or multiple storage accounts in the scope selector, up to 200 storage accounts will be returned. For example, if you had a total of 573 storage accounts across three subscriptions that you've selected, only 200 accounts would be displayed.

- Time Range - by default, displays the last 4 hours of information based on the corresponding selections made.

The counter tile under the drop-down lists rolls-up the total number of storage accounts in the subscription and reflects how many of the total are selected. There is conditional color-coding or heatmaps for columns in the workbook that report transaction metrics or errors. The deepest color has the highest value and a lighter color is based on the lowest values. For the error-based columns, the value is in red and for the metric-based columns, the value is in blue.

Select a value in the columns Availability, E2E Latency, Server Latency, and transaction error type/Errors directs you to a report tailored to the specific type of storage metrics that match the column selected for that storage account. For more information about the workbooks for each category, see the Detailed storage workbooks section below.

Note

For details on which errors can be shown in the report, see Response Type schema and look for response types such as ServerOtherError, ClientOtherError, ClientThrottlingError. Depending on the storage accounts selected, if there are more than three types of errors reported, all other errors are represented under the category of Other.

The default Availability threshold is:

- Warning - 99%
- Critical - 90%

To set an availability threshold based on the results of your observation or requirements, review modify the availability threshold.