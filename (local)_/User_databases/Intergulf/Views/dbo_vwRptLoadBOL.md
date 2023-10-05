#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadBOL

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadBOL]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:30:44 PM Wednesday, May 1, 2013 |
| Last Modified | 7:42:34 PM Monday, November 15, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| ProfileId | bigint | 8 |
| Number | varchar(50) | 50 |
| ShippingWeight | decimal(18,0) | 9 |
| Transporter Name | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| Driver FName | varchar(50) | 50 |
| Driver LName | varchar(50) | 50 |
| FunctionShippingName | varchar(5000) | 5000 |
| ShippingName | varchar(1000) | 1000 |
| ContainerType | varchar(200) | 200 |
| MaterialCode | nvarchar(50) | 100 |
| IntergulfDescription | nvarchar(50) | 100 |
| PreProperShippingName | nvarchar(100) | 200 |
| ProperShippingName | nvarchar(300) | 600 |
| PostProperShippingName | nvarchar(100) | 200 |
| ProductPlacardNumber | nvarchar(50) | 100 |
| Hazmat | nvarchar(50) | 100 |
| ProductHazardClass | nvarchar(50) | 100 |
| ProductPackingGroup | nvarchar(50) | 100 |
| Name | nvarchar(100) | 200 |
| Address | nvarchar(50) | 100 |
| City | nvarchar(50) | 100 |
| State | nvarchar(50) | 100 |
| Zip | nvarchar(50) | 100 |
| DispatcherFName | varchar(50) | 50 |
| DispatcherLName | varchar(50) | 50 |
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
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(3000) | 3000 |
| Generator City | varchar(50) | 50 |
| Generator State | varchar(50) | 50 |
| Generator Zip | varchar(50) | 50 |
| Generator Phone | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLoadBOL]
AS
SELECT DISTINCT 
                         TOP (100) PERCENT dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.TrailerId, dbo.Loads.TankNumber, dbo.Loads.DeliveryReleaseNumber, dbo.Loads.ProfileId, dbo.Loads.Number, 
                         dbo.Loads.ShippingWeight, dbo.Transporter.Name AS [Transporter Name], dbo.Profile.ProfileNumber, dbo.Driver.FirstName AS [Driver FName], dbo.Driver.LastName AS [Driver LName], 
                         dbo.fnProperShippingName(dbo.Profile.MaterialCodeId) AS FunctionShippingName, dbo.Profile.ShippingName, dbo.ContainerType.Description AS ContainerType, dbo.MaterialCode.MaterialCode, 
                         dbo.MaterialCode.Description AS IntergulfDescription, dbo.MaterialCode.PreProperShippingName, dbo.MaterialCode.ProperShippingName, dbo.MaterialCode.PostProperShippingName, 
                         dbo.MaterialCode.ProductPlacardNumber, dbo.MaterialCode.Hazmat, dbo.MaterialCode.ProductHazardClass, dbo.MaterialCode.ProductPackingGroup, dbo.Destination.Name, dbo.Destination.Address, 
                         dbo.Destination.City, dbo.Destination.State, dbo.Destination.Zip, dbo.UserMaster.FirstName AS DispatcherFName, dbo.UserMaster.LastName AS DispatcherLName, 
                         dbo.ManifestMailingAddress.Name AS GMailingName, dbo.ManifestMailingAddress.Address AS GMailingAddress, dbo.ManifestMailingAddress.City AS GMailingCity, 
                         dbo.ManifestMailingAddress.State AS GMailingState, dbo.ManifestMailingAddress.Zip AS GMailingZip, dbo.ProfileManifestMailingAddress.Name AS PMailingName, 
                         dbo.ProfileManifestMailingAddress.Address AS PMailingAddress, dbo.ProfileManifestMailingAddress.City AS PMailingCity, dbo.ProfileManifestMailingAddress.State AS PMailingState, 
                         dbo.ProfileManifestMailingAddress.Zip AS PMailingZip, dbo.EmergencyContact.Name AS GContactName, dbo.EmergencyContact.Phone AS GContactPhone, dbo.ProfileEmergencyContact.Name AS PContactName, 
                         dbo.ProfileEmergencyContact.Phone AS PContactPhone, SUBSTRING(dbo.ProductHazardousMaterial.UNNumber, 3, 4) AS UNNumber, dbo.ProductERG.GUIDE_PAGE, dbo.Generator.Name AS [Generator Name], 
                         dbo.Generator.Address AS [Generator Address], dbo.Generator.City AS [Generator City], dbo.Generator.State AS [Generator State], dbo.Generator.Zip AS [Generator Zip], 
                         dbo.Generator.Phone AS [Generator Phone]
FROM            dbo.EmergencyContact RIGHT OUTER JOIN
                         dbo.ManifestMailingAddress RIGHT OUTER JOIN
                         dbo.ProfileManifestMailingAddress RIGHT OUTER JOIN
                         dbo.ProfileEmergencyContact RIGHT OUTER JOIN
                         dbo.ProductERG RIGHT OUTER JOIN
                         dbo.ProductHazardousMaterial ON dbo.ProductERG.UN_NUMBER = SUBSTRING(dbo.ProductHazardousMaterial.UNNumber, 3, 4) RIGHT OUTER JOIN
                         dbo.Profile INNER JOIN
                         dbo.MaterialCode ON dbo.Profile.MaterialCodeId = dbo.MaterialCode.ID INNER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.ProductHazardousMaterial.ID = dbo.MaterialCode.ProperShippingNameId ON dbo.ProfileEmergencyContact.Id = dbo.Profile.Id ON 
                         dbo.ProfileManifestMailingAddress.Id = dbo.Profile.Id ON dbo.ManifestMailingAddress.Id = dbo.Profile.GeneratorId ON dbo.EmergencyContact.Id = dbo.Profile.GeneratorId RIGHT OUTER JOIN
                         dbo.Destination RIGHT OUTER JOIN
                         dbo.Loads LEFT OUTER JOIN
                         dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id LEFT OUTER JOIN
                         dbo.UserMaster ON dbo.Loads.UpdateUser = dbo.UserMaster.UserName ON dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                         dbo.ContainerType ON dbo.Loads.ContainerTypeId = dbo.ContainerType.Id ON dbo.Profile.Id = dbo.Loads.ProfileId LEFT OUTER JOIN
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

