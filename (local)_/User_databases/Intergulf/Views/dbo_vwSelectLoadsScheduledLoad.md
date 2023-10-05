#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsScheduledLoad

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsScheduledLoad]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:22:12 PM Monday, March 28, 2016 |
| Last Modified | 9:22:12 PM Monday, March 28, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| LoadId | bigint | 8 |  |
| TruckId | varchar(50) | 50 |  |
| TrailerId | varchar(50) | 50 |  |
| DriverId | bigint | 8 |  |
| TransporterId | bigint | 8 |  |
| PumpNo | varchar(50) | 50 |  |
| LoadScheduledDate | datetime | 8 |  |
| LoadScheduledTime | datetime | 8 |  |
| ScheduledDate | date | 3 |  |
| ScheduledTime | varchar(5) | 5 |  |
| ArrivalDate | date | 3 |  |
| ArrivalTime | varchar(50) | 50 |  |
| LabCheckInDate | date | 3 |  |
| LabCheckInTime | varchar(5) | 5 |  |
| PadStartDate | date | 3 |  |
| PadStartTime | varchar(5) | 5 |  |
| PadStopDate | date | 3 |  |
| PadStopTime | varchar(5) | 5 |  |
| LabCheckOutDate | date | 3 |  |
| LabCheckOutTime | varchar(5) | 5 |  |
| Status | varchar(50) | 50 |  |
| ActualPumpNo | varchar(50) | 50 |  |
| VesselTank | varchar(100) | 100 |  |
| DestinationId | bigint | 8 |  |
| DeliveryReleaseNumber | varchar(50) | 50 |  |
| TankNumber | varchar(50) | 50 |  |
| PumpStartDate | date | 3 |  |
| PumpStartTime | varchar(5) | 5 |  |
| PumpStopDate | date | 3 |  |
| PumpStopTime | varchar(5) | 5 |  |
| Notes | varchar(6000) | 6000 |  |
| CompleteDate | date | 3 |  |
| CompleteTime | varchar(5) | 5 |  |
| SpecialRequirements | varchar(3000) | 3000 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsScheduledLoad]
AS
SELECT     dbo.Loads.Id, dbo.LoadsSchedule.LoadId, dbo.Loads.TruckId, dbo.Loads.TrailerId, dbo.Loads.DriverId, dbo.Loads.TransporterId, dbo.LoadsSchedule.PumpNo, 
                      dbo.Loads.ScheduledDate AS LoadScheduledDate, dbo.Loads.ScheduledTime AS LoadScheduledTime, dbo.LoadsSchedule.ScheduledDate, 
                      dbo.LoadsSchedule.ScheduledTime, dbo.LoadsSchedule.ArrivalDate, dbo.LoadsSchedule.ArrivalTime, dbo.LoadsSchedule.LabCheckInDate, 
                      dbo.LoadsSchedule.LabCheckInTime, dbo.LoadsSchedule.PadStartDate, dbo.LoadsSchedule.PadStartTime, dbo.LoadsSchedule.PadStopDate, 
                      dbo.LoadsSchedule.PadStopTime, dbo.LoadsSchedule.LabCheckOutDate, dbo.LoadsSchedule.LabCheckOutTime, dbo.LoadsSchedule.Status, 
                      dbo.LoadsSchedule.ActualPumpNo, dbo.Loads.VesselTank, dbo.Loads.DestinationId, dbo.Loads.DeliveryReleaseNumber, dbo.Loads.TankNumber, 
                      dbo.LoadsSchedule.PumpStartDate, dbo.LoadsSchedule.PumpStartTime, dbo.LoadsSchedule.PumpStopDate, dbo.LoadsSchedule.PumpStopTime, dbo.Loads.Notes, 
                      dbo.LoadsSchedule.CompleteDate, dbo.LoadsSchedule.CompleteTime, dbo.Loads.SpecialRequirements
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.LoadsSchedule ON dbo.Loads.Id = dbo.LoadsSchedule.LoadId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

