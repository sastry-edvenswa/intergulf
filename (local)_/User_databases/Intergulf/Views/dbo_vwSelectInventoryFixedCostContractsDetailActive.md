#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectInventoryFixedCostContractsDetailActive

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectInventoryFixedCostContractsDetailActive]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:21:56 PM Tuesday, August 12, 2008 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ContractId | bigint | 8 |
| ExposureDate | datetime | 8 |
| Quantity | bigint | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |
| UpdateComputer | varchar(50) | 50 |
| Status | varchar(10) | 10 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectInventoryFixedCostContractsDetailActive]
AS
SELECT     dbo.InventoryFixedCostContractsDetail.*, dbo.InventoryFixedCostContracts.Status
FROM         dbo.InventoryFixedCostContracts RIGHT OUTER JOIN
                      dbo.InventoryFixedCostContractsDetail ON dbo.InventoryFixedCostContracts.Id = dbo.InventoryFixedCostContractsDetail.ContractId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[InventoryFixedCostContracts]](../Tables/dbo_InventoryFixedCostContracts.md)
* [[dbo].[InventoryFixedCostContractsDetail]](../Tables/dbo_InventoryFixedCostContractsDetail.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

