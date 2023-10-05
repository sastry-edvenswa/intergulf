#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnLoadTime

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnLoadTime]

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
| @StartTime | real | 4 |
| @EndTime | real | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


CREATE FUNCTION [dbo].[fnLoadTime] (@StartTime real,@EndTime Real)
RETURNS Real
 AS  
BEGIN 
declare @ElaspedTime real

IF @EndTime > @StartTime
	SET @ElaspedTime = @EndTime - @StartTime
ELSE
	SET @ElaspedTime = (@EndTime + 24) - @StartTime
Return @ElaspedTime
END


GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectLoads4thQtrBayportLoadTimes]](../../../Views/dbo_vwSelectLoads4thQtrBayportLoadTimes.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

