#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnCleanNotes

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnCleanNotes]

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
| @Notes | varchar(6000) | 6000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


CREATE FUNCTION [dbo].[fnCleanNotes] (@Notes as varchar(6000))
RETURNS varchar(6000)
 AS  
BEGIN 
declare @ReturnNotes varchar(6000)

SET @ReturnNotes = REPLACE(@Notes, ',', CHAR(10))
SET @ReturnNotes = REPLACE(@ReturnNotes, ',', CHAR(13))
SET @ReturnNotes = REPLACE(@ReturnNotes, ',', CHAR(9))

Return @ReturnNotes
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

