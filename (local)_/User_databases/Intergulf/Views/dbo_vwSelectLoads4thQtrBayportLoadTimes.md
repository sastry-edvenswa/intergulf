#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoads4thQtrBayportLoadTimes

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoads4thQtrBayportLoadTimes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:34:21 PM Monday, February 26, 2018 |
| Last Modified | 9:34:21 PM Monday, February 26, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Name | varchar(100) | 100 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| Location | varchar(50) | 50 |
| LabStartTime | decimal(18,2) | 9 |
| PadEndTime | decimal(18,2) | 9 |
| LoadTime | real | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoads4thQtrBayportLoadTimes]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Generator.Name, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.LabTest.Location, dbo.Loads.LabStartTime, 
                         dbo.Loads.PadEndTime, dbo.fnLoadTime(dbo.Loads.LabStartTime, dbo.Loads.PadEndTime) AS LoadTime
FROM            dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id
WHERE        (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2017-10-01 00:00:00', 102)) AND (dbo.Loads.ScheduledDate <= CONVERT(DATETIME, '2017-12-31 00:00:00', 
                         102)) AND (dbo.LabTest.Location = 'BayPort Lab')
ORDER BY dbo.Loads.ScheduledDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[fnLoadTime]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnLoadTime.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

