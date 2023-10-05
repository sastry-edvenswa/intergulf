#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectVendor

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectVendor]

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
CREATE FUNCTION [dbo].[fnSelectVendor]
                 (  )


RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.Vendor
        Order by Name
       )

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Vendor]](../../../Tables/dbo_Vendor.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfileNew]](../../../Views/dbo_vwChooseProfileNew.md)
* [[dbo].[vwRptLoadAccountingDetail]](../../../Views/dbo_vwRptLoadAccountingDetail.md)
* [[dbo].[vwRptLoadLabWorksheet]](../../../Views/dbo_vwRptLoadLabWorksheet.md)
* [[dbo].[vwSelectExportLoadArrivalTimePerformance]](../../../Views/dbo_vwSelectExportLoadArrivalTimePerformance.md)
* [[dbo].[vwSelectExportLoadsForAccounting]](../../../Views/dbo_vwSelectExportLoadsForAccounting.md)
* [[dbo].[vwSelectLoadsReadyForAccounting]](../../../Views/dbo_vwSelectLoadsReadyForAccounting.md)
* [[dbo].[vwSelectLoadsReadyForAccountingExport]](../../../Views/dbo_vwSelectLoadsReadyForAccountingExport.md)
* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../../../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)
* [[dbo].[vwSelectProfilesInReview]](../../../Views/dbo_vwSelectProfilesInReview.md)
* [[dbo].[vwSelectProfilesRecertificationDateExpired]](../../../Views/dbo_vwSelectProfilesRecertificationDateExpired.md)
* [[dbo].[vwVendor]](../../../Views/dbo_vwVendor.md)
* [[dbo].[fnSelectProfileGlobalSearch]](dbo_fnSelectProfileGlobalSearch.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

