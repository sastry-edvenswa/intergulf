#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptSelectSchedulePumpTimes

# ![Views](../../../../Images/View32.png) [dbo].[vwRptSelectSchedulePumpTimes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:48:48 PM Tuesday, March 29, 2016 |
| Last Modified | 9:48:48 PM Tuesday, March 29, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadId | bigint | 8 |
| GeneratorName | varchar(100) | 100 |
| ScheduledDate | date | 3 |
| ScheduledTime | varchar(5) | 5 |
| PumpNo | varchar(50) | 50 |
| ActualPumpNo | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| Number | bigint | 8 |
| ScheduledTimeUnits | int | 4 |
| StartDateTime | bigint | 8 |
| EndDateTime | bigint | 8 |
| ArrivalDate | date | 3 |
| ArrivalTime | varchar(50) | 50 |
| LabCheckInDate | date | 3 |
| LabCheckInTime | varchar(5) | 5 |
| RackNo | varchar(50) | 50 |
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
| CompleteDate | date | 3 |
| CompleteTime | varchar(5) | 5 |
| Status | varchar(50) | 50 |
| OverRideStatus | varchar(50) | 50 |
| ScheduledStartDateTime | datetime | 8 |
| ScheduledEndDateTime | datetime | 8 |
| VesselTank | varchar(100) | 100 |
| TankNumber | varchar(50) | 50 |
| SortOrder | bigint | 8 |
| CreateDateTime | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptSelectSchedulePumpTimes]
AS
SELECT     TOP (100) PERCENT dbo.LoadsSchedule.LoadId, dbo.Generator.Name AS GeneratorName, dbo.LoadsSchedule.ScheduledDate, dbo.LoadsSchedule.ScheduledTime, 
                      dbo.LoadsSchedule.PumpNo, dbo.LoadsSchedule.ActualPumpNo, dbo.Pumps.Description, dbo.Pumps.Number, dbo.LoadsSchedule.ScheduledTimeUnits, 
                      dbo.LoadsSchedule.StartDateTime, dbo.LoadsSchedule.EndDateTime, dbo.LoadsSchedule.ArrivalDate, dbo.LoadsSchedule.ArrivalTime, 
                      dbo.LoadsSchedule.LabCheckInDate, dbo.LoadsSchedule.LabCheckInTime, dbo.LoadsSchedule.RackNo, dbo.LoadsSchedule.PadStartDate, 
                      dbo.LoadsSchedule.PadStartTime, dbo.LoadsSchedule.PadStopDate, dbo.LoadsSchedule.PadStopTime, dbo.LoadsSchedule.PumpStartDate, 
                      dbo.LoadsSchedule.PumpStartTime, dbo.LoadsSchedule.PumpStopDate, dbo.LoadsSchedule.PumpStopTime, dbo.LoadsSchedule.LabCheckOutDate, 
                      dbo.LoadsSchedule.LabCheckOutTime, dbo.LoadsSchedule.CompleteDate, dbo.LoadsSchedule.CompleteTime, dbo.LoadsSchedule.Status, 
                      dbo.LoadsSchedule.OverRideStatus, dbo.LoadsSchedule.ScheduledStartDateTime, dbo.LoadsSchedule.ScheduledEndDateTime, dbo.Loads.VesselTank, 
                      dbo.Loads.TankNumber, dbo.Pumps.SortOrder, dbo.LoadsSchedule.CreateDateTime
FROM         dbo.Pumps INNER JOIN
                      dbo.LoadsSchedule ON dbo.Pumps.Id = dbo.LoadsSchedule.PumpNo LEFT OUTER JOIN
                      dbo.Profile INNER JOIN
                      dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId INNER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.LoadsSchedule.LoadId = dbo.Loads.Id
ORDER BY dbo.LoadsSchedule.ScheduledDate, dbo.Pumps.SortOrder, dbo.LoadsSchedule.ScheduledTime

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Pumps]](../Tables/dbo_Pumps.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

