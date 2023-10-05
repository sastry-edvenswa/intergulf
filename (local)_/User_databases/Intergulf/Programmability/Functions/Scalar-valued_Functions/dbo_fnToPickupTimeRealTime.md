#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnToPickupTimeRealTime

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnToPickupTimeRealTime]

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
| @PickupTime | varchar(30) | 30 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO


CREATE FUNCTION [dbo].[fnToPickupTimeRealTime] (@Direction as Varchar(30),@PickupTime as Varchar(30))
RETURNS Varchar(30)
 AS  
BEGIN 

declare @return Varchar(30)


	if @Direction = 'In Bound'
		Set @return = @PickupTime
	else if @Direction = 'Out Bound'
		Set @return = 0
	else
		Set @return = 999


Return @return

END

GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectExportLoadArrivalTimePerformance]](../../../Views/dbo_vwSelectExportLoadArrivalTimePerformance.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

