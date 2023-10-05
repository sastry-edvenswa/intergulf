#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnUpdateDateTimeSaturn

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnUpdateDateTimeSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @loadUpdateDate | datetime | 8 |
| @LabUpdateDate | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE FUNCTION [dbo].[fnUpdateDateTimeSaturn] (@loadUpdateDate as datetime,@LabUpdateDate as datetime)
RETURNS datetime
 AS  
BEGIN 
declare @ReturnUpdateDate as datetime

IF @loadUpdateDate > @LabUpdateDate
	SET @ReturnUpdateDate = @loadUpdateDate
ELSE IF @LabUpdateDate > @loadUpdateDate
	SET @ReturnUpdateDate = @LabUpdateDate

Return @ReturnUpdateDate
END


GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectSaturnTransactions]](../../../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../../../Views/dbo_vwSelectSaturnTransactionsBackup.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

