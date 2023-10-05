#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadForSchedule

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadForSchedule]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:19:56 PM Tuesday, February 16, 2016 |
| Last Modified | 10:19:56 PM Tuesday, February 16, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| LoadNo | bigint | 8 | 0 - 0 |
| Generator | varchar(100) | 100 |  |
| ProfileNo | varchar(50) | 50 |  |
| RequestedDate | datetime | 8 |  |
| RequestedTime | datetime | 8 |  |
| ScheduledDate | datetime | 8 |  |
| ScheduledTime | datetime | 8 |  |
| MaterialDescription | varchar(3000) | 3000 |  |
| Direction | varchar(50) | 50 |  |
| ProfileType | varchar(50) | 50 |  |
| DispatchStatus | varchar(50) | 50 |  |
| LoadRequestId | bigint | 8 |  |
| LabTestId | bigint | 8 |  |
| TruckId | varchar(50) | 50 |  |
| Description | varchar(50) | 50 |  |
| WasteCode | varchar(50) | 50 |  |
| VesselTank | varchar(100) | 100 |  |
| Destination | nvarchar(100) | 200 |  |
| SpecialRequirements | varchar(3000) | 3000 |  |
| BlindLoadId | bigint | 8 |  |
| DestinationId | bigint | 8 |  |
| TankNumber | varchar(50) | 50 |  |
| DeliveryReleaseNumber | varchar(50) | 50 |  |
| Notes | varchar(6000) | 6000 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadForSchedule]
AS
SELECT     TOP (100) PERCENT dbo.Loads.Id AS LoadNo, dbo.Generator.Name AS Generator, dbo.Profile.ProfileNumber AS ProfileNo, dbo.Loads.RequestedDate, 
                      dbo.Loads.RequestedTime, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Profile.MaterialDescription, dbo.Profile.Direction, dbo.Profile.ProfileType, 
                      dbo.Loads.DispatchStatus, dbo.Loads.LoadRequestId, dbo.Loads.LabTestId, dbo.Loads.TruckId, dbo.Equipment.Description, dbo.Profile.WasteCode, 
                      dbo.Loads.VesselTank, dbo.Destination.Name AS Destination, dbo.Loads.SpecialRequirements, dbo.Loads.BlindLoadId, dbo.Loads.DestinationId, 
                      dbo.Loads.TankNumber, dbo.Loads.DeliveryReleaseNumber, dbo.Loads.Notes
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                      dbo.Equipment ON dbo.Loads.TruckId = dbo.Equipment.Id LEFT OUTER JOIN
                      dbo.Customer RIGHT OUTER JOIN
                      dbo.Profile ON dbo.Customer.Id = dbo.Profile.CustomerId ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
ORDER BY dbo.Loads.ScheduledDate

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

