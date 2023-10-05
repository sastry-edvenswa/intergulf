#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectLabTestDisbursement

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectLabTestDisbursement]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE FUNCTION [dbo].[fnSelectLabTestDisbursement]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.LabTestDisbursement
       )


GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTestDisbursement]](../../../Tables/dbo_LabTestDisbursement.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptAirPermitLoads]](../../../Views/dbo_vwRptAirPermitLoads.md)
* [[dbo].[vwSelectLabTestAirPermitLoads]](../../../Views/dbo_vwSelectLabTestAirPermitLoads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

