#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectVendorForSaturn

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectVendorForSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:21:35 PM Thursday, December 15, 2022 |
| Last Modified | 4:24:44 PM Thursday, December 15, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| Name | varchar(50) | 50 |  |
| Address | varchar(300) | 300 |  |
| City | varchar(100) | 100 |  |
| State | varchar(50) | 50 |  |
| Zip | varchar(50) | 50 |  |
| Sage No | varchar(50) | 50 |  |
| ShortName | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectVendorForSaturn]
AS
SELECT        TOP (100) PERCENT Id, Name, Address, City, State, Zip, Mas90Id AS [Sage No], ShortName
FROM            dbo.Vendor
ORDER BY Name
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

