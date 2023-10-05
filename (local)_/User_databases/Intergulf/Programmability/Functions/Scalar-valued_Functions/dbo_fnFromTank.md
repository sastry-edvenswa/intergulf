#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnFromTank

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnFromTank]

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
| @LoadTank | varchar(255) | 255 |
| @LabTank | varchar(255) | 255 |
| @TransactionType | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


CREATE FUNCTION [dbo].[fnFromTank] (@LoadTank as VARCHAR(255), @LabTank as VARCHAR(255),@TransactionType as VARCHAR(255))
RETURNS VARCHAR(255)
 AS  
BEGIN 
declare @FromTank VARCHAR(255)

IF @TransactionType = 'Transfer'
	SET @FromTank = @LoadTank
ELSE IF @TransactionType = 'Tank Transfer'
	SET @FromTank = @LoadTank
ELSE IF @TransactionType = "Sale"
	SET @FromTank = @LabTank
ELSE IF @TransactionType = "Tank Sale"
	SET @FromTank = @LabTank
ELSE IF @TransactionType = "Decant"
	SET @FromTank = @LabTank
ELSE
	SET @FromTank = null


Return @FromTank
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

