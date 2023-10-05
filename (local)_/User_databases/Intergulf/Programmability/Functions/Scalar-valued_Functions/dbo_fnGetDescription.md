#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnGetDescription

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnGetDescription]

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
| @MaterialDescription | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO
CREATE FUNCTION [dbo].[fnGetDescription] (@MaterialDescription varchar(255))  
RETURNS varchar(255)
 AS  
BEGIN 
declare @return varchar(255)
Return  replace(@Materialdescription,char(13)+char(10)," ")
END


GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwProfileGrid]](../../../Views/dbo_vwProfileGrid.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

