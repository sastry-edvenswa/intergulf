#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportLoadsTruckTimes

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportLoadsTruckTimes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:46:31 PM Thursday, January 7, 2021 |
| Last Modified | 6:32:41 PM Thursday, January 7, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Load Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| DispatchStatus | varchar(50) | 50 |
| LegNumber | int | 4 |
| BeginningDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| StartTime | numeric(18,2) | 9 |
| PickupLocationArrivalTime | numeric(18,2) | 9 |
| PickupLocationDepartTime | numeric(18,2) | 9 |
| DeliveryLocationArrivalTime | numeric(18,2) | 9 |
| DeliveryLocationDepartTime | numeric(18,2) | 9 |
| EndTime | numeric(18,2) | 9 |
| Leg Time | numeric(19,2) | 9 |
| AddWashOut | bit | 1 |
| TPAddWashOut | bit | 1 |
| AccountingStatus | varchar(40) | 40 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportLoadsTruckTimes]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id AS [Load Id], dbo.Loads.ScheduledDate, dbo.Loads.DispatchStatus, dbo.LoadsBilling.LegNumber, dbo.LoadsBilling.BeginningDate, dbo.LoadsBilling.TruckId, 
                         dbo.LoadsBilling.StartTime, dbo.LoadsBilling.PickupLocationArrivalTime, dbo.LoadsBilling.PickupLocationDepartTime, dbo.LoadsBilling.DeliveryLocationArrivalTime, 
                         dbo.LoadsBilling.DeliveryLocationDepartTime, dbo.LoadsBilling.EndTime, dbo.LoadsBilling.EndTime - dbo.LoadsBilling.StartTime AS [Leg Time], dbo.LoadsBillingSummary.AddWashOut, 
                         dbo.LoadsBillingSummary.TPAddWashOut, dbo.Loads.AccountingStatus
FROM            dbo.Loads RIGHT OUTER JOIN
                         dbo.LoadsBilling ON dbo.Loads.Id = dbo.LoadsBilling.LoadId RIGHT OUTER JOIN
                         dbo.LoadsBillingSummary ON dbo.Loads.Id = dbo.LoadsBillingSummary.LoadId
ORDER BY dbo.Loads.ScheduledDate, dbo.LoadsBilling.TruckId, [Load Id]
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBilling]](../Tables/dbo_LoadsBilling.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

