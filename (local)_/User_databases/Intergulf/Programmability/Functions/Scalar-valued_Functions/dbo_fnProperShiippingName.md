#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnProperShiippingName

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnProperShiippingName]

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
| @Pre | varchar(5000) | 5000 |
| @Name | varchar(5000) | 5000 |
| @Post | varchar(5000) | 5000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO
CREATE FUNCTION [dbo].[fnProperShiippingName] (@Pre varchar(5000),@Name varchar(5000),@Post varchar(5000))  
RETURNS varchar(5000)
 AS  
BEGIN 
declare @return varchar(5000)
Return  LTRIM(RTrim(@pre + " " + @Name+ " " + @Post))
END
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

