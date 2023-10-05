#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectLabTestSample

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectLabTestSample]

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
CREATE FUNCTION [dbo].[fnSelectLabTestSample]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.LabTestSample
       )

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTestSample]](../../../Tables/dbo_LabTestSample.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectLabTestSample]](../../../Views/dbo_vwSelectLabTestSample.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

