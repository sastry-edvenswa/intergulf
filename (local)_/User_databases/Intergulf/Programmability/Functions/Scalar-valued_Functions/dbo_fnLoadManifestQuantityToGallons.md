#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnLoadManifestQuantityToGallons

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnLoadManifestQuantityToGallons]

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
| @ManifestQty | decimal(15,2) | 9 |
| @ManifestUnits | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnLoadManifestQuantityToGallons] (@ManifestQty  Decimal(15,2),@ManifestUnits varchar(255))  
RETURNS Decimal(15,2)
 AS  
BEGIN 

declare @return Decimal(15,2)

if len(@ManifestQty) > 0
	if @ManifestUnits = 'Gallons'
		Set @return = Cast(@ManifestQty as Decimal)
	else if @ManifestUnits = 'Barrels'
		Set @return = Cast(@ManifestQty * 42 as Decimal)
	else if @ManifestUnits = 'Drums'
		Set @return = Cast(@ManifestQty * 55 as Decimal)
	else if @ManifestUnits = 'Totes'
		Set @return = Cast(@ManifestQty * 275 as Decimal)
	else if @ManifestUnits = 'Cubic Meters'
		Set @return = Cast(@ManifestQty * 6.3 * 42 as Decimal)
	else if @ManifestUnits = 'Pounds'
		Set @return = Cast(@ManifestQty / 8.33 as Decimal)
	else if @ManifestUnits = 'Yards'
		Set @return = Cast(@ManifestQty * 202 as Decimal)
	else if @ManifestUnits = 'Large Totes'
		Set @return = Cast(@ManifestQty * 330 as Decimal)
	else if @ManifestUnits = 'Small Totes'
		Set @return = Cast(@ManifestQty * 275 as Decimal)
	else if @ManifestUnits = 'Buckets'
		Set @return = Cast(@ManifestQty * 5 as Decimal)
	else if @ManifestUnits = 'Pails'
		Set @return = Cast(@ManifestQty * 5 as Decimal)
	else
		Set @return = Cast(@ManifestQty as Decimal)
else
	Set @return = Cast(0 as Decimal)

Return @return

END
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[fnSelectProfileVolume]](dbo_fnSelectProfileVolume.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

