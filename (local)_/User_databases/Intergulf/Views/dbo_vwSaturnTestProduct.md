#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSaturnTestProduct

# ![Views](../../../../Images/View32.png) [dbo].[vwSaturnTestProduct]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:23:15 PM Thursday, February 16, 2023 |
| Last Modified | 3:23:15 PM Thursday, February 16, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Product | varchar(10) | 10 |
| Description | varchar(500) | 500 |
| Inventry | bit | 1 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSaturnTestProduct]
AS
SELECT        TOP (100) PERCENT Product, Description, Inventry
FROM            dbo.Product
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Product]](../Tables/dbo_Product.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

