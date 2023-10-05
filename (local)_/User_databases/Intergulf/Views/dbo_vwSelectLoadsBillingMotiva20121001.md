#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsBillingMotiva20121001

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsBillingMotiva20121001]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:38:50 PM Monday, May 26, 2014 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadId | bigint | 8 |
| LegNumber | int | 4 |
| BeginningDate | datetime | 8 |
| StartTime | numeric(18,2) | 9 |
| PickupLocationArrivalTime | numeric(18,2) | 9 |
| PickupLocationDepartTime | numeric(18,2) | 9 |
| DeliveryLocationArrivalTime | numeric(18,2) | 9 |
| DeliveryLocationDepartTime | numeric(18,2) | 9 |
| EndTime | numeric(18,2) | 9 |
| BillingTime | numeric(18,2) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsBillingMotiva20121001]
AS
SELECT     TOP 100 PERCENT dbo.LoadsBilling.LoadId, dbo.LoadsBilling.LegNumber, dbo.LoadsBilling.BeginningDate, dbo.LoadsBilling.StartTime, 
                      dbo.LoadsBilling.PickupLocationArrivalTime, dbo.LoadsBilling.PickupLocationDepartTime, dbo.LoadsBilling.DeliveryLocationArrivalTime, 
                      dbo.LoadsBilling.DeliveryLocationDepartTime, dbo.LoadsBilling.EndTime, dbo.LoadsBillingSummary.BillingTime
FROM         dbo.LoadsBilling LEFT OUTER JOIN
                      dbo.LoadsBillingSummary ON dbo.LoadsBilling.LoadId = dbo.LoadsBillingSummary.LoadId
ORDER BY dbo.LoadsBilling.LoadId, dbo.LoadsBilling.LegNumber

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadsBilling]](../Tables/dbo_LoadsBilling.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectLoadsMotiva20121001]](dbo_vwSelectLoadsMotiva20121001.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

