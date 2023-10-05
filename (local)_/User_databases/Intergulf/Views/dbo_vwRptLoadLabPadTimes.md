#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadLabPadTimes

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadLabPadTimes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:56:21 PM Tuesday, April 20, 2010 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Name | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ProfileType | varchar(50) | 50 |
| LabCheckInDate | datetime | 8 |
| LabStartTime | decimal(18,2) | 9 |
| LabTestStartTime | decimal(18,2) | 9 |
| LabTestEndTime | decimal(18,2) | 9 |
| LabEndTime | decimal(18,2) | 9 |
| PadStartTime | decimal(18,2) | 9 |
| PadPumpStartTime | decimal(18,2) | 9 |
| PadPumpStopTime | decimal(18,2) | 9 |
| PadEndTime | decimal(18,2) | 9 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLoadLabPadTimes]
AS
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Generator.Name, dbo.Profile.ProfileNumber, dbo.Profile.MaterialDescription, dbo.Profile.ProfileType, 
                      dbo.Loads.LabCheckInDate, dbo.Loads.LabStartTime, dbo.Loads.LabTestStartTime, dbo.Loads.LabTestEndTime, dbo.Loads.LabEndTime, 
                      dbo.Loads.PadStartTime, dbo.Loads.PadPumpStartTime, dbo.Loads.PadPumpStopTime, dbo.Loads.PadEndTime, dbo.Loads.ScheduledDate, 
                      dbo.Loads.ScheduledTime
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id RIGHT OUTER JOIN
                      dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId
WHERE     (dbo.Loads.LabTestStartTime IS NOT NULL) OR
                      (dbo.Loads.LabStartTime IS NOT NULL) OR
                      (dbo.Loads.LabTestEndTime IS NOT NULL) OR
                      (dbo.Loads.PadStartTime IS NOT NULL) OR
                      (dbo.Loads.PadEndTime IS NOT NULL) OR
                      (dbo.Loads.PadPumpStopTime IS NOT NULL) OR
                      (dbo.Loads.PadPumpStartTime IS NOT NULL)

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

