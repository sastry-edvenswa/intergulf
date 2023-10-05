#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectStates

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectStates]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | NO |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO
CREATE FUNCTION [dbo].[fnSelectStates]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.States
        Order by State
       )
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[States]](../../../Tables/dbo_States.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

