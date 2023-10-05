#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProfileManifest

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProfileManifest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:53:16 PM Wednesday, October 13, 2021 |
| Last Modified | 4:09:42 PM Tuesday, November 16, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProfileNumber | varchar(50) | 50 |
| Transporter Name | varchar(100) | 100 |
| Transporter Phone | varchar(50) | 50 |
| Transporter Epa Number | varchar(50) | 50 |
| Transporter Tceq Number | varchar(50) | 50 |
| DotNo | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| PreProperShippingName | nvarchar(100) | 200 |
| ProperShippingName | nvarchar(300) | 600 |
| PostProperShippingName | nvarchar(100) | 200 |
| ProductPlacardNumber | nvarchar(50) | 100 |
| Hazmat | nvarchar(50) | 100 |
| ProductHazardClass | nvarchar(50) | 100 |
| ProductPackingGroup | nvarchar(50) | 100 |
| IntergulfDescription | nvarchar(50) | 100 |
| ShippingName | varchar(1000) | 1000 |
| GMailingName | varchar(100) | 100 |
| GMailingAddress | varchar(3000) | 3000 |
| GMailingCity | varchar(50) | 50 |
| GMailingState | varchar(50) | 50 |
| GMailingZip | varchar(50) | 50 |
| PMailingName | varchar(100) | 100 |
| PMailingAddress | varchar(3000) | 3000 |
| PMailingCity | varchar(50) | 50 |
| PMailingState | varchar(50) | 50 |
| PMailingZip | varchar(50) | 50 |
| PContactName | varchar(50) | 50 |
| PContactPhone | varchar(50) | 50 |
| FunctionProperShippingName | varchar(5000) | 5000 |
| MaterialCode | nvarchar(50) | 100 |
| GContactName | varchar(50) | 50 |
| GContactPhone | varchar(50) | 50 |
| ContactPhone | varchar(50) | 50 |
| Driver FName | varchar(12) | 12 |
| Driver LName | varchar(12) | 12 |
| ContactName | varchar(50) | 50 |
| GUIDE_PAGE | nvarchar(255) | 510 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptProfileManifest]
AS
SELECT        dbo.Profile.Id, dbo.Profile.ProfileNumber, dbo.Transporter.Name AS [Transporter Name], dbo.Transporter.Phone AS [Transporter Phone], dbo.Transporter.EpaIdNo AS [Transporter Epa Number], 
                         dbo.Transporter.TceqNo AS [Transporter Tceq Number], dbo.Transporter.DotNo, dbo.Generator.Name AS [Generator Name], MaterialCode.PreProperShippingName, MaterialCode.ProperShippingName, 
                         MaterialCode.PostProperShippingName, MaterialCode.ProductPlacardNumber, MaterialCode.Hazmat, MaterialCode.ProductHazardClass, MaterialCode.ProductPackingGroup, 
                         MaterialCode.Description AS IntergulfDescription, dbo.Profile.ShippingName, dbo.ManifestMailingAddress.Name AS GMailingName, dbo.ManifestMailingAddress.Address AS GMailingAddress, 
                         dbo.ManifestMailingAddress.City AS GMailingCity, dbo.ManifestMailingAddress.State AS GMailingState, dbo.ManifestMailingAddress.Zip AS GMailingZip, 
                         dbo.ProfileManifestMailingAddress.Name AS PMailingName, dbo.ProfileManifestMailingAddress.Address AS PMailingAddress, dbo.ProfileManifestMailingAddress.City AS PMailingCity, 
                         dbo.ProfileManifestMailingAddress.State AS PMailingState, dbo.ProfileManifestMailingAddress.Zip AS PMailingZip, dbo.ProfileEmergencyContact.Name AS PContactName, 
                         dbo.ProfileEmergencyContact.Phone AS PContactPhone, dbo.fnProperShippingName(dbo.Profile.MaterialCodeId) AS FunctionProperShippingName, MaterialCode.MaterialCode, 
                         dbo.EmergencyContact.Name AS GContactName, dbo.EmergencyContact.Phone AS GContactPhone, dbo.Profile.ContactPhone, 'Driver FName' AS [Driver FName], 'Driver LName' AS [Driver LName], 
                         dbo.Profile.ContactName, dbo.ProductERG.GUIDE_PAGE
FROM            dbo.ProductERG RIGHT OUTER JOIN
                         dbo.Transporter RIGHT OUTER JOIN
                         dbo.ProductHazardousMaterial RIGHT OUTER JOIN
                         dbo.MaterialCode AS MaterialCode ON dbo.ProductHazardousMaterial.ID = MaterialCode.ProperShippingNameId RIGHT OUTER JOIN
                         dbo.ProfileManifestMailingAddress RIGHT OUTER JOIN
                         dbo.Profile ON dbo.ProfileManifestMailingAddress.Id = dbo.Profile.Id LEFT OUTER JOIN
                         dbo.EmergencyContact ON dbo.Profile.Id = dbo.EmergencyContact.Id LEFT OUTER JOIN
                         dbo.ProfileEmergencyContact ON dbo.Profile.Id = dbo.ProfileEmergencyContact.Id ON MaterialCode.ID = dbo.Profile.MaterialCodeId LEFT OUTER JOIN
                         dbo.ManifestMailingAddress RIGHT OUTER JOIN
                         dbo.Generator ON dbo.ManifestMailingAddress.Id = dbo.Generator.Id ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Transporter.Id = dbo.Profile.TransporterId ON 
                         dbo.ProductERG.UN_NUMBER = SUBSTRING(dbo.ProductHazardousMaterial.UNNumber, 3, 4)
WHERE        (dbo.Profile.Status = 'Active')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[EmergencyContact]](../Tables/dbo_EmergencyContact.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[ManifestMailingAddress]](../Tables/dbo_ManifestMailingAddress.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[ProductERG]](../Tables/dbo_ProductERG.md)
* [[dbo].[ProductHazardousMaterial]](../Tables/dbo_ProductHazardousMaterial.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ProfileEmergencyContact]](../Tables/dbo_ProfileEmergencyContact.md)
* [[dbo].[ProfileManifestMailingAddress]](../Tables/dbo_ProfileManifestMailingAddress.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[fnProperShippingName]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProperShippingName.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

