#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadRequest

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadRequest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:14:22 PM Sunday, April 8, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| SalesPersonId | varchar(50) | 50 |
| CustomerId | bigint | 8 |
| VendorId | bigint | 8 |
| ProfileId | bigint | 8 |
| ContactName | varchar(50) | 50 |
| ContactPhone | varchar(50) | 50 |
| PickupLocation | varchar(50) | 50 |
| LoadRequestDate | datetime | 8 |
| LoadRequestTime | varchar(50) | 50 |
| NoLoads | decimal(18,0) | 9 |
| EstQuantity | varchar(50) | 50 |
| EquipmentType | varchar(50) | 50 |
| SubOk | varchar(50) | 50 |
| SpecialRequirements | varchar(3000) | 3000 |
| DestinationId | bigint | 8 |
| WashOutRequired | varchar(50) | 50 |
| WeightTicket | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |
| CreateUser | varchar(50) | 50 |
| CreateDate | datetime | 8 |
| CreateTime | datetime | 8 |
| Processed | int | 4 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| Direction | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| HazMat | varchar(50) | 50 |
| DocumentType | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| Vendor Name | varchar(50) | 50 |
| Destination Name | nvarchar(100) | 200 |
| SalesPerson First Name | varchar(50) | 50 |
| SalesPerson Last Name | varchar(50) | 50 |
| Material Code Id | nvarchar(50) | 100 |
| Material Code Description | nvarchar(50) | 100 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLoadRequest]
AS
SELECT     fnSelectLoadRequest.Id, fnSelectLoadRequest.SalesPersonId, fnSelectLoadRequest.CustomerId, fnSelectLoadRequest.VendorId, 
                      fnSelectLoadRequest.ProfileId, fnSelectLoadRequest.ContactName, fnSelectLoadRequest.ContactPhone, fnSelectLoadRequest.PickupLocation, 
                      fnSelectLoadRequest.LoadRequestDate, fnSelectLoadRequest.LoadRequestTime, fnSelectLoadRequest.NoLoads, fnSelectLoadRequest.EstQuantity, 
                      fnSelectLoadRequest.EquipmentType, fnSelectLoadRequest.SubOk, fnSelectLoadRequest.SpecialRequirements, fnSelectLoadRequest.DestinationId, 
                      fnSelectLoadRequest.WashOutRequired, fnSelectLoadRequest.WeightTicket, fnSelectLoadRequest.VesselTank, fnSelectLoadRequest.CreateUser, 
                      fnSelectLoadRequest.CreateDate, fnSelectLoadRequest.CreateTime, fnSelectLoadRequest.Processed, fnSelectLoadRequest.UpdateDateTime, 
                      fnSelectLoadRequest.UpdateUser, fnSelectLoadRequest.UpdateComputer, dbo.Profile.ProfileNumber, dbo.Profile.MaterialDescription, 
                      dbo.Profile.Direction, dbo.Profile.ProfileType, dbo.Profile.HazMat, dbo.Profile.DocumentType, dbo.Generator.Name AS [Generator Name], 
                      dbo.Customer.Name AS [Customer Name], dbo.Vendor.Name AS [Vendor Name], dbo.Destination.Name AS [Destination Name], 
                      dbo.UserMaster.FirstName AS [SalesPerson First Name], dbo.UserMaster.LastName AS [SalesPerson Last Name], 
                      dbo.MaterialCode.MaterialCode AS [Material Code Id], dbo.MaterialCode.Description AS [Material Code Description]
FROM         dbo.UserMaster RIGHT OUTER JOIN
                      dbo.MaterialCode RIGHT OUTER JOIN
                      dbo.Profile ON dbo.MaterialCode.ID = dbo.Profile.MaterialCodeId ON dbo.UserMaster.UserName = dbo.Profile.SalesPersonId LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id RIGHT OUTER JOIN
                      dbo.Vendor RIGHT OUTER JOIN
                      dbo.fnSelectLoadRequest() fnSelectLoadRequest LEFT OUTER JOIN
                      dbo.Destination ON fnSelectLoadRequest.DestinationId = dbo.Destination.Id ON dbo.Vendor.Id = fnSelectLoadRequest.VendorId LEFT OUTER JOIN
                      dbo.Customer ON fnSelectLoadRequest.CustomerId = dbo.Customer.Id ON dbo.Profile.Id = fnSelectLoadRequest.ProfileId
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)
* [[dbo].[fnSelectLoadRequest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoadRequest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

