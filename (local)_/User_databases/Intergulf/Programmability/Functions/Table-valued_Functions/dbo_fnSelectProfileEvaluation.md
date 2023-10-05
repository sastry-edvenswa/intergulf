#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectProfileEvaluation

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectProfileEvaluation]

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
CREATE FUNCTION [dbo].[fnSelectProfileEvaluation]
                 (  )
RETURNS table
AS
RETURN (
        SELECT *
        FROM dbo.ProfileEvaluation
       )
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ProfileEvaluation]](../../../Tables/dbo_ProfileEvaluation.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwProfileEvaluation]](../../../Views/dbo_vwProfileEvaluation.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

