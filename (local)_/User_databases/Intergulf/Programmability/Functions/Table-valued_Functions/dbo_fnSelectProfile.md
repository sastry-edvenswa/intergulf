#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectProfile

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectProfile]

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

CREATE      FUNCTION [dbo].[fnSelectProfile]
                 (  )
RETURNS table
AS
RETURN (
        SELECT *
        FROM dbo.Profile

       )

















GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Profile]](../../../Tables/dbo_Profile.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfileNew]](../../../Views/dbo_vwChooseProfileNew.md)
* [[dbo].[vwProfile]](../../../Views/dbo_vwProfile.md)
* [[dbo].[vwRptAirPermitLoads]](../../../Views/dbo_vwRptAirPermitLoads.md)
* [[dbo].[vwRptLoadAccountingDetail]](../../../Views/dbo_vwRptLoadAccountingDetail.md)
* [[dbo].[vwRptLoadLabWorksheet]](../../../Views/dbo_vwRptLoadLabWorksheet.md)
* [[dbo].[vwSelectExportLoadArrivalTimePerformance]](../../../Views/dbo_vwSelectExportLoadArrivalTimePerformance.md)
* [[dbo].[vwSelectExportLoadsForAccounting]](../../../Views/dbo_vwSelectExportLoadsForAccounting.md)
* [[dbo].[vwSelectLoadsAccountingActive]](../../../Views/dbo_vwSelectLoadsAccountingActive.md)
* [[dbo].[vwSelectLoadsReadyForAccounting]](../../../Views/dbo_vwSelectLoadsReadyForAccounting.md)
* [[dbo].[vwSelectLoadsReadyForAccountingExport]](../../../Views/dbo_vwSelectLoadsReadyForAccountingExport.md)
* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../../../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)
* [[dbo].[vwSelectPendingLoadsNew]](../../../Views/dbo_vwSelectPendingLoadsNew.md)
* [[dbo].[vwSelectProfile]](../../../Views/dbo_vwSelectProfile.md)
* [[dbo].[vwSelectProfilesInReview]](../../../Views/dbo_vwSelectProfilesInReview.md)
* [[dbo].[vwSelectProfilesRecertificationDateExpired]](../../../Views/dbo_vwSelectProfilesRecertificationDateExpired.md)
* [[dbo].[vwSelectReadyToBillLoads]](../../../Views/dbo_vwSelectReadyToBillLoads.md)
* [[dbo].[vwSelectReadyToBillLoadsInternal]](../../../Views/dbo_vwSelectReadyToBillLoadsInternal.md)
* [[dbo].[vwSelectReadyToBillLoadsInternalNew]](../../../Views/dbo_vwSelectReadyToBillLoadsInternalNew.md)
* [[dbo].[vwSelectReadyToBillLoadsNew]](../../../Views/dbo_vwSelectReadyToBillLoadsNew.md)
* [[dbo].[fnSelectLoadsReadyToBill]](dbo_fnSelectLoadsReadyToBill.md)
* [[dbo].[fnSelectProfileGlobalSearch]](dbo_fnSelectProfileGlobalSearch.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

