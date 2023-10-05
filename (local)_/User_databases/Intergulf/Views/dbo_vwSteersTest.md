#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSteersTest

# ![Views](../../../../Images/View32.png) [dbo].[vwSteersTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 5:20:55 PM Thursday, September 20, 2018 |
| Last Modified | 5:38:47 PM Wednesday, September 26, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| WasteCode | varchar(50) | 50 |
| WCIdent | varchar(1) | 1 |
| DispatchStatus | varchar(50) | 50 |
| LabId | bigint | 8 |
| Status | varchar(50) | 50 |
| StatusDescription | varchar(2000) | 2000 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| Name | nvarchar(100) | 200 |
| Facility | varchar(50) | 50 |
| DocumentNumber | varchar(50) | 50 |
| Lab Doc Type | varchar(50) | 50 |
| Profile Doc Type | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSteersTest]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Profile.WasteCode, RIGHT(dbo.Profile.WasteCode, 1) AS WCIdent, dbo.Loads.DispatchStatus, dbo.LabTest.Id AS LabId, dbo.LabTest.Status, 
                         dbo.LabTest.StatusDescription, dbo.Profile.ProfileType, dbo.Profile.Direction, dbo.Destination.Name, dbo.Destination.Facility, dbo.LabTest.DocumentNumber, dbo.LabTest.DocumentType AS [Lab Doc Type], 
                         dbo.Profile.DocumentType AS [Profile Doc Type]
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                         dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE        (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2018-09-01 00:00:00', 102)) AND (dbo.Loads.ScheduledDate <= CONVERT(DATETIME, '2018-09-20 00:00:00', 102))
ORDER BY dbo.Loads.ScheduledDate, dbo.Loads.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

