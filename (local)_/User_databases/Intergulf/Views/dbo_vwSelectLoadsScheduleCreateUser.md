#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsScheduleCreateUser

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsScheduleCreateUser]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 5:06:28 PM Tuesday, July 25, 2017 |
| Last Modified | 5:06:28 PM Tuesday, July 25, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadId | bigint | 8 |
| ScheduledDate | date | 3 |
| ScheduledTime | varchar(5) | 5 |
| ScheduledTimeUnits | int | 4 |
| Status | varchar(50) | 50 |
| OverRideStatus | varchar(50) | 50 |
| CreateUser | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |
| ScheduledStartDateTime | datetime | 8 |
| ScheduledEndDateTime | datetime | 8 |
| ActualPumpNo | varchar(50) | 50 |
| CompleteDate | date | 3 |
| CompleteTime | varchar(5) | 5 |
| Load Create Date | datetime | 8 |
| Load Create User | varchar(50) | 50 |
| CustomerPickupDelivery | varchar(3) | 3 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsScheduleCreateUser]
AS
SELECT        TOP (100) PERCENT dbo.LoadsSchedule.LoadId, dbo.LoadsSchedule.ScheduledDate, dbo.LoadsSchedule.ScheduledTime, dbo.LoadsSchedule.ScheduledTimeUnits, dbo.LoadsSchedule.Status, 
                         dbo.LoadsSchedule.OverRideStatus, dbo.LoadsSchedule.CreateUser, dbo.LoadsSchedule.CreateDateTime, dbo.LoadsSchedule.UpdateUser, dbo.LoadsSchedule.UpdateDateTime, 
                         dbo.LoadsSchedule.ScheduledStartDateTime, dbo.LoadsSchedule.ScheduledEndDateTime, dbo.LoadsSchedule.ActualPumpNo, dbo.LoadsSchedule.CompleteDate, dbo.LoadsSchedule.CompleteTime, 
                         dbo.Loads.UpdateDateTime AS [Load Create Date], dbo.Loads.UpdateUser AS [Load Create User], dbo.LoadRequest.CustomerPickupDelivery
FROM            dbo.LoadRequest INNER JOIN
                         dbo.Loads ON dbo.LoadRequest.Id = dbo.Loads.LoadRequestId RIGHT OUTER JOIN
                         dbo.LoadsSchedule ON dbo.Loads.Id = dbo.LoadsSchedule.LoadId
WHERE        (dbo.LoadsSchedule.LoadId = 244179) OR
                         (dbo.LoadsSchedule.LoadId = 244262) OR
                         (dbo.LoadsSchedule.LoadId = 244187) OR
                         (dbo.LoadsSchedule.LoadId = 244290) OR
                         (dbo.LoadsSchedule.LoadId = 244003) OR
                         (dbo.LoadsSchedule.LoadId = 244149) OR
                         (dbo.LoadsSchedule.LoadId = 244152) OR
                         (dbo.LoadsSchedule.LoadId = 244215) OR
                         (dbo.LoadsSchedule.LoadId = 244115) OR
                         (dbo.LoadsSchedule.LoadId = 244156)
ORDER BY dbo.LoadsSchedule.CreateDateTime, dbo.LoadsSchedule.CreateUser
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

