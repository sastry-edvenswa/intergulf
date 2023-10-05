#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectRequestedLoads

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectRequestedLoads]

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
CREATE FUNCTION [dbo].[fnSelectRequestedLoads]
                 (  )
RETURNS table
AS
RETURN (
SELECT     TOP 100 PERCENT *
FROM         dbo.LoadRequest
WHERE     (Processed = '0')
ORDER BY LoadRequestDate, LoadRequestTime
       )

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadRequest]](../../../Tables/dbo_LoadRequest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

