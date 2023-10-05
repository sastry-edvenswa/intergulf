#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProfileTCEQ

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProfileTCEQ]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 1:03:13 PM Tuesday, October 5, 2021 |
| Last Modified | 4:09:08 PM Tuesday, November 16, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ProfileId | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(3000) | 3000 |
| Generator City | varchar(50) | 50 |
| Generator State | varchar(50) | 50 |
| Generator Zip | varchar(50) | 50 |
| Generator Phone | varchar(50) | 50 |
| Generator Epa Number | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
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
| GContactName | varchar(50) | 50 |
| GContactPhone | varchar(50) | 50 |
| PContactName | varchar(50) | 50 |
| PContactPhone | varchar(50) | 50 |
| Transporter Name | varchar(100) | 100 |
| Transporter Epa Number | varchar(50) | 50 |
| Destination Name | nvarchar(100) | 200 |
| Destination Address | nvarchar(50) | 100 |
| Destination City | nvarchar(50) | 100 |
| Destination State | nvarchar(50) | 100 |
| Destination Zip | nvarchar(50) | 100 |
| Destination Phone | nvarchar(50) | 100 |
| Destination Epa Number | nvarchar(50) | 100 |
| FunctionProperShippingName | varchar(5000) | 5000 |
| MaterialCode | nvarchar(50) | 100 |
| Description | nvarchar(50) | 100 |
| PreProperShippingName | nvarchar(100) | 200 |
| ProperShippingName | nvarchar(300) | 600 |
| PostProperShippingName | nvarchar(100) | 200 |
| Hazmat | nvarchar(50) | 100 |
| ProductPackingGroup | nvarchar(50) | 100 |
| ProductHazardClass | nvarchar(50) | 100 |
| ProductPlacardNumber | nvarchar(50) | 100 |
| ShippingName | varchar(1000) | 1000 |
| UOM | varchar(1) | 1 |
| EPAWasteCode1 | varchar(10) | 10 |
| EPAWasteCode2 | varchar(10) | 10 |
| EPAWasteCode3 | varchar(10) | 10 |
| EPAWasteCode4 | varchar(10) | 10 |
| Contact | varchar(50) | 50 |
| RegistrationNo | varchar(50) | 50 |
| Destination Number | nvarchar(50) | 100 |
| Transporter Number | varchar(50) | 50 |
| UNNumber | nvarchar(4) | 8 |
| GUIDE_PAGE | nvarchar(255) | 510 |
| WasteCode | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptProfileTCEQ]
AS
SELECT        dbo.Profile.Id AS ProfileId, dbo.Generator.Name AS [Generator Name], dbo.Generator.Address AS [Generator Address], dbo.Generator.City AS [Generator City], dbo.Generator.State AS [Generator State], 
                         dbo.Generator.Zip AS [Generator Zip], dbo.Generator.Phone AS [Generator Phone], dbo.Generator.EpaIdNo AS [Generator Epa Number], dbo.Profile.ProfileType, dbo.Profile.ProfileNumber, 
                         dbo.ManifestMailingAddress.Name AS GMailingName, dbo.ManifestMailingAddress.Address AS GMailingAddress, dbo.ManifestMailingAddress.City AS GMailingCity, 
                         dbo.ManifestMailingAddress.State AS GMailingState, dbo.ManifestMailingAddress.Zip AS GMailingZip, dbo.ProfileManifestMailingAddress.Name AS PMailingName, 
                         dbo.ProfileManifestMailingAddress.Address AS PMailingAddress, dbo.ProfileManifestMailingAddress.City AS PMailingCity, dbo.ProfileManifestMailingAddress.State AS PMailingState, 
                         dbo.ProfileManifestMailingAddress.Zip AS PMailingZip, dbo.EmergencyContact.Name AS GContactName, dbo.EmergencyContact.Phone AS GContactPhone, dbo.ProfileEmergencyContact.Name AS PContactName, 
                         dbo.ProfileEmergencyContact.Phone AS PContactPhone, dbo.Transporter.Name AS [Transporter Name], dbo.Transporter.EpaIdNo AS [Transporter Epa Number], dbo.Destination.Name AS [Destination Name], 
                         dbo.Destination.Address AS [Destination Address], dbo.Destination.City AS [Destination City], dbo.Destination.State AS [Destination State], dbo.Destination.Zip AS [Destination Zip], 
                         dbo.Destination.Phone AS [Destination Phone], dbo.Destination.EpaIdNo AS [Destination Epa Number], dbo.fnProperShippingName(dbo.Profile.MaterialCodeId) AS FunctionProperShippingName, 
                         dbo.MaterialCode.MaterialCode, dbo.MaterialCode.Description, dbo.MaterialCode.PreProperShippingName, dbo.MaterialCode.ProperShippingName, dbo.MaterialCode.PostProperShippingName, 
                         dbo.MaterialCode.Hazmat, dbo.MaterialCode.ProductPackingGroup, dbo.MaterialCode.ProductHazardClass, dbo.MaterialCode.ProductPlacardNumber, dbo.Profile.ShippingName, dbo.Profile.UOM, 
                         dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.Generator.Contact, dbo.Generator.RegistrationNo, 
                         dbo.Destination.TceqNo AS [Destination Number], dbo.Transporter.TceqNo AS [Transporter Number], SUBSTRING(dbo.ProductHazardousMaterial.UNNumber, 3, 4) AS UNNumber, dbo.ProductERG.GUIDE_PAGE, 
                         dbo.Profile.WasteCode
FROM            dbo.Destination RIGHT OUTER JOIN
                         dbo.Profile LEFT OUTER JOIN
                         dbo.MaterialCode LEFT OUTER JOIN
                         dbo.ProductHazardousMaterial LEFT OUTER JOIN
                         dbo.ProductERG ON SUBSTRING(dbo.ProductHazardousMaterial.UNNumber, 3, 4) = dbo.ProductERG.UN_NUMBER ON dbo.MaterialCode.ProperShippingNameId = dbo.ProductHazardousMaterial.ID ON 
                         dbo.Profile.MaterialCodeId = dbo.MaterialCode.ID ON dbo.Destination.Id = dbo.Profile.DestinationId LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Profile.TransporterId = dbo.Transporter.Id LEFT OUTER JOIN
                         dbo.EmergencyContact ON dbo.Profile.GeneratorId = dbo.EmergencyContact.Id LEFT OUTER JOIN
                         dbo.ProfileEmergencyContact ON dbo.Profile.Id = dbo.ProfileEmergencyContact.Id LEFT OUTER JOIN
                         dbo.ProfileManifestMailingAddress ON dbo.Profile.Id = dbo.ProfileManifestMailingAddress.Id LEFT OUTER JOIN
                         dbo.ManifestMailingAddress ON dbo.Profile.GeneratorId = dbo.ManifestMailingAddress.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
WHERE        (dbo.Profile.Status = 'Active')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
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

