#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSaturnTestVendor

# ![Views](../../../../Images/View32.png) [dbo].[vwSaturnTestVendor]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:21:19 PM Thursday, February 16, 2023 |
| Last Modified | 3:21:19 PM Thursday, February 16, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| Mas90Id | varchar(50) | 50 |  |
| Name | varchar(50) | 50 |  |
| ShortName | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSaturnTestVendor]
AS
SELECT        TOP (100) PERCENT Id, Mas90Id, Name, ShortName
FROM            dbo.Vendor
ORDER BY ShortName
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

