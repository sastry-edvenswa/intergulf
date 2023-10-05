#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectMonthlyDischarge

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectMonthlyDischarge]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:27:07 PM Tuesday, October 16, 2018 |
| Last Modified | 4:27:07 PM Tuesday, October 16, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ScheduledDate | datetime | 8 |
| ProfileNumber | varchar(50) | 50 |
| CustomerName | varchar(50) | 50 |
| GeneratorName | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| Facility | varchar(50) | 50 |
| SICCode | varchar(50) | 50 |
| EpaIdNo | varchar(50) | 50 |
| StateId | varchar(50) | 50 |
| TransporterName | varchar(50) | 50 |
| TransporterId | varchar(50) | 50 |
| OrganicWaste | varchar(5) | 5 |
| OilyWaste | varchar(5) | 5 |
| OtherWaste | varchar(5) | 5 |
| WasteName | varchar(5000) | 5000 |
| MaterialDescription | varchar(3000) | 3000 |
| TCEQWasteCode | varchar(50) | 50 |
| TreatmentDescription | varchar(10) | 10 |
| IndustrialCategory | varchar(20) | 20 |
| GCApprovalDate | datetime | 8 |
| EPAWasteCodes | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectMonthlyDischarge]
AS
SELECT        TOP (100) PERCENT dbo.Loads.ScheduledDate, dbo.Profile.ProfileNumber, dbo.Customer.Name AS CustomerName, dbo.Generator.Name AS GeneratorName, 
                         dbo.Destination.Name AS Destination, dbo.Destination.Facility, dbo.Profile.SICCode, dbo.Generator.EpaIdNo, dbo.Generator.RegistrationNo AS StateId, 
                         dbo.Transporter.Name AS TransporterName, dbo.Transporter.TceqNo AS TransporterId, dbo.fnProfileMaterialClassificationOrganic(dbo.Profile.MaterialClassification) 
                         AS OrganicWaste, dbo.fnProfileMaterialClassificationOily(dbo.Profile.MaterialClassification) AS OilyWaste, 
                         dbo.fnProfileMaterialClassificationOther(dbo.Profile.MaterialClassification) AS OtherWaste, 
                         dbo.fnProfileMaterialClassificationDescription(dbo.Profile.MaterialClassification) AS WasteName, dbo.Profile.MaterialDescription, 
                         dbo.Profile.WasteCode AS TCEQWasteCode, dbo.LabTest.HandlingCode AS TreatmentDescription, dbo.Profile.IndustrialCategory, dbo.Profile.GCApprovalDate, 
                         dbo.fnProfileEPAWasteCodes(dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4) 
                         AS EPAWasteCodes
FROM            dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId INNER JOIN
                         dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId INNER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id INNER JOIN
                         dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id INNER JOIN
                         dbo.Transporter ON dbo.Loads.TransporterId = dbo.Transporter.Id LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id
ORDER BY GeneratorName, dbo.Profile.ProfileNumber

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[fnProfileEPAWasteCodes]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProfileEPAWasteCodes.md)
* [[dbo].[fnProfileMaterialClassificationDescription]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProfileMaterialClassificationDescription.md)
* [[dbo].[fnProfileMaterialClassificationOily]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProfileMaterialClassificationOily.md)
* [[dbo].[fnProfileMaterialClassificationOrganic]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProfileMaterialClassificationOrganic.md)
* [[dbo].[fnProfileMaterialClassificationOther]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProfileMaterialClassificationOther.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

