#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwShippingMethod

# ![Views](../../../../Images/View32.png) [dbo].[vwShippingMethod]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:32:28 AM Saturday, February 10, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Description | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwShippingMethod]
AS
SELECT     fnSelectShippingMethod.*
FROM         dbo.fnSelectShippingMethod() fnSelectShippingMethod
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectShippingMethod]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectShippingMethod.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

