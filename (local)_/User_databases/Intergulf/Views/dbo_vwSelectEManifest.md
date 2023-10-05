#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectEManifest

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectEManifest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:24:59 PM Saturday, July 24, 2021 |
| Last Modified | 8:44:59 PM Sunday, August 29, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Transporter Name | varchar(100) | 100 |
| Transporter Epa Number | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| ProfileId | bigint | 8 |
| MaterialCode | nvarchar(50) | 100 |
| PreProperShippingName | nvarchar(100) | 200 |
| ProperShippingName | nvarchar(300) | 600 |
| PostProperShippingName | nvarchar(100) | 200 |
| ProductPlacardNumber | nvarchar(50) | 100 |
| Hazmat | nvarchar(50) | 100 |
| ProductHazardClass | nvarchar(50) | 100 |
| ProductPackingGroup | nvarchar(50) | 100 |
| Number | varchar(50) | 50 |
| PackageType | varchar(50) | 50 |
| ShippingWeight | decimal(18,0) | 9 |
| Driver FName | varchar(50) | 50 |
| Driver LName | varchar(50) | 50 |
| IntergulfDescription | nvarchar(50) | 100 |
| EPAWasteCode1 | varchar(10) | 10 |
| EPAWasteCode2 | varchar(10) | 10 |
| EPAWasteCode3 | varchar(10) | 10 |
| EPAWasteCode4 | varchar(10) | 10 |
| ShippingName | varchar(1000) | 1000 |
| ProfileNumber | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| Destination Name | nvarchar(100) | 200 |
| Destination Address | nvarchar(50) | 100 |
| Destination City | nvarchar(50) | 100 |
| Destination State | nvarchar(50) | 100 |
| Destination Zip | nvarchar(50) | 100 |
| Destination Phone | nvarchar(50) | 100 |
| Destination Epa Number | nvarchar(50) | 100 |
| DispatcherFName | varchar(50) | 50 |
| DispatcherLName | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(3000) | 3000 |
| Generator City | varchar(50) | 50 |
| Generator State | varchar(50) | 50 |
| Generator Zip | varchar(50) | 50 |
| Generator Epa Number | varchar(50) | 50 |
| RegistrationNo | varchar(50) | 50 |
| Generator Phone | varchar(50) | 50 |
| UOM | varchar(1) | 1 |
| Code | varchar(50) | 50 |
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
| UNNumber | nvarchar(4) | 8 |
| GUIDE_PAGE | nvarchar(255) | 510 |
| Contact | varchar(50) | 50 |
| FunctionProperShippingName | varchar(5000) | 5000 |
| ProfileType | varchar(50) | 50 |
| Destination Number | nvarchar(50) | 100 |
| Transporter Number | varchar(50) | 50 |
| LabTestId | bigint | 8 |
| DocumentNumber | varchar(50) | 50 |
| ScheduledTime | datetime | 8 |
| Transporter Phone | varchar(50) | 50 |
| HandlingCode | varchar(10) | 10 |
| MaterialDescription | varchar(3000) | 3000 |
| Quantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectEManifest]
AS
SELECT DISTINCT 
                         dbo.Loads.Id, dbo.Transporter.Name AS [Transporter Name], dbo.Transporter.EpaIdNo AS [Transporter Epa Number], dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.TrailerId, dbo.Loads.TankNumber, 
                         dbo.Loads.DeliveryReleaseNumber, dbo.Loads.ProfileId, dbo.MaterialCode.MaterialCode, dbo.MaterialCode.PreProperShippingName, dbo.MaterialCode.ProperShippingName, 
                         dbo.MaterialCode.PostProperShippingName, dbo.MaterialCode.ProductPlacardNumber, dbo.MaterialCode.Hazmat, dbo.MaterialCode.ProductHazardClass, dbo.MaterialCode.ProductPackingGroup, 
                         dbo.Loads.Number, dbo.Loads.PackageType, dbo.Loads.ShippingWeight, dbo.Driver.FirstName AS [Driver FName], dbo.Driver.LastName AS [Driver LName], dbo.MaterialCode.Description AS IntergulfDescription, 
                         dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.Profile.ShippingName, dbo.Profile.ProfileNumber, dbo.Profile.WasteCode, 
                         dbo.Destination.Name AS [Destination Name], dbo.Destination.Address AS [Destination Address], dbo.Destination.City AS [Destination City], dbo.Destination.State AS [Destination State], 
                         dbo.Destination.Zip AS [Destination Zip], dbo.Destination.Phone AS [Destination Phone], dbo.Destination.EpaIdNo AS [Destination Epa Number], dbo.UserMaster.FirstName AS DispatcherFName, 
                         dbo.UserMaster.LastName AS DispatcherLName, dbo.Generator.Name AS [Generator Name], dbo.Generator.Address AS [Generator Address], dbo.Generator.City AS [Generator City], 
                         dbo.Generator.State AS [Generator State], dbo.Generator.Zip AS [Generator Zip], dbo.Generator.EpaIdNo AS [Generator Epa Number], dbo.Generator.RegistrationNo, dbo.Generator.Phone AS [Generator Phone], 
                         dbo.Profile.UOM, dbo.ContainerType.Code, dbo.ManifestMailingAddress.Name AS GMailingName, dbo.ManifestMailingAddress.Address AS GMailingAddress, dbo.ManifestMailingAddress.City AS GMailingCity, 
                         dbo.ManifestMailingAddress.State AS GMailingState, dbo.ManifestMailingAddress.Zip AS GMailingZip, dbo.ProfileManifestMailingAddress.Name AS PMailingName, 
                         dbo.ProfileManifestMailingAddress.Address AS PMailingAddress, dbo.ProfileManifestMailingAddress.City AS PMailingCity, dbo.ProfileManifestMailingAddress.State AS PMailingState, 
                         dbo.ProfileManifestMailingAddress.Zip AS PMailingZip, dbo.EmergencyContact.Name AS GContactName, dbo.EmergencyContact.Phone AS GContactPhone, dbo.ProfileEmergencyContact.Name AS PContactName, 
                         dbo.ProfileEmergencyContact.Phone AS PContactPhone, SUBSTRING(dbo.ProductHazardousMaterial.UNNumber, 3, 4) AS UNNumber, dbo.ProductERG.GUIDE_PAGE, dbo.Generator.Contact, 
                         dbo.fnProperShippingName(dbo.Profile.MaterialCodeId) AS FunctionProperShippingName, dbo.Profile.ProfileType, dbo.Destination.TceqNo AS [Destination Number], 
                         dbo.Transporter.TceqNo AS [Transporter Number], dbo.Loads.LabTestId, dbo.LabTest.DocumentNumber, dbo.Loads.ScheduledTime, dbo.Transporter.Phone AS [Transporter Phone], dbo.LabTest.HandlingCode, 
                         dbo.Profile.MaterialDescription, dbo.LabTest.Quantity, dbo.LabTest.Units
