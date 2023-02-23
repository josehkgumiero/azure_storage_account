# Detailed storage workbooks

Whether you selected a value in the columns Availability, E2E Latency, Server Latency, and transaction error type/Errors from the multiple storage account Overview workbook, or selecting any one of buttons for Failures, Performance, Availability, and Capacity from the Overview workbook from a specific storage account, each deliver a set of interactive storage-related information tailored to that category.

- Availability opens the Availability workbook. It shows the current health state of Azure Storage service, a table showing the available health state of each object categorized by data service defined in the storage account with a trend line representing the time range selected, and an availability trend chart for each data service in the account.

- E2E Latency and Server Latency opens the Performance workbook. It includes a rollup status tile showing E2E latency and server latency, a performance chart of E2E versus server latency, and a table breaking down latency of successful calls by API categorized by data service defined in the storage account.

- Selecting any of the error categories listed in the grid open the Failure workbook. The report shows metric tiles of all other client-side errors except described ones and successful requests, client-throttling errors, a performance chart for the transaction Response Type dimension metric specific to ClientOtherError attribute, and two tables - Transactions by API name and Transactions by Response type.

- Capacity opens the Capacity workbook. It shows the total amount of storage used for each storage data object in the account in the tiles and the chart, and how many data objects are stored in the account.