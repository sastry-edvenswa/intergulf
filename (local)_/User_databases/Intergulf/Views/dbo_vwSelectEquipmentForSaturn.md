#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectEquipmentForSaturn

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectEquipmentForSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:33:51 PM Thursday, December 15, 2022 |
| Last Modified | 4:33:51 PM Thursday, December 15, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| Status | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectEquipmentForSaturn]
AS
SELECT        TOP (100) PERCENT Id, Description, Type, Status
FROM            dbo.Equipment
ORDER BY Type DESC, Description
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

