#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnProfileEPAWasteCodes

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnProfileEPAWasteCodes]

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
| @EPAWC1 | varchar(10) | 10 |
| @EPAWC2 | varchar(10) | 10 |
| @EPAWC3 | varchar(10) | 10 |
| @EPAWC4 | varchar(10) | 10 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnProfileEPAWasteCodes] (@EPAWC1 varchar(10),@EPAWC2 varchar(10),@EPAWC3 varchar(10),@EPAWC4 varchar(10))  
RETURNS varchar(50)
 AS  
BEGIN 
declare @return varchar(50)
Return  LTRIM(RTrim(@EPAWC1 + char(10) + @EPAWC2 + char(10) + @EPAWC3 +  char(10) + @EPAWC4))
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