FROM            dbo.ProductERG RIGHT OUTER JOIN
                         dbo.ProductHazardousMaterial ON dbo.ProductERG.UN_NUMBER = SUBSTRING(dbo.ProductHazardousMaterial.UNNumber, 3, 4) RIGHT OUTER JOIN
                         dbo.MaterialCode ON dbo.ProductHazardousMaterial.ID = dbo.MaterialCode.ProperShippingNameId RIGHT OUTER JOIN
                         dbo.Profile LEFT OUTER JOIN
                         dbo.ManifestMailingAddress RIGHT OUTER JOIN
                         dbo.Generator LEFT OUTER JOIN
                         dbo.EmergencyContact ON dbo.Generator.Id = dbo.EmergencyContact.Id ON dbo.ManifestMailingAddress.Id = dbo.Generator.Id ON dbo.Profile.GeneratorId = dbo.Generator.Id ON 
                         dbo.MaterialCode.ID = dbo.Profile.MaterialCodeId RIGHT OUTER JOIN
                         dbo.UserMaster RIGHT OUTER JOIN
                         dbo.ContainerType RIGHT OUTER JOIN
                         dbo.ProfileManifestMailingAddress RIGHT OUTER JOIN
                         dbo.ProfileEmergencyContact RIGHT OUTER JOIN
                         dbo.Loads LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id ON dbo.ProfileEmergencyContact.Id = dbo.Loads.ProfileId ON dbo.ProfileManifestMailingAddress.Id = dbo.Loads.ProfileId ON 
                         dbo.ContainerType.Id = dbo.Loads.ContainerTypeId ON dbo.UserMaster.UserName = dbo.Loads.UpdateUser LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id ON dbo.Profile.Id = dbo.Loads.ProfileId LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Loads.TransporterId = dbo.Transporter.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ContainerType]](../Tables/dbo_ContainerType.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[EmergencyContact]](../Tables/dbo_EmergencyContact.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[ManifestMailingAddress]](../Tables/dbo_ManifestMailingAddress.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[ProductERG]](../Tables/dbo_ProductERG.md)
* [[dbo].[ProductHazardousMaterial]](../Tables/dbo_ProductHazardousMaterial.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ProfileEmergencyContact]](../Tables/dbo_ProfileEmergencyContact.md)
* [[dbo].[ProfileManifestMailingAddress]](../Tables/dbo_ProfileManifestMailingAddress.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[fnProperShippingName]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProperShippingName.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

