#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnProfileHazardYesNo

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnProfileHazardYesNo]

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

CREATE FUNCTION [dbo].[fnProfileHazardYesNo] (@String varchar(5000))
RETURNS varchar(3)
 AS  
BEGIN 
declare @c varchar(3)

IF ( Left(@String,1) = '1')
	SET @C = "Yes"
ELSE
	SET @C = "No"
Return @C
END

GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLabTestForm]](../../../Views/dbo_vwRptLabTestForm.md)
* [[dbo].[fnSelectOneLabTest]](../Table-valued_Functions/dbo_fnSelectOneLabTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

