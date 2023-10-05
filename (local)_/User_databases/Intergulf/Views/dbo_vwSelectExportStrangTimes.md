#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportStrangTimes

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportStrangTimes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:27:23 PM Tuesday, March 12, 2019 |
| Last Modified | 2:27:23 PM Tuesday, March 12, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Name | varchar(100) | 100 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| Destination | nvarchar(100) | 200 |
| Location | varchar(50) | 50 |
| LabStartTime | decimal(18,2) | 9 |
| LabEndTime | decimal(18,2) | 9 |
| PadStartTime | decimal(18,2) | 9 |
| PadEndTime | decimal(18,2) | 9 |
| Direction | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| Lab Notes | varchar(5000) | 5000 |
| Pad Notes | varchar(3000) | 3000 |
| Load Notes | varchar(6000) | 6000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportStrangTimes]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Generator.Name, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Destination.Name AS Destination, dbo.LabTest.Location, dbo.Loads.LabStartTime, 
                         dbo.Loads.LabEndTime, dbo.Loads.PadStartTime, dbo.Loads.PadEndTime, dbo.Profile.Direction, dbo.Loads.DispatchStatus, dbo.LabTest.Notes AS [Lab Notes], dbo.Loads.PadNotes AS [Pad Notes], 
                         dbo.Loads.Notes AS [Load Notes]
FROM            dbo.Destination RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                         dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id
WHERE        (dbo.LabTest.Location = 'Strang Lab')
ORDER BY dbo.Loads.ScheduledDate
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

