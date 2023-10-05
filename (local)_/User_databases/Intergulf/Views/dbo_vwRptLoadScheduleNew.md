#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadScheduleNew

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadScheduleNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:38:11 PM Thursday, January 30, 2014 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| LastName | varchar(50) | 50 |
| ScheduledTime | datetime | 8 |
| FirstName | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| VesselTank | varchar(100) | 100 |
| TruckId | varchar(50) | 50 |
| Truck Description | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Trailer Description | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| Destination | nvarchar(100) | 200 |
| Direction | varchar(50) | 50 |
| FacilityName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLoadScheduleNew]
AS
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Driver.LastName, dbo.Loads.ScheduledTime, dbo.Driver.FirstName, 
                      dbo.Generator.Name AS [Generator Name], dbo.Profile.ProfileNumber, dbo.Profile.MaterialDescription, dbo.Loads.VesselTank, dbo.Loads.TruckId, 
                      dbo.Equipment.Description AS [Truck Description], dbo.Loads.TrailerId, Equipment_1.Description AS [Trailer Description], dbo.Loads.DispatchStatus, 
                      dbo.Destination.Name AS Destination, dbo.Profile.Direction, dbo.Destination.FacilityName
FROM         dbo.Destination RIGHT OUTER JOIN
                      dbo.Loads ON dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                      dbo.Equipment ON dbo.Loads.TruckId = dbo.Equipment.Id LEFT OUTER JOIN
                      dbo.Equipment Equipment_1 ON dbo.Loads.TrailerId = Equipment_1.Id LEFT OUTER JOIN
                      dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id LEFT OUTER JOIN
                      dbo.Generator RIGHT OUTER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
ORDER BY dbo.Profile.Direction, dbo.Destination.FacilityName, dbo.Loads.ScheduledDate, dbo.Driver.LastName, dbo.Loads.ScheduledTime

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

