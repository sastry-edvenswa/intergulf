#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectInventoryRailCarContractsDetailActive

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectInventoryRailCarContractsDetailActive]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:17:51 PM Tuesday, August 12, 2008 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ContractId | bigint | 8 |
| ContractDetailId | bigint | 8 |
| ExposureDate | datetime | 8 |
| Quantity | bigint | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |
| UpdateComputer | varchar(50) | 50 |
| Status | varchar(10) | 10 |
| Type | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectInventoryRailCarContractsDetailActive]
AS
SELECT     dbo.InventoryRailCarContractsDetails.*, dbo.InventoryRailCarContracts.Status, dbo.InventoryRailCarContracts.Type
FROM         dbo.InventoryRailCarContracts RIGHT OUTER JOIN
                      dbo.InventoryRailCarContractsDetails ON dbo.InventoryRailCarContracts.Id = dbo.InventoryRailCarContractsDetails.ContractId
WHERE     (dbo.InventoryRailCarContracts.Status = 'Active') AND (dbo.InventoryRailCarContracts.Type = 'FIXED')

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[InventoryRailCarContracts]](../Tables/dbo_InventoryRailCarContracts.md)
* [[dbo].[InventoryRailCarContractsDetails]](../Tables/dbo_InventoryRailCarContractsDetails.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

