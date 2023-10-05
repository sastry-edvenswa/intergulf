#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsScheduled

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsScheduled]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:45:24 AM Wednesday, August 2, 2017 |
| Last Modified | 12:45:24 AM Wednesday, August 2, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| LoadId | bigint | 8 |
| ScheduledDate | date | 3 |
| ScheduledTime | varchar(5) | 5 |
| ScheduledTimeUnits | int | 4 |
| StartDateTime | bigint | 8 |
| EndDateTime | bigint | 8 |
| ArrivalDate | date | 3 |
| ArrivalTime | varchar(50) | 50 |
| LabCheckInDate | date | 3 |
| LabCheckInTime | varchar(5) | 5 |
| RackNo | varchar(50) | 50 |
| PumpNo | varchar(50) | 50 |
| PadStartDate | date | 3 |
| PadStartTime | varchar(5) | 5 |
| PadStopDate | date | 3 |
| PadStopTime | varchar(5) | 5 |
| PumpStartDate | date | 3 |
| PumpStartTime | varchar(5) | 5 |
| PumpStopDate | date | 3 |
| PumpStopTime | varchar(5) | 5 |
| LabCheckOutDate | date | 3 |
| LabCheckOutTime | varchar(5) | 5 |
| Status | varchar(50) | 50 |
| OverRideStatus | varchar(50) | 50 |
| CreateUser | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| CreateComputer | varchar(50) | 50 |
| UpdateUser | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |
| UpdateComputer | varchar(50) | 50 |
| ScheduledStartDateTime | datetime | 8 |
| ScheduledEndDateTime | datetime | 8 |
| ActualPumpNo | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| SpecialEquipment | varchar(3000) | 3000 |
| SpecialInstructions | varchar(3000) | 3000 |
| SortOrder | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsScheduled]
AS
SELECT        dbo.LoadsSchedule.Id, dbo.LoadsSchedule.LoadId, dbo.LoadsSchedule.ScheduledDate, dbo.LoadsSchedule.ScheduledTime, 
                         dbo.LoadsSchedule.ScheduledTimeUnits, dbo.LoadsSchedule.StartDateTime, dbo.LoadsSchedule.EndDateTime, dbo.LoadsSchedule.ArrivalDate, 
                         dbo.LoadsSchedule.ArrivalTime, dbo.LoadsSchedule.LabCheckInDate, dbo.LoadsSchedule.LabCheckInTime, dbo.LoadsSchedule.RackNo, 
                         dbo.LoadsSchedule.PumpNo, dbo.LoadsSchedule.PadStartDate, dbo.LoadsSchedule.PadStartTime, dbo.LoadsSchedule.PadStopDate, 
                         dbo.LoadsSchedule.PadStopTime, dbo.LoadsSchedule.PumpStartDate, dbo.LoadsSchedule.PumpStartTime, dbo.LoadsSchedule.PumpStopDate, 
                         dbo.LoadsSchedule.PumpStopTime, dbo.LoadsSchedule.LabCheckOutDate, dbo.LoadsSchedule.LabCheckOutTime, dbo.LoadsSchedule.Status, 
                         dbo.LoadsSchedule.OverRideStatus, dbo.LoadsSchedule.CreateUser, dbo.LoadsSchedule.CreateDateTime, dbo.LoadsSchedule.CreateComputer, 
                         dbo.LoadsSchedule.UpdateUser, dbo.LoadsSchedule.UpdateDateTime, dbo.LoadsSchedule.UpdateComputer, dbo.LoadsSchedule.ScheduledStartDateTime, 
                         dbo.LoadsSchedule.ScheduledEndDateTime, dbo.LoadsSchedule.ActualPumpNo, dbo.Profile.MaterialDescription, dbo.Profile.SpecialEquipment, 
                         dbo.Profile.SpecialInstructions, dbo.Pumps.SortOrder
FROM            dbo.Pumps RIGHT OUTER JOIN
                         dbo.LoadsSchedule ON dbo.Pumps.Id = dbo.LoadsSchedule.PumpNo LEFT OUTER JOIN
                         dbo.Profile INNER JOIN
                         dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId ON dbo.LoadsSchedule.LoadId = dbo.Loads.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Pumps]](../Tables/dbo_Pumps.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

