#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnToPoundsDesc

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnToPoundsDesc]

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
| @ManifestQty | varchar(255) | 255 |
| @ManifestUnits | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnToPoundsDesc] (@ManifestQty  varchar(255),@ManifestUnits varchar(255))  
RETURNS varchar(255)
 AS  
BEGIN 

declare @return varchar(255)

if @ManifestUnits = 'Barrel'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Drums'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Totes'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Cubic Meters'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Yards'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Large Totes'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Small Totes'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Buckets'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Pails'
	Set @return = 'Pounds'
else if @ManifestUnits = 'Gallons'
	Set @return = 'Pounds'
else
	Set @return = @ManifestUnits

Return @return

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

