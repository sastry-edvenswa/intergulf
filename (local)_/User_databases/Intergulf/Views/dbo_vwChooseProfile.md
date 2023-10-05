#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwChooseProfile

# ![Views](../../../../Images/View32.png) [dbo].[vwChooseProfile]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:10:35 AM Wednesday, August 12, 2015 |
| Last Modified | 12:59:35 PM Tuesday, October 4, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(3000) | 3000 |
| Profile Number | varchar(50) | 50 |
| Customer Id | bigint | 8 |
| Customer Name | varchar(100) | 100 |
| Vendor Id | bigint | 8 |
| Vendor Name | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| Direction | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialClassification | varchar(200) | 200 |
| MaterialCodeId | int | 4 |
| ProductCategory | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| ProcessDescription | varchar(3000) | 3000 |
| DocumentType | varchar(50) | 50 |
| ContactName | varchar(50) | 50 |
| ContactEmail | varchar(50) | 50 |
| ContactPhone | varchar(50) | 50 |
| ContactFax | varchar(50) | 50 |
| DeepWell | varchar(50) | 50 |
| DispatchNotes | varchar(6000) | 6000 |
| HazMat | varchar(50) | 50 |
| SpecialEquipment | varchar(3000) | 3000 |
| SpecialInstructions | varchar(3000) | 3000 |
| BillingDepartment | varchar(100) | 100 |
| MSDSFileName | varchar(600) | 600 |
| LinkProfileId | bigint | 8 |
| DestinationId | bigint | 8 |
| Destination | nvarchar(100) | 200 |
| HTYes | varchar(50) | 50 |
| ShippingName | varchar(5000) | 5000 |
| Status | varchar(20) | 20 |
| DOTCorrosive | bit | 1 |
| CSUOilBearing | bit | 1 |
| EPAWasteCode1 | varchar(10) | 10 |
| EPAWasteCode2 | varchar(10) | 10 |
| EPAWasteCode3 | varchar(10) | 10 |
| EPAWasteCode4 | varchar(10) | 10 |
| DestinationDisplay | varchar(255) | 255 |
| NESHAP | bit | 1 |
| ContractNumber | varchar(20) | 20 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwChooseProfile]
AS
SELECT        TOP (100) PERCENT dbo.Profile.Id, dbo.Profile.GeneratorId AS [Generator Id], dbo.Generator.Name AS [Generator Name], dbo.Generator.Address AS [Generator Address], 
                         dbo.Profile.ProfileNumber AS [Profile Number], dbo.Profile.CustomerId AS [Customer Id], dbo.Customer.Name AS [Customer Name], dbo.Profile.VendorId AS [Vendor Id], dbo.Vendor.Name AS [Vendor Name], 
                         dbo.Profile.MaterialDescription, dbo.Profile.Direction, dbo.Profile.ProfileType, dbo.Profile.WasteCode, dbo.Profile.MaterialClassification, dbo.Profile.MaterialCodeId, dbo.Profile.ProductCategory, 
                         dbo.Profile.SalesPersonId, dbo.Profile.ProcessDescription, dbo.Profile.DocumentType, dbo.Profile.ContactName, dbo.Profile.ContactEmail, dbo.Profile.ContactPhone, dbo.Profile.ContactFax, dbo.Profile.DeepWell, 
                         dbo.Profile.DispatchNotes, dbo.Profile.HazMat, dbo.Profile.SpecialEquipment, dbo.Profile.SpecialInstructions, dbo.Profile.BillingDepartment, dbo.Profile.MSDSFileName, dbo.Profile.LinkProfileId, 
                         dbo.Profile.DestinationId, dbo.Destination.Name AS Destination, dbo.Profile.HTYes, dbo.fnProperShippingName(dbo.Profile.MaterialCodeId) AS ShippingName, dbo.Profile.Status, dbo.Profile.DOTCorrosive, 
                         dbo.Profile.CSUOilBearing, dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.fnGetDestinationDisplay(dbo.Destination.Name, 
                         dbo.Destination.Facility) AS DestinationDisplay, dbo.Profile.NESHAP, dbo.Profile.ContractNumber
FROM            dbo.Profile LEFT OUTER JOIN
                         dbo.Destination ON dbo.Profile.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Vendor ON dbo.Profile.VendorId = dbo.Vendor.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
ORDER BY [Generator Name]
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)
* [[dbo].[fnGetDestinationDisplay]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnGetDestinationDisplay.md)
* [[dbo].[fnProperShippingName]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProperShippingName.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

