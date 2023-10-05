#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnProfileMaterialClassificationDescription

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnProfileMaterialClassificationDescription]

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
| @String | varchar(5000) | 5000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnProfileMaterialClassificationDescription] (@String varchar(5000))
RETURNS varchar(5000)
 AS  
BEGIN 
declare @c varchar(1000)
declare @i int

	SET @i = (LEN(@String) - CHARINDEX('-',@String,0)-1)

	SET @c = RIGHT(@String,@i)

Return @c
END
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectMonthlyDischarge]](../../../Views/dbo_vwSelectMonthlyDischarge.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

