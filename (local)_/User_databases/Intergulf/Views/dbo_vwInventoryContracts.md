#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwInventoryContracts

# ![Views](../../../../Images/View32.png) [dbo].[vwInventoryContracts]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:29:12 PM Monday, January 28, 2008 |
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
| MarketCost | numeric(18,2) | 9 |
| Comments | varchar(2000) | 2000 |
| SalesPersonFirstName | varchar(50) | 50 |
| SalesPersonLastName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwInventoryContracts]
AS
SELECT     dbo.InventoryContracts.Id, dbo.Vendor.Name AS VendorName, dbo.InventoryContracts.ExposureDate, dbo.InventoryContracts.Category, 
                      dbo.InventoryContracts.Quantity, dbo.InventoryContracts.MarketCost, dbo.InventoryContracts.Comments, 
                      dbo.UserMaster.FirstName AS SalesPersonFirstName, dbo.UserMaster.LastName AS SalesPersonLastName
FROM         dbo.UserMaster RIGHT OUTER JOIN
                      dbo.InventoryContracts ON dbo.UserMaster.UserName = dbo.InventoryContracts.SalesPersonId LEFT OUTER JOIN
                      dbo.Vendor ON dbo.InventoryContracts.VendorId = dbo.Vendor.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

