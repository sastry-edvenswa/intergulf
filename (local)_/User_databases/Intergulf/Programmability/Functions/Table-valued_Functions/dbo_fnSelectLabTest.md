#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectLabTest

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectLabTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE   FUNCTION [dbo].[fnSelectLabTest]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.LabTest
       )




GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../../../Tables/dbo_LabTest.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptAirPermitLoads]](../../../Views/dbo_vwRptAirPermitLoads.md)
* [[dbo].[vwRptLoadAccountingDetail]](../../../Views/dbo_vwRptLoadAccountingDetail.md)
* [[dbo].[vwRptLoadLabWorksheet]](../../../Views/dbo_vwRptLoadLabWorksheet.md)
* [[dbo].[vwSelectExportLoadArrivalTimePerformance]](../../../Views/dbo_vwSelectExportLoadArrivalTimePerformance.md)
* [[dbo].[vwSelectExportLoadsForAccounting]](../../../Views/dbo_vwSelectExportLoadsForAccounting.md)
* [[dbo].[vwSelectLabTestAirPermitLoads]](../../../Views/dbo_vwSelectLabTestAirPermitLoads.md)
* [[dbo].[vwSelectLoadsReadyForAccounting]](../../../Views/dbo_vwSelectLoadsReadyForAccounting.md)
* [[dbo].[vwSelectLoadsReadyForAccountingExport]](../../../Views/dbo_vwSelectLoadsReadyForAccountingExport.md)
* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../../../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

