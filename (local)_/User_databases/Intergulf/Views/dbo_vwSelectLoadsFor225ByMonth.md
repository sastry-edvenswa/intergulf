#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsFor225ByMonth

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsFor225ByMonth]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:17:55 PM Tuesday, October 4, 2016 |
| Last Modified | 8:20:36 PM Tuesday, October 4, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadId | bigint | 8 |
| ScheduledDate | date | 3 |
| Receive Date | datetime | 8 |
| Name | varchar(100) | 100 |
| MaterialDescription | varchar(3000) | 3000 |
| Direction | varchar(50) | 50 |
| Destination | nvarchar(100) | 200 |
| Pump Description | varchar(50) | 50 |
| Pump No | bigint | 8 |
| TankNumber | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |
| DispatchStatus | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| AccountingAction | varchar(40) | 40 |
| Accountingnotes | varchar(3000) | 3000 |
| Scheduled Status | varchar(50) | 50 |
| Scheduled ORide | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsFor225ByMonth]
AS
SELECT     TOP (100) PERCENT dbo.LoadsSchedule.LoadId, dbo.LoadsSchedule.ScheduledDate, dbo.Loads.ScheduledDate AS [Receive Date], dbo.Generator.Name, dbo.Profile.MaterialDescription, 
                      dbo.Profile.Direction, dbo.Destination.Name AS Destination, dbo.Pumps.Description AS [Pump Description], dbo.Pumps.Number AS [Pump No], dbo.Loads.TankNumber, dbo.Loads.VesselTank, 
                      dbo.Loads.DispatchStatus, dbo.LoadsBillingSummary.BillingDepartment, dbo.LoadsBillingSummary.BillingStatus, dbo.Loads.AccountingAction, dbo.Loads.Accountingnotes, 
                      dbo.LoadsSchedule.Status AS [Scheduled Status], dbo.LoadsSchedule.OverRideStatus AS [Scheduled ORide]
FROM         dbo.Pumps INNER JOIN
                      dbo.LoadsSchedule ON dbo.Pumps.Id = dbo.LoadsSchedule.PumpNo LEFT OUTER JOIN
                      dbo.LoadsBillingSummary ON dbo.LoadsSchedule.LoadId = dbo.LoadsBillingSummary.LoadId LEFT OUTER JOIN
                      dbo.Profile INNER JOIN
                      dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId INNER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id INNER JOIN
                      dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id ON dbo.LoadsSchedule.LoadId = dbo.Loads.Id
WHERE     (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2016-09-01 00:00:00', 102)) AND (dbo.Loads.ScheduledDate <= CONVERT(DATETIME, '2016-09-30 00:00:00', 102))
ORDER BY [Receive Date], dbo.LoadsSchedule.LoadId
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Pumps]](../Tables/dbo_Pumps.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

