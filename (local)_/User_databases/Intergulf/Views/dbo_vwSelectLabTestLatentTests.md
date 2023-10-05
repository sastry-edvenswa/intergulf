#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLabTestLatentTests

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLabTestLatentTests]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:52:48 PM Wednesday, September 17, 2014 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| LoadId | decimal(18,0) | 9 |
| TestDate | datetime | 8 |
| StartTime | datetime | 8 |
| LatentEmailSent | varchar(3) | 3 |
| LabCheckInDate | datetime | 8 |
| LabStartTime | decimal(18,2) | 9 |
| LabTestStartTime | decimal(18,2) | 9 |
| LabTestEndTime | decimal(18,2) | 9 |
| LabEndTime | decimal(18,2) | 9 |
| PadCheckInDate | datetime | 8 |
| PadStartTime | decimal(18,2) | 9 |
| PadPumpStartTime | decimal(18,2) | 9 |
| PadPumpStopTime | decimal(18,2) | 9 |
| PadEndTime | decimal(18,2) | 9 |
| Status | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLabTestLatentTests]
AS
SELECT     TOP 100 PERCENT dbo.LabTest.Id, dbo.LabTest.LoadId, dbo.LabTest.TestDate, dbo.LabTest.StartTime, dbo.LabTest.LatentEmailSent, 
                      dbo.Loads.LabCheckInDate, dbo.Loads.LabStartTime, dbo.Loads.LabTestStartTime, dbo.Loads.LabTestEndTime, dbo.Loads.LabEndTime, 
                      dbo.Loads.PadCheckInDate, dbo.Loads.PadStartTime, dbo.Loads.PadPumpStartTime, dbo.Loads.PadPumpStopTime, dbo.Loads.PadEndTime, 
                      dbo.LabTest.Status
FROM         dbo.LabTest LEFT OUTER JOIN
                      dbo.Loads ON dbo.LabTest.LoadId = dbo.Loads.Id
WHERE     (dbo.LabTest.LatentEmailSent IS NULL) AND (dbo.LabTest.TestDate > CONVERT(DATETIME, '2014-08-01 00:00:00', 102)) AND 
                      (dbo.LabTest.Status = 'Open')
ORDER BY dbo.LabTest.TestDate DESC

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

