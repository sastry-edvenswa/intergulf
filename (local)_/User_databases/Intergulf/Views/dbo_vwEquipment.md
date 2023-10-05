#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwEquipment

# ![Views](../../../../Images/View32.png) [dbo].[vwEquipment]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:37:26 PM Sunday, February 11, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| Status | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| DriverId | bigint | 8 |
| TransporterId | bigint | 8 |
| VinNo | varchar(50) | 50 |
| MakeYear | varchar(50) | 50 |
| Make | varchar(50) | 50 |
| LicensePlate | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwEquipment]
AS
SELECT     fnSelectEquipment.*
FROM         dbo.fnSelectEquipment() fnSelectEquipment
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectEquipment]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectEquipment.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

