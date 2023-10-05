#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnSaturnQty

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnSaturnQty]

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
| @LabQuantity | decimal(18,0) | 9 |
| @LabUnit | varchar(255) | 255 |
| @ActualQuantity | decimal(18,0) | 9 |
| @ActualUnit | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


CREATE FUNCTION [dbo].[fnSaturnQty] (@LabQuantity as decimal(18,0), @LabUnit as VARCHAR(255),@ActualQuantity as decimal(18,0),@ActualUnit as VARCHAR(255))
RETURNS decimal(18,0)
 AS  
BEGIN 
declare @SaturnQty decimal(18,0)

IF @LabUnit = "Percent"
	SET @SaturnQty = @ActualQuantity * @LabQuantity / 100
ELSE
	SET @SaturnQty = @LabQuantity


Return @SaturnQty
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

