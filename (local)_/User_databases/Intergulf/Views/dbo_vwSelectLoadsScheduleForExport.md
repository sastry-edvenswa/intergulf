#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsScheduleForExport

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsScheduleForExport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:16:06 PM Tuesday, March 6, 2018 |
| Last Modified | 10:16:06 PM Tuesday, March 6, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| TruckId | varchar(50) | 50 |
| ScheduledDate | varchar(30) | 30 |
| ScheduledTime | varchar(30) | 30 |
| Generator | varchar(100) | 100 |
| TrailerId | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| Destination | nvarchar(100) | 200 |
| Transporter | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsScheduleForExport]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Loads.TruckId, CONVERT(varchar, dbo.Loads.ScheduledDate, 101) AS ScheduledDate, CONVERT(varchar, 
                         dbo.Loads.ScheduledTime, 108) AS ScheduledTime, dbo.Generator.Name AS Generator, dbo.Loads.TrailerId, dbo.Profile.Direction, 
                         dbo.Destination.Name AS Destination, dbo.Transporter.Name AS Transporter, dbo.Loads.DispatchStatus
FROM            dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Loads.TransporterId = dbo.Transporter.Id
WHERE        (dbo.Loads.ScheduledDate = CONVERT(DATETIME, '2018-02-01 00:00:00', 102))
ORDER BY dbo.Loads.TruckId, CONVERT(varchar, dbo.Loads.ScheduledDate, 101), CONVERT(varchar, dbo.Loads.ScheduledTime, 108)

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

