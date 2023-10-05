#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnProfileDays

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnProfileDays]

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
| @Status | varchar(255) | 255 |
| @CreateDate | date | 3 |
| @StatusDate | date | 3 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


CREATE FUNCTION [dbo].[fnProfileDays] (@Status as varchar(255), @CreateDate as Date, @StatusDate as Date)
RETURNS int
 AS  
BEGIN 
declare @Days int

IF @Status = 'Active'
	SET @Days = DATEDIFF(DAY,@CreateDate,@StatusDate)
ELSE
	SET @Days = null

If @Days = 0
	Set @Days = 1

Return @Days
END


GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectExportProfilesApprovalDays]](../../../Views/dbo_vwSelectExportProfilesApprovalDays.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

