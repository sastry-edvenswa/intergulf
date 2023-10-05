#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectMaterialCode

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectMaterialCode]

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
CREATE FUNCTION [dbo].[fnSelectMaterialCode]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.MaterialCode
        Order by MaterialCode
       )



GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[MaterialCode]](../../../Tables/dbo_MaterialCode.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwMaterialCode]](../../../Views/dbo_vwMaterialCode.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

