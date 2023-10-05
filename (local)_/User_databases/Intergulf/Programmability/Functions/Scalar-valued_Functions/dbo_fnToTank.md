#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnToTank

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnToTank]

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


CREATE FUNCTION [dbo].[fnToTank] (@LoadTank as VARCHAR(255), @LabTank as VARCHAR(255),@TransactionType as VARCHAR(255))
RETURNS VARCHAR(225)
 AS  
BEGIN 
declare @ToTank VARCHAR(255)

IF @TransactionType = "Sale"
	SET @ToTank = null
ELSE IF @TransactionType = "Tank Sale"
	SET @ToTank = null
ELSE IF @TransactionType = "Decant"
	SET @ToTank = null
ELSE
	SET @ToTank = @LabTank


Return @ToTank
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

