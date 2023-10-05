#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectLoadRequest

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectLoadRequest]

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
CREATE FUNCTION [dbo].[fnSelectLoadRequest]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.LoadRequest
       )
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadRequest]](../../../Tables/dbo_LoadRequest.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadRequest]](../../../Views/dbo_vwRptLoadRequest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

