#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnLoadQuantityToGallons

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnLoadQuantityToGallons]

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
| @Qty | decimal(15,0) | 9 |
| @Units | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnLoadQuantityToGallons] (@Qty Decimal(15,0),@Units varchar(255))  
RETURNS Decimal(15,0)
 AS  
BEGIN 

declare @return Decimal(15,0)

if len(@Qty) > 0
	if @Units = 'Gallons'
		Set @return = Cast(@Qty as Decimal(15,0))
	else if @Units = 'Barrels'
		Set @return = Cast(@Qty * 42 as Decimal(15,0))
	else if @Units = 'Drums'
		Set @return = Cast(@Qty * 55 as Decimal(15,0))
	else if @Units = 'Totes'
		Set @return = Cast(@Qty * 275 as Decimal(15,0))
	else if @Units = 'Cubic Meters'
		Set @return = Cast(@Qty * 6.3 * 42 as Decimal(15,0))
	else if @Units = 'Pounds'
		Set @return = Cast(@Qty / 8.33 as Decimal(15,0))
	else if @Units = 'Yards'
		Set @return = Cast(@Qty * 202 as Decimal(15,0))
	else if @Units = 'Large Totes'
		Set @return = Cast(@Qty * 330 as Decimal(15,0))
	else if @Units = 'Small Totes'
		Set @return = Cast(@Qty * 275 as Decimal(15,0))
	else if @Units = 'Buckets'
		Set @return = Cast(@Qty * 5 as Decimal(15,0))
	else if @Units = 'Pails'
		Set @return = Cast(@Qty * 5 as Decimal(15,0))
	else
		Set @return = Cast(@Qty as Decimal(15,0))
else
	Set @return = Cast(0 as Decimal(15,0))

Return @return

END
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../../../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)
* [[dbo].[vwSelectProfileVolumeQuantity]](../../../Views/dbo_vwSelectProfileVolumeQuantity.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

