#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnToPickupTimeRealTimeToggle

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnToPickupTimeRealTimeToggle]

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
| @Direction | varchar(30) | 30 |
| @Nothing | varchar | 1 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


CREATE FUNCTION [dbo].[fnToPickupTimeRealTimeToggle] (@Direction as Varchar(30),@Nothing as Varchar(1))
RETURNS numeric(10,0)
 AS  
BEGIN 

declare @return numeric(10,0)


	if @Direction = 'In Bound'
		Set @return = 1
	else if @Direction = 'Out Bound'
		Set @return = 0
	else
		Set @return = 999


Return @return

END

GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

