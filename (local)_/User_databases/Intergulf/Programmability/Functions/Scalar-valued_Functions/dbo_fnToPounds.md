#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnToPounds

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnToPounds]

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
| @ManifestQty | numeric(10,0) | 9 |
| @ManifestUnits | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnToPounds] (@ManifestQty  numeric(10,0),@ManifestUnits varchar(255))  
RETURNS numeric(10,0)
 AS  
BEGIN 

declare @return numeric(10,0)

if @ManifestUnits = 'Barrel'
	Set @return = @ManifestQty * 42 * 8.33
else if @ManifestUnits = 'Drums'
	Set @return = @ManifestQty * 55 * 8.33
else if @ManifestUnits = 'Totes'
	Set @return = @ManifestQty * 250 * 8.33
else if @ManifestUnits = 'Cubic Meters'
	Set @return = @ManifestQty * 6.3 * 42 * 8.33
else if @ManifestUnits = 'Yards'
	Set @return = @ManifestQty * 202 * 8.33
else if @ManifestUnits = 'Large Totes'
	Set @return = @ManifestQty * 330 * 8.33
else if @ManifestUnits = 'Small Totes'
	Set @return = @ManifestQty * 275 * 8.33
else if @ManifestUnits = 'Buckets'
	Set @return = @ManifestQty * 5 * 8.33
else if @ManifestUnits = 'Pails'
	Set @return = @ManifestQty * 5 * 8.33
else if @ManifestUnits = 'Gallons'
	Set @return = @ManifestQty * 8.33
else
	Set @return = @ManifestQty

Return format(@return ,"###0")

END


GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectExportLoadsForSteers]](../../../Views/dbo_vwSelectExportLoadsForSteers.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

