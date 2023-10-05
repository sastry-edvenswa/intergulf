#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProducts

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProducts]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:26:56 PM Wednesday, November 16, 2022 |
| Last Modified | 2:26:56 PM Wednesday, November 16, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Product | varchar(10) | 10 |
| Description | varchar(500) | 500 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProducts]
AS
SELECT        TOP (100) PERCENT Product, Description
FROM            dbo.Product
ORDER BY Product
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Product]](../Tables/dbo_Product.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

