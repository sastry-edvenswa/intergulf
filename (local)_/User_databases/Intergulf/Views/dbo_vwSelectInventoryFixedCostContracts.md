#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectInventoryFixedCostContracts

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectInventoryFixedCostContracts]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:55:37 PM Tuesday, August 12, 2008 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| VendorName | varchar(50) | 50 |
| ExposureDate | datetime | 8 |
| Category | varchar(50) | 50 |
| Quantity | bigint | 8 |
| MarketCost | numeric(18,4) | 9 |
| Comments | varchar(2000) | 2000 |
| SalesPersonFirstName | varchar(50) | 50 |
| SalesPersonLastName | varchar(50) | 50 |
| Status | varchar(10) | 10 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectInventoryFixedCostContracts]
AS
SELECT     dbo.InventoryFixedCostContracts.Id, dbo.Vendor.Name AS VendorName, dbo.InventoryFixedCostContracts.ExposureDate, 
                      dbo.InventoryFixedCostContracts.Category, dbo.InventoryFixedCostContracts.Quantity, dbo.InventoryFixedCostContracts.MarketCost, 
                      dbo.InventoryFixedCostContracts.Comments, dbo.UserMaster.FirstName AS SalesPersonFirstName, 
                      dbo.UserMaster.LastName AS SalesPersonLastName, dbo.InventoryFixedCostContracts.Status
FROM         dbo.UserMaster RIGHT OUTER JOIN
                      dbo.InventoryFixedCostContracts ON dbo.UserMaster.UserName = dbo.InventoryFixedCostContracts.SalesPersonId LEFT OUTER JOIN
                      dbo.Vendor ON dbo.InventoryFixedCostContracts.VendorId = dbo.Vendor.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[InventoryFixedCostContracts]](../Tables/dbo_InventoryFixedCostContracts.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

