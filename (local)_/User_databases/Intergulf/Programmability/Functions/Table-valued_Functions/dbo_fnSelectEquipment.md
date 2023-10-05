#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectEquipment

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectEquipment]

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


CREATE FUNCTION [dbo].[fnSelectEquipment]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 percent *
        FROM dbo.Equipment
        Order By Type DESC,Id
       )



GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Equipment]](../../../Tables/dbo_Equipment.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwEquipment]](../../../Views/dbo_vwEquipment.md)
* [[dbo].[vwRptLoadAccountingDetail]](../../../Views/dbo_vwRptLoadAccountingDetail.md)
* [[dbo].[vwRptLoadLabWorksheet]](../../../Views/dbo_vwRptLoadLabWorksheet.md)
* [[dbo].[vwSelectReadyToBillLoads]](../../../Views/dbo_vwSelectReadyToBillLoads.md)
* [[dbo].[vwSelectReadyToBillLoadsInternal]](../../../Views/dbo_vwSelectReadyToBillLoadsInternal.md)
* [[dbo].[vwSelectReadyToBillLoadsInternalNew]](../../../Views/dbo_vwSelectReadyToBillLoadsInternalNew.md)
* [[dbo].[vwSelectReadyToBillLoadsNew]](../../../Views/dbo_vwSelectReadyToBillLoadsNew.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

