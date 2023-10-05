#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptWasteLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwRptWasteLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 5:20:13 PM Wednesday, January 13, 2010 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| RegistrationNo | varchar(50) | 50 |
| EpaIdNo | varchar(50) | 50 |
| SICCode | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| DocumentNumber | varchar(50) | 50 |
| DocumentType | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| WasteCode | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| HandlingCode | varchar(10) | 10 |
| Quantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptWasteLoads]
AS
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Generator.Name AS [Generator Name], dbo.Destination.Name AS Destination, dbo.Generator.RegistrationNo, 
                      dbo.Generator.EpaIdNo, dbo.Profile.SICCode, dbo.Loads.ScheduledDate, dbo.LabTest.DocumentNumber, dbo.LabTest.DocumentType, 
                      dbo.Profile.MaterialDescription, dbo.Profile.WasteCode, dbo.Profile.ProfileType, dbo.LabTest.HandlingCode, dbo.LabTest.Quantity, 
                      dbo.LabTest.Units
FROM         dbo.Generator INNER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId INNER JOIN
                      dbo.LabTest INNER JOIN
                      dbo.Loads INNER JOIN
                      dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id ON dbo.LabTest.Id = dbo.Loads.LabTestId ON 
                      dbo.Profile.Id = dbo.Loads.ProfileId
WHERE     (dbo.Profile.ProfileType = 'Waste') OR
                      (dbo.Profile.ProfileType = 'Recycled')
ORDER BY dbo.Generator.Name, dbo.Loads.ScheduledDate

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

