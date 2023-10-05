#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsScheduledForChart

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsScheduledForChart]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:09:55 AM Wednesday, January 13, 2016 |
| Last Modified | 8:09:55 AM Wednesday, January 13, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| LoadId | bigint | 8 |  |
| ScheduledDate | date | 3 |  |
| ScheduledTime | varchar(5) | 5 |  |
| ScheduledTimeUnits | int | 4 |  |
| StartDateTime | bigint | 8 |  |
| EndDateTime | bigint | 8 |  |
| ArrivalDate | date | 3 |  |
| ArrivalTime | varchar(50) | 50 |  |
| LabCheckInDate | date | 3 |  |
| LabCheckInTime | varchar(5) | 5 |  |
| RackNo | varchar(50) | 50 |  |
| PumpNo | varchar(50) | 50 |  |
| PadStartDate | date | 3 |  |
| PadStartTime | varchar(5) | 5 |  |
| PadStopDate | date | 3 |  |
| PadStopTime | varchar(5) | 5 |  |
| LabCheckOutDate | date | 3 |  |
| LabCheckOutTime | varchar(5) | 5 |  |
| Status | varchar(50) | 50 |  |
| OverRideStatus | varchar(50) | 50 |  |
| CreateUser | varchar(50) | 50 |  |
| CreateDateTime | datetime | 8 |  |
| CreateComputer | varchar(50) | 50 |  |
| UpdateUser | varchar(50) | 50 |  |
| UpdateDateTime | datetime | 8 |  |
| UpdateComputer | varchar(50) | 50 |  |
| ScheduledStartDateTime | datetime | 8 |  |
| ScheduledEndDateTime | datetime | 8 |  |
| ActualPumpNo | varchar(50) | 50 |  |
| MaterialDescription | varchar(3000) | 3000 |  |
| SpecialEquipment | varchar(3000) | 3000 |  |
| SpecialInstructions | varchar(3000) | 3000 |  |
| DispatchStatus | varchar(50) | 50 |  |
| Direction | varchar(50) | 50 |  |
| DestinationFacility | varchar(50) | 50 |  |
| GeneratorFacility | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsScheduledForChart]
AS
SELECT     dbo.LoadsSchedule.Id, dbo.LoadsSchedule.LoadId, dbo.LoadsSchedule.ScheduledDate, dbo.LoadsSchedule.ScheduledTime, 
                      dbo.LoadsSchedule.ScheduledTimeUnits, dbo.LoadsSchedule.StartDateTime, dbo.LoadsSchedule.EndDateTime, dbo.LoadsSchedule.ArrivalDate, 
                      dbo.LoadsSchedule.ArrivalTime, dbo.LoadsSchedule.LabCheckInDate, dbo.LoadsSchedule.LabCheckInTime, dbo.LoadsSchedule.RackNo, 
                      dbo.LoadsSchedule.PumpNo, dbo.LoadsSchedule.PadStartDate, dbo.LoadsSchedule.PadStartTime, dbo.LoadsSchedule.PadStopDate, 
                      dbo.LoadsSchedule.PadStopTime, dbo.LoadsSchedule.LabCheckOutDate, dbo.LoadsSchedule.LabCheckOutTime, dbo.LoadsSchedule.Status, 
                      dbo.LoadsSchedule.OverRideStatus, dbo.LoadsSchedule.CreateUser, dbo.LoadsSchedule.CreateDateTime, dbo.LoadsSchedule.CreateComputer, 
                      dbo.LoadsSchedule.UpdateUser, dbo.LoadsSchedule.UpdateDateTime, dbo.LoadsSchedule.UpdateComputer, dbo.LoadsSchedule.ScheduledStartDateTime, 
                      dbo.LoadsSchedule.ScheduledEndDateTime, dbo.LoadsSchedule.ActualPumpNo, dbo.Profile.MaterialDescription, dbo.Profile.SpecialEquipment, 
                      dbo.Profile.SpecialInstructions, dbo.Loads.DispatchStatus, dbo.Profile.Direction, dbo.Destination.Facility AS DestinationFacility, 
                      dbo.Generator.Facility AS GeneratorFacility
FROM         dbo.Generator RIGHT OUTER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId RIGHT OUTER JOIN
                      dbo.Destination INNER JOIN
                      dbo.Loads ON dbo.Destination.Id = dbo.Loads.DestinationId ON dbo.Profile.Id = dbo.Loads.ProfileId RIGHT OUTER JOIN
                      dbo.LoadsSchedule ON dbo.Loads.Id = dbo.LoadsSchedule.LoadId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

