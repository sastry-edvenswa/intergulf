#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectPendingLoads

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectPendingLoads]

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
CREATE FUNCTION [dbo].[fnSelectPendingLoads]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 percent *
        FROM dbo.Loads
        Where DispatchStatus = 'Pending'
        Order by ScheduledDate,ScheduledTime
)

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../../../Tables/dbo_Loads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

