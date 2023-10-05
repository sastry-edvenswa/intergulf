#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectProductHazardousMaterial

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectProductHazardousMaterial]

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
CREATE FUNCTION [dbo].[fnSelectProductHazardousMaterial]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 percent *
        FROM dbo.ProductHazardousMaterial
        Order By ProperShippingName
)
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ProductHazardousMaterial]](../../../Tables/dbo_ProductHazardousMaterial.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

