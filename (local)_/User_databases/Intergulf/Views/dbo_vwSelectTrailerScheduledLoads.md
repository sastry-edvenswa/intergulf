#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectTrailerScheduledLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectTrailerScheduledLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:37:59 PM Thursday, August 10, 2017 |
| Last Modified | 11:37:59 PM Thursday, August 10, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| LoadRequestId | bigint | 8 |
| LabTestId | bigint | 8 |
| TruckId | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| Destination Name | nvarchar(100) | 200 |
| BlindLoadId | bigint | 8 |
| DocumentNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| Destination | nvarchar(100) | 200 |
| TrailerId | varchar(50) | 50 |
| Location | varchar(50) | 50 |
| LocationStatus | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectTrailerScheduledLoads]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], 
                         dbo.Profile.ProfileNumber AS [Profile Number], dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Profile.ProfileType, dbo.Profile.Direction, 
                         dbo.Loads.DispatchStatus, dbo.Loads.LoadRequestId, dbo.Loads.LabTestId, dbo.Loads.TruckId, dbo.Equipment.Description, dbo.Profile.WasteCode, 
                         Destination_1.Name AS [Destination Name], dbo.Loads.BlindLoadId, dbo.Loads.DocumentNumber, dbo.Loads.DeliveryReleaseNumber, 
                         dbo.Destination.Name AS Destination, dbo.Loads.TrailerId, Equipment_1.Location, Equipment_1.LocationStatus
FROM            dbo.Equipment INNER JOIN
                         dbo.Equipment AS Equipment_1 ON dbo.Equipment.Id = Equipment_1.Id RIGHT OUTER JOIN
                         dbo.Loads ON Equipment_1.Id = dbo.Loads.TrailerId LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Destination AS Destination_1 ON dbo.Loads.DestinationId = Destination_1.Id LEFT OUTER JOIN
                         dbo.Customer RIGHT OUTER JOIN
                         dbo.Profile ON dbo.Customer.Id = dbo.Profile.CustomerId ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
ORDER BY dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

