#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnSaturnUnits

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnSaturnUnits]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | NO |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @LabQuantity | decimal(18,2) | 9 |
| @LabUnit | varchar(255) | 255 |
| @ActualQuantity | decimal(18,2) | 9 |
| @ActualUnit | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


Create FUNCTION [dbo].[fnSaturnUnits] (@LabQuantity as decimal(18,2), @LabUnit as VARCHAR(255),@ActualQuantity as decimal(18,2),@ActualUnit as VARCHAR(255))
RETURNS varchar(255)
 AS  
BEGIN 
declare @SaturnUnits varchar(255)

IF @LabUnit = "Percent"
	SET @SaturnUnits = @ActualUnit
ELSE
	SET @SaturnUnits = @LabUnit


Return @SaturnUnits
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

