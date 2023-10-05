#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadBillingDetail

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadBillingDetail]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 5:08:01 PM Tuesday, April 17, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ScheduledDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| PickupLocationArrivalTime | numeric(18,2) | 9 |
| PickupLocationDepartTime | numeric(18,2) | 9 |
| DeliveryArrivalTime | numeric(18,2) | 9 |
| DeliveryDepartTime | numeric(18,2) | 9 |
| PickupDepartTime | numeric(18,2) | 9 |
| DeliveryCompleteTime | numeric(18,2) | 9 |
| BillingDepartment | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLoadBillingDetail]
AS
SELECT     TOP 100 PERCENT dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.Id, dbo.Generator.Name AS [Generator Name], 
                      dbo.Loads.PickupLocationArrivalTime, dbo.Loads.PickupLocationDepartTime, dbo.Loads.DeliveryArrivalTime, dbo.Loads.DeliveryDepartTime, 
                      dbo.Loads.PickupDepartTime, dbo.Loads.DeliveryCompleteTime, dbo.Loads.BillingDepartment, dbo.Loads.BillingStatus, dbo.Loads.VesselTank
FROM         dbo.Generator RIGHT OUTER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId RIGHT OUTER JOIN
                      dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId
ORDER BY dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

