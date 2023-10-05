#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectShippingMethod

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectShippingMethod]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET ANSI_NULLS OFF
GO
CREATE FUNCTION [dbo].[fnSelectShippingMethod]
                 (  )
RETURNS table
AS
RETURN (
        SELECT top 100 percent *
        FROM dbo.ShippingMethod
        Order by Description
       )

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ShippingMethod]](../../../Tables/dbo_ShippingMethod.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwShippingMethod]](../../../Views/dbo_vwShippingMethod.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

