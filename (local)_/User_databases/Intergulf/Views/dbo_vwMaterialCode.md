#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwMaterialCode

# ![Views](../../../../Images/View32.png) [dbo].[vwMaterialCode]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:43:23 AM Saturday, February 10, 2007 |
| Last Modified | 3:23:16 PM Wednesday, November 20, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ID | int | 4 |
| MaterialCode | nvarchar(50) | 100 |
| Description | nvarchar(50) | 100 |
| PreProperShippingName | nvarchar(100) | 200 |
| ProperShippingName | nvarchar(300) | 600 |
| PostProperShippingName | nvarchar(100) | 200 |
| ProfileType | nvarchar(50) | 100 |
| AltProperShippingName | nvarchar(100) | 200 |
| MSDSNumber | nvarchar(50) | 100 |
| Notes | ntext | max |
| Hazmat | nvarchar(50) | 100 |
| Number | nvarchar(50) | 100 |
| PackageType | nvarchar(50) | 100 |
| ProductName | nvarchar(50) | 100 |
| ProductClassification | nvarchar(50) | 100 |
| ProductPackingGroup | nvarchar(50) | 100 |
| ProductHazardClass | nvarchar(50) | 100 |
| ProductPlacardNumber | nvarchar(50) | 100 |
| CustomersUsing | nvarchar(50) | 100 |
| IntergulfClass | nvarchar(50) | 100 |
| ProperShippingNameId | bigint | 8 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |
| IsRQ | bit | 1 |
| IsWaste | bit | 1 |
| Constituents1 | nvarchar(50) | 100 |
| Constituents2 | nvarchar(50) | 100 |
| ReviewedById | nvarchar(50) | 100 |
| UseProperShippingName | nvarchar(500) | 1000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwMaterialCode]
AS
SELECT        ID, MaterialCode, Description, PreProperShippingName, ProperShippingName, PostProperShippingName, ProfileType, AltProperShippingName, MSDSNumber, Notes, Hazmat, Number, PackageType, 
                         ProductName, ProductClassification, ProductPackingGroup, ProductHazardClass, ProductPlacardNumber, CustomersUsing, IntergulfClass, ProperShippingNameId, UpdateDateTime, UpdateUser, UpdateComputer, 
                         IsRQ, IsWaste, Constituents1, Constituents2, ReviewedById, UseProperShippingName
FROM            dbo.fnSelectMaterialCode() AS fnSelectMaterialCode
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectMaterialCode]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectMaterialCode.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

