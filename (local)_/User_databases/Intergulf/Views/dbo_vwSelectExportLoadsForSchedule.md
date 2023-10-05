#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportLoadsForSchedule

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportLoadsForSchedule]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:51:25 PM Monday, April 23, 2018 |
| Last Modified | 3:15:55 PM Wednesday, May 22, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| DriverId | bigint | 8 |
| GeneratorId | bigint | 8 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Id | bigint | 8 |
| Generator | varchar(100) | 100 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| Direction | varchar(50) | 50 |
| Destination | nvarchar(100) | 200 |
| DispatchStatus | varchar(50) | 50 |
| MaterialClassification | varchar(200) | 200 |
| ProfileType | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportLoadsForSchedule]
AS
SELECT        TOP (100) PERCENT dbo.Loads.DriverId, dbo.Profile.GeneratorId, dbo.Loads.TruckId, dbo.Loads.TrailerId, dbo.Loads.Id, dbo.Generator.Name AS Generator, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, 
                         dbo.Profile.Direction, dbo.Destination.Name AS Destination, dbo.Loads.DispatchStatus, dbo.Profile.MaterialClassification, dbo.Profile.ProfileType
FROM            dbo.Destination RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                         dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
ORDER BY dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.ScheduledTime
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

