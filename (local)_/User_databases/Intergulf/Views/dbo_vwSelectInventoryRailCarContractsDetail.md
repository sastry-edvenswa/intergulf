#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectInventoryRailCarContractsDetail

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectInventoryRailCarContractsDetail]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:57:45 PM Tuesday, August 12, 2008 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| ContractId | bigint | 8 |  |
| CarNumber | varchar(50) | 50 |  |
| BolNumber | varchar(50) | 50 |  |
| Shipper | varchar(50) | 50 |  |
| ShipDate | datetime | 8 |  |
| ETADate | datetime | 8 |  |
| ArriveDate | datetime | 8 |  |
| CallInDate | datetime | 8 |  |
| SpotDate | datetime | 8 |  |
| DischargeDate | datetime | 8 |  |
| ReleaseDate | datetime | 8 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectInventoryRailCarContractsDetail]
AS
SELECT     TOP 100 PERCENT Id, ContractId, CarNumber, BolNumber, Shipper, ShipDate, ETADate, ArriveDate, CallInDate, SpotDate, DischargeDate, 
                      ReleaseDate
FROM         dbo.InventoryRailCarContractsDetail
ORDER BY CarNumber, ShipDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[InventoryRailCarContractsDetail]](../Tables/dbo_InventoryRailCarContractsDetail.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

