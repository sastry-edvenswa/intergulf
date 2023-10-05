#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectDriver

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectDriver]

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
CREATE FUNCTION [dbo].[fnSelectDriver]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.Driver
        Order By FirstName,LastName
       )

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Driver]](../../../Tables/dbo_Driver.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwDriver]](../../../Views/dbo_vwDriver.md)
* [[dbo].[vwRptLoadAccountingDetail]](../../../Views/dbo_vwRptLoadAccountingDetail.md)
* [[dbo].[vwRptLoadLabWorksheet]](../../../Views/dbo_vwRptLoadLabWorksheet.md)
* [[dbo].[vwSelectExportLoadArrivalTimePerformance]](../../../Views/dbo_vwSelectExportLoadArrivalTimePerformance.md)
* [[dbo].[vwSelectExportLoadsForAccounting]](../../../Views/dbo_vwSelectExportLoadsForAccounting.md)
* [[dbo].[vwSelectLoadsReadyForAccounting]](../../../Views/dbo_vwSelectLoadsReadyForAccounting.md)
* [[dbo].[vwSelectLoadsReadyForAccountingExport]](../../../Views/dbo_vwSelectLoadsReadyForAccountingExport.md)
* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../../../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)
* [[dbo].[vwSelectPendingLoadsNew]](../../../Views/dbo_vwSelectPendingLoadsNew.md)
* [[dbo].[vwSelectReadyToBillLoads]](../../../Views/dbo_vwSelectReadyToBillLoads.md)
* [[dbo].[vwSelectReadyToBillLoadsInternal]](../../../Views/dbo_vwSelectReadyToBillLoadsInternal.md)
* [[dbo].[vwSelectReadyToBillLoadsInternalNew]](../../../Views/dbo_vwSelectReadyToBillLoadsInternalNew.md)
* [[dbo].[vwSelectReadyToBillLoadsNew]](../../../Views/dbo_vwSelectReadyToBillLoadsNew.md)
* [[dbo].[fnSelectLoadsReadyToBill]](dbo_fnSelectLoadsReadyToBill.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

