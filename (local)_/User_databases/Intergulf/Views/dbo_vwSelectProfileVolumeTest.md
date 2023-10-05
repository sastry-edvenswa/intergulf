#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileVolumeTest

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileVolumeTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:17:53 PM Friday, January 6, 2023 |
| Last Modified | 10:17:53 PM Friday, January 6, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Generator | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| TotalQty | decimal(15,2) | 9 |
| Address | varchar(3000) | 3000 |
| City | varchar(50) | 50 |
| Zip | varchar(50) | 50 |
| CompanyProfileNumber | varchar(100) | 100 |
| SICCode | varchar(50) | 50 |
| Phone | varchar(50) | 50 |
| MaterialClassification | varchar(200) | 200 |
| PetroleumPcnt | varchar(50) | 50 |
| PetroleumPhase | varchar(300) | 300 |
| AqueousPcnt | varchar(50) | 50 |
| AqueousPhase | varchar(300) | 300 |
| SolidsPcnt | varchar(50) | 50 |
| SolidsPhase | varchar(300) | 300 |
| MaterialDescription | varchar(3000) | 3000 |
| ProcessDescription | varchar(3000) | 3000 |
| CreateDate | datetime | 8 |
| DocumentType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| Facility | varchar(50) | 50 |
| EPAWasteCode1 | varchar(10) | 10 |
| EPAWasteCode2 | varchar(10) | 10 |
| EPAWasteCode3 | varchar(10) | 10 |
| EPAWasteCode4 | varchar(10) | 10 |
| RegistrationNo | varchar(50) | 50 |
| EpaIdNo | varchar(50) | 50 |
| DestinationId | bigint | 8 |
| ScheduledDate | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfileVolumeTest]
AS
SELECT        dbo.Generator.Name AS Generator, dbo.Profile.ProfileNumber, dbo.Profile.ProfileType, dbo.fnSelectProfileVolume(dbo.Profile.Id, CONVERT(DATETIME, 01 / 01 / 23, 102), CONVERT(DATETIME, 01 / 06 / 23, 102)) 
                         AS TotalQty, dbo.Generator.Address, dbo.Generator.City, dbo.Generator.Zip, dbo.Profile.CompanyProfileNumber, dbo.Profile.SICCode, dbo.Generator.Phone, dbo.Profile.MaterialClassification, 
                         dbo.ProfileConstituents.PetroleumPcnt, dbo.ProfileConstituents.PetroleumPhase, dbo.ProfileConstituents.AqueousPcnt, dbo.ProfileConstituents.AqueousPhase, dbo.ProfileConstituents.SolidsPcnt, 
                         dbo.ProfileConstituents.SolidsPhase, dbo.Profile.MaterialDescription, dbo.Profile.ProcessDescription, dbo.Profile.CreateDate, dbo.Profile.DocumentType, dbo.Profile.Direction, dbo.Destination.Facility, 
                         dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.Generator.RegistrationNo, dbo.Generator.EpaIdNo, dbo.Profile.DestinationId, 
                         dbo.Loads.ScheduledDate
FROM            dbo.Destination RIGHT OUTER JOIN
                         dbo.Profile ON dbo.Destination.Id = dbo.Profile.DestinationId LEFT OUTER JOIN
                         dbo.LabTest LEFT OUTER JOIN
                         dbo.Loads ON dbo.LabTest.LoadId = dbo.Loads.Id ON dbo.Profile.Id = dbo.LabTest.ProfileId LEFT OUTER JOIN
                         dbo.ProfileConstituents ON dbo.Profile.Id = dbo.ProfileConstituents.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
GROUP BY dbo.Generator.Name, dbo.Profile.ProfileNumber, dbo.Generator.Address, dbo.Generator.City, dbo.Generator.Zip, dbo.Profile.MaterialDescription, dbo.Profile.ProcessDescription, dbo.Profile.SICCode, 
                         dbo.Generator.Phone, dbo.Profile.ProfileType, dbo.Profile.CompanyProfileNumber, dbo.Profile.MaterialClassification, dbo.ProfileConstituents.PetroleumPcnt, dbo.ProfileConstituents.PetroleumPhase, 
                         dbo.ProfileConstituents.AqueousPcnt, dbo.ProfileConstituents.AqueousPhase, dbo.ProfileConstituents.SolidsPcnt, dbo.ProfileConstituents.SolidsPhase, dbo.Profile.CreateDate, dbo.Profile.DocumentType, 
                         dbo.Destination.Facility, dbo.Profile.Direction, dbo.Profile.Id, dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.Generator.RegistrationNo, 
                         dbo.Generator.EpaIdNo, dbo.Profile.DestinationId, dbo.Loads.ScheduledDate
HAVING        (dbo.Profile.Direction = 'In Bound')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ProfileConstituents]](../Tables/dbo_ProfileConstituents.md)
* [[dbo].[fnSelectProfileVolume]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSelectProfileVolume.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

