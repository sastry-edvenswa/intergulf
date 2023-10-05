#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectTankTurnLabTests

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectTankTurnLabTests]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE  FUNCTION [dbo].[fnSelectTankTurnLabTests]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.TankTest
       )

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[TankTest]](../../../Tables/dbo_TankTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

