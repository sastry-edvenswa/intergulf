#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectInventoryRailCarContracts

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectInventoryRailCarContracts]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:01:06 PM Tuesday, August 12, 2008 |
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

CREATE VIEW [dbo].[vwSelectInventoryRailCarContracts]
AS
SELECT     dbo.InventoryRailCarContracts.Id, dbo.Vendor.Name AS VendorName, dbo.InventoryRailCarContracts.ExposureDate, 
                      dbo.InventoryRailCarContracts.Category, dbo.InventoryRailCarContracts.Quantity, dbo.InventoryRailCarContracts.MarketCost, 
                      dbo.InventoryRailCarContracts.Comments, dbo.UserMaster.FirstName AS SalesPersonFirstName, 
                      dbo.UserMaster.LastName AS SalesPersonLastName, dbo.InventoryRailCarContracts.Status
FROM         dbo.Vendor RIGHT OUTER JOIN
                      dbo.InventoryRailCarContracts LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.InventoryRailCarContracts.SalesPersonId = dbo.UserMaster.UserName ON 
                      dbo.Vendor.Id = dbo.InventoryRailCarContracts.VendorId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[InventoryRailCarContracts]](../Tables/dbo_InventoryRailCarContracts.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

