# DAX Measures

## Total Customers

```DAX
Total Customers =
DISTINCTCOUNT(Marketing_Data[ID])
Total Spending =
SUM(Marketing_Data[TotalSpent])
Average Spending =
AVERAGE(Marketing_Data[TotalSpent])
Total Purchases =
SUM(Marketing_Data[TotalPurchases])
Average Income =
AVERAGE(Marketing_Data[Income])
Total Campaign Responses =
CALCULATE(
    DISTINCTCOUNT(Marketing_Data[ID]),
    Marketing_Data[Response] = 1
Total Campaign Responses =
CALCULATE(
    DISTINCTCOUNT(Marketing_Data[ID]),
    Marketing_Data[Response] = 1
)

Campaign Response Rate =
DIVIDE(
    [Total Campaign Responses],
    [Total Customers],
    0
)

Average Recency =
AVERAGE(Marketing_Data[Recency])

Total Campaigns Accepted =
SUM(Marketing_Data[TotalCampaignsAccepted])

Complaint Rate =
DIVIDE(
    CALCULATE(
        DISTINCTCOUNT(Marketing_Data[ID]),
        Marketing_Data[Complain] = 1
    ),
    [Total Customers],
    0
)

Web Purchases =
SUM(Marketing_Data[NumWebPurchases])

Catalog Purchases =
SUM(Marketing_Data[NumCatalogPurchases])

Store Purchases =
SUM(Marketing_Data[NumStorePurchases])

