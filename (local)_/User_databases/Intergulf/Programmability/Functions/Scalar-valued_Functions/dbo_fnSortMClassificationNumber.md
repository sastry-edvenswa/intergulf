#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnSortMClassificationNumber

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnSortMClassificationNumber]

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
| @Id | varchar(9) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO
CREATE FUNCTION [dbo].[fnSortMClassificationNumber] (@Id varchar(9))  
RETURNS numeric(9)
 AS  
BEGIN 
declare @return varchar(9)
Return  right(@id,len(@id)-1)
END


GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

