#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadManifest

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadManifest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:12:06 PM Monday, December 17, 2012 |
| Last Modified | 4:16:03 PM Tuesday, February 22, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Transporter Name | varchar(100) | 100 |
| Transporter Epa Number | varchar(50) | 50 |
| Transporter Tceq Number | varchar(50) | 50 |
| Transporter Contact | varchar(50) | 50 |
| Transporter Phone | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| ProfileId | bigint | 8 |
| PickupLocation | varchar(200) | 200 |
| ContactName | varchar(100) | 100 |
| ContactPhone | varchar(50) | 50 |
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
| ContainerType | varchar(50) | 50 |
| IntergulfDescription | nvarchar(50) | 100 |
| ShippingName | varchar(1000) | 1000 |
| ProfileNumber | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| DispatcherFName | varchar(50) | 50 |
| DispatcherLName | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| DotNo | varchar(50) | 50 |
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
| FunctionProperShippingName | varchar(5000) | 5000 |
| GUIDE_PAGE | nvarchar(255) | 510 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLoadManifest]
AS
SELECT DISTINCT 
                         dbo.Loads.Id, dbo.Transporter.Name AS [Transporter Name], dbo.Transporter.EpaIdNo AS [Transporter Epa Number], dbo.Transporter.TceqNo AS [Transporter Tceq Number], 
                         dbo.Transporter.Contact AS [Transporter Contact], dbo.Transporter.Phone AS [Transporter Phone], dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.TrailerId, dbo.Loads.TankNumber, 
                         dbo.Loads.DeliveryReleaseNumber, dbo.Loads.ProfileId, dbo.Loads.PickupLocation, dbo.Loads.ContactName, dbo.Loads.ContactPhone, dbo.MaterialCode.MaterialCode, 
                         dbo.MaterialCode.PreProperShippingName, dbo.MaterialCode.ProperShippingName, dbo.MaterialCode.PostProperShippingName, dbo.MaterialCode.ProductPlacardNumber, dbo.MaterialCode.Hazmat, 
                         dbo.MaterialCode.ProductHazardClass, dbo.MaterialCode.ProductPackingGroup, dbo.Loads.Number, dbo.Loads.PackageType, dbo.Loads.ShippingWeight, dbo.Driver.FirstName AS [Driver FName], 
                         dbo.Driver.LastName AS [Driver LName], dbo.ContainerType.Code AS ContainerType, dbo.MaterialCode.Description AS IntergulfDescription, dbo.Profile.ShippingName, dbo.Profile.ProfileNumber, 
                         dbo.Profile.WasteCode, dbo.UserMaster.FirstName AS DispatcherFName, dbo.UserMaster.LastName AS DispatcherLName, dbo.Generator.Name AS [Generator Name], dbo.Transporter.DotNo, 
                         dbo.ManifestMailingAddress.Name AS GMailingName, dbo.ManifestMailingAddress.Address AS GMailingAddress, dbo.ManifestMailingAddress.City AS GMailingCity, 
                         dbo.ManifestMailingAddress.State AS GMailingState, dbo.ManifestMailingAddress.Zip AS GMailingZip, dbo.ProfileManifestMailingAddress.Name AS PMailingName, 
                         dbo.ProfileManifestMailingAddress.Address AS PMailingAddress, dbo.ProfileManifestMailingAddress.City AS PMailingCity, dbo.ProfileManifestMailingAddress.State AS PMailingState, 
                         dbo.ProfileManifestMailingAddress.Zip AS PMailingZip, dbo.EmergencyContact.Name AS GContactName, dbo.EmergencyContact.Phone AS GContactPhone, dbo.ProfileEmergencyContact.Name AS PContactName, 
                         dbo.ProfileEmergencyContact.Phone AS PContactPhone, dbo.fnProperShippingName(dbo.Profile.MaterialCodeId) AS FunctionProperShippingName, dbo.ProductERG.GUIDE_PAGE
FROM            dbo.ProductERG RIGHT OUTER JOIN
                         dbo.ProductHazardousMaterial RIGHT OUTER JOIN
                         dbo.MaterialCode ON dbo.ProductHazardousMaterial.ID = dbo.MaterialCode.ProperShippingNameId ON dbo.ProductERG.UN_NUMBER = SUBSTRING(dbo.ProductHazardousMaterial.UNNumber, 3, 4) 
                         RIGHT OUTER JOIN
                         dbo.EmergencyContact RIGHT OUTER JOIN
                         dbo.Transporter RIGHT OUTER JOIN
                         dbo.ContainerType RIGHT OUTER JOIN
                         dbo.Driver RIGHT OUTER JOIN
                         dbo.UserMaster RIGHT OUTER JOIN
                         dbo.Loads ON dbo.UserMaster.UserName = dbo.Loads.UpdateUser LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id ON dbo.Driver.Id = dbo.Loads.DriverId ON dbo.ContainerType.Id = dbo.Loads.ContainerTypeId LEFT OUTER JOIN
                         dbo.Profile LEFT OUTER JOIN
                         dbo.Generator LEFT OUTER JOIN
                         dbo.ManifestMailingAddress ON dbo.Generator.Id = dbo.ManifestMailingAddress.Id ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id ON 
                         dbo.Transporter.Id = dbo.Loads.TransporterId ON dbo.EmergencyContact.Id = dbo.Generator.Id LEFT OUTER JOIN
                         dbo.ProfileEmergencyContact ON dbo.Loads.ProfileId = dbo.ProfileEmergencyContact.Id ON dbo.MaterialCode.ID = dbo.Profile.MaterialCodeId FULL OUTER JOIN
                         dbo.ProfileManifestMailingAddress ON dbo.Loads.ProfileId = dbo.ProfileManifestMailingAddress.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ContainerType]](../Tables/dbo_ContainerType.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[EmergencyContact]](../Tables/dbo_EmergencyContact.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
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

