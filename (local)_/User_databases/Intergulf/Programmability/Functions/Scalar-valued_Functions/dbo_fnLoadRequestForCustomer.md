#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnLoadRequestForCustomer

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnLoadRequestForCustomer]

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
| @String | varchar(3) | 3 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


CREATE FUNCTION [dbo].[fnLoadRequestForCustomer] (@String varchar(3))
RETURNS varchar(3)
 AS  
BEGIN 
declare @c varchar(3)

IF @String = Null
	SET @C = "No"
ELSE
	SET @C = @String
Return @C
END


GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectRequestedLoads]](../../../Views/dbo_vwSelectRequestedLoads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

