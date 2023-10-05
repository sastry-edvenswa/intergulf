#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnProfileMaterialClassificationOily

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnProfileMaterialClassificationOily]

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

CREATE FUNCTION [dbo].[fnProfileMaterialClassificationOily] (@String varchar(5000))
RETURNS varchar(5)
 AS  
BEGIN 
declare @c varchar(1)

IF ( Left(@String,1) = 'B')
	SET @C = Left(@String,1)
ELSE
	SET @C = null
Return @C
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

