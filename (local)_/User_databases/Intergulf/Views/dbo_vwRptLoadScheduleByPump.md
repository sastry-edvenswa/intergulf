#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadScheduleByPump

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadScheduleByPump]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:01:31 PM Thursday, March 3, 2016 |
| Last Modified | 9:01:31 PM Thursday, March 3, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadId | bigint | 8 |
| GeneratorName | varchar(100) | 100 |
| Direction | varchar(50) | 50 |
| PumpNo | int | 4 |
| SPumpNo | bigint | 8 |
| SSortOrder | bigint | 8 |
| SPumpDesc | varchar(50) | 50 |
| ActualPumpNo | varchar(50) | 50 |
| APumpNo | bigint | 8 |
| ASortOrder | bigint | 8 |
| APumpDesc | varchar(50) | 50 |
| ScheduledDate | date | 3 |
| ScheduledTime | varchar(5) | 5 |
| LabCheckInDate | date | 3 |
| LabCheckInTime | varchar(5) | 5 |
| LabCheckOutDate | date | 3 |
| LabCheckOutTime | varchar(5) | 5 |
| Status | varchar(50) | 50 |
| OverRideStatus | varchar(50) | 50 |
| StartDateTime | bigint | 8 |
| EndDateTime | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLoadScheduleByPump]
AS
SELECT     TOP (100) PERCENT dbo.LoadsSchedule.LoadId, dbo.Generator.Name AS GeneratorName, dbo.Profile.Direction, CONVERT(int, dbo.LoadsSchedule.PumpNo) 
                      AS PumpNo, dbo.Pumps.Number AS SPumpNo, dbo.Pumps.SortOrder AS SSortOrder, dbo.Pumps.Description AS SPumpDesc, dbo.LoadsSchedule.ActualPumpNo, 
                      Pumps_1.Number AS APumpNo, Pumps_1.SortOrder AS ASortOrder, Pumps_1.Description AS APumpDesc, dbo.LoadsSchedule.ScheduledDate, 
                      dbo.LoadsSchedule.ScheduledTime, dbo.LoadsSchedule.LabCheckInDate, dbo.LoadsSchedule.LabCheckInTime, dbo.LoadsSchedule.LabCheckOutDate, 
                      dbo.LoadsSchedule.LabCheckOutTime, dbo.LoadsSchedule.Status, dbo.LoadsSchedule.OverRideStatus, dbo.LoadsSchedule.StartDateTime, 
                      dbo.LoadsSchedule.EndDateTime
FROM         dbo.Pumps AS Pumps_1 RIGHT OUTER JOIN
                      dbo.LoadsSchedule ON Pumps_1.Number = dbo.LoadsSchedule.ActualPumpNo LEFT OUTER JOIN
                      dbo.Pumps ON dbo.LoadsSchedule.PumpNo = dbo.Pumps.Number LEFT OUTER JOIN
                      dbo.Profile INNER JOIN
                      dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId INNER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.LoadsSchedule.LoadId = dbo.Loads.Id
ORDER BY dbo.LoadsSchedule.ScheduledDate, SSortOrder, CONVERT(int, dbo.LoadsSchedule.PumpNo), dbo.LoadsSchedule.ScheduledTime

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

