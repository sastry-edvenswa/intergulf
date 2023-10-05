#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadPadTimesForExport

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadPadTimesForExport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:47:32 AM Friday, September 29, 2017 |
| Last Modified | 2:47:32 AM Friday, September 29, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Name | varchar(100) | 100 |
| ScheduledDate | datetime | 8 |
| ProfileNumber | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| PadStartTime | decimal(18,2) | 9 |
| PadPumpStartTime | decimal(18,2) | 9 |
| PadPumpStopTime | decimal(18,2) | 9 |
| PadEndTime | decimal(18,2) | 9 |
| WashOutPerformed | varchar(50) | 50 |
| Expr1 | varchar(5) | 5 |
| PumpStartTime | varchar(5) | 5 |
| PumpStopTime | varchar(5) | 5 |
| PadStopTime | varchar(5) | 5 |
| LabCheckOutTime | varchar(5) | 5 |
| Status | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadPadTimesForExport]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Generator.Name, dbo.Loads.ScheduledDate, dbo.Profile.ProfileNumber, dbo.Loads.DispatchStatus, dbo.Loads.PadStartTime, 
                         dbo.Loads.PadPumpStartTime, dbo.Loads.PadPumpStopTime, dbo.Loads.PadEndTime, dbo.Loads.WashOutPerformed, dbo.LoadsSchedule.PadStartTime AS Expr1, 
                         dbo.LoadsSchedule.PumpStartTime, dbo.LoadsSchedule.PumpStopTime, dbo.LoadsSchedule.PadStopTime, dbo.LoadsSchedule.LabCheckOutTime, 
                         dbo.LoadsSchedule.Status, dbo.Loads.TankNumber
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.LoadsSchedule ON dbo.Loads.Id = dbo.LoadsSchedule.LoadId LEFT OUTER JOIN
                         dbo.Generator RIGHT OUTER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE        (dbo.Profile.ProfileNumber = '07023') AND (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2015-01-01 00:00:00', 102)) AND 
                         (dbo.Loads.DispatchStatus = 'Complete')
ORDER BY dbo.Loads.ScheduledDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

