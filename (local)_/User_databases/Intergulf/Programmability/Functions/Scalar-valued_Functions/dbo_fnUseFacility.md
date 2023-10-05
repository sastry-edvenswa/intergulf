#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnUseFacility

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnUseFacility]

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
| @DestinationFacility | varchar(255) | 255 |
| @GeneratorFacility | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnUseFacility] (@DestinationFacility  varchar(255),@GeneratorFacility varchar(255))  
RETURNS varchar(255)
 AS  
BEGIN 

declare @return varchar(255)

if len(@DestinationFacility) > 0
	Set @return = @DestinationFacility
else
	if len(@GeneratorFacility) > 0
		Set @return = @GeneratorFacility
	else
		Set @return = null

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

