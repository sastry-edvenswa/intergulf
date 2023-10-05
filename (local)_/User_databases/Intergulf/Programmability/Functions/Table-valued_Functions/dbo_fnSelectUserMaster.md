#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectUserMaster

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectUserMaster]

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

CREATE FUNCTION [dbo].[fnSelectUserMaster]
                 (  )
RETURNS table
AS
RETURN (
        SELECT Top 100 Percent *
        FROM dbo.UserMaster
        Order by UserName
       )








GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[UserMaster]](../../../Tables/dbo_UserMaster.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadAccountingDetail]](../../../Views/dbo_vwRptLoadAccountingDetail.md)
* [[dbo].[vwRptLoadLabWorksheet]](../../../Views/dbo_vwRptLoadLabWorksheet.md)
* [[dbo].[vwUserMaster]](../../../Views/dbo_vwUserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

