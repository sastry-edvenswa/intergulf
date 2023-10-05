#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnProperShippingName

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnProperShippingName]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @Key | varchar(100) | 100 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnProperShippingName] (@Key varchar(100))  
RETURNS varchar(5000)
 AS  
BEGIN

	declare @IsRQ varchar(1)
	declare @UnNumber varchar(20)
	declare @IsWaste varchar(1)
	declare @PreProperShippingName varchar(2000)
	declare @ProperShippingName varchar(2000)
	declare @Constituents varchar(2000)
	declare @Constituents1 varchar(2000)
	declare @Constituents2 varchar(2000)
	declare @Hazmat varchar(10)
	declare @HazardClass varchar(200)
	declare @PackingGroup varchar(200)
	declare @PostProperShippingName varchar(2000)
	
	declare @Return varchar(5000)
	
	SELECT @IsRQ = IsRQ  FROM MaterialCode WHERE Id = @Key
	SELECT @UnNumber = ProductPlacardNumber  FROM MaterialCode WHERE Id = @Key
	SELECT @IsWaste = IsWaste  FROM MaterialCode WHERE Id = @Key
	SELECT @PreProperShippingName = PreProperShippingName FROM MaterialCode WHERE Id = @Key
	SELECT @ProperShippingName = ProperShippingName FROM MaterialCode WHERE Id = @Key
	SELECT @Constituents1 = Constituents1 FROM MaterialCode WHERE Id = @Key
	SELECT @Constituents2 = Constituents2 FROM MaterialCode WHERE Id = @Key
	SELECT @Hazmat = Hazmat FROM MaterialCode WHERE Id = @Key
	SELECT @HazardClass = ProductHazardClass FROM MaterialCode WHERE Id = @Key
	SELECT @PackingGroup = ProductPackingGroup FROM MaterialCode WHERE Id = @Key
	SELECT @PostProperShippingName = PostProperShippingName FROM MaterialCode WHERE Id = @Key

	Set @Return = 
		Case
		When @IsRQ = 1
		Then 'RQ'
		Else 'x'
		End;

	Set @Return =
		Case
		When  @Return <> 'x' and Len(@UnNumber) > 0
		Then @Return + ', ' + @UnNumber
		When  @Return <> 'x' and Len(@UnNumber) = 0
		Then @Return
		When @Return = 'x' and Len(@UnNumber) > 0
		Then @UnNumber
		Else 'x'
		End;

	Set @Return =
		Case
		When  @Return <> 'x' and @IsWaste = 1
		Then @Return + ', ' + 'Waste'
		When  @Return <> 'x' and @IsWaste <> 1
		Then @Return
		When @Return = 'x' and @IsWaste = 1
		Then 'Waste'
		Else 'x'
		End;

	Set @Return =
		Case
		When  @Return <> 'x' and Len(@PreProperShippingName) > 0
		Then @Return + ', ' + @PreProperShippingName
		When  @Return <> 'x' and Len(@PreProperShippingName) = 0
		Then @Return
		When @Return = 'x' and Len(@PreProperShippingName) > 0
		Then @PreProperShippingName
		Else 'x'
		End;

	Set @Return =
		Case
		When  @Return <> 'x' and Len(@ProperShippingName) > 0
		Then @Return + ', ' + @ProperShippingName
		When  @Return <> 'x' and Len(@ProperShippingName) = 0
		Then @Return
		When @Return = 'x' and Len(@ProperShippingName) > 0
		Then @ProperShippingName
		Else 'x'
		End;

	Set @Constituents =
		Case
		When Len(@Constituents1) > 0 and Len(@Constituents2) > 0
		Then '(' + @Constituents1 + ', ' + @Constituents2 + ')'
		When Len(@Constituents1) > 0 and  Len(@Constituents2) = 0
		Then '(' + @Constituents1 + ')'
		When Len(@Constituents1) = 0 and Len(@Constituents2) > 0
		Then '(' + @Constituents2 + ')'
		Else 'x'
		End;

	Set @Return =
		Case
		When  @Return <> 'x' and @Constituents <> 'x'
		Then @Return + ', ' + @Constituents
		Else @Return
		End;

	Set @Return =
		Case
		When  @Return <> 'x' and @Hazmat = 'X'
		Then @Return + ', ' + @HazardClass + ', PG ' + @PackingGroup
		Else @Return
		End;

	Set @Return =
		Case
		When  @Return <> 'x' and Len(@PostProperShippingName) > 0
		Then @Return + ', ' + @PostProperShippingName
		When  @Return <> 'x' and Len(@PostProperShippingName) = 0
		Then @Return
		When @Return = 'x' and Len(@PostProperShippingName) > 0
		Then @PostProperShippingName
		Else 'x'
		End;

	Return  @Return

END














































































































GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[MaterialCode]](../../../Tables/dbo_MaterialCode.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfile]](../../../Views/dbo_vwChooseProfile.md)
* [[dbo].[vwRptLoadBOL]](../../../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadManifest]](../../../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadTCEQ]](../../../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptProfileBol]](../../../Views/dbo_vwRptProfileBol.md)
* [[dbo].[vwRptProfileManifest]](../../../Views/dbo_vwRptProfileManifest.md)
* [[dbo].[vwRptProfileTCEQ]](../../../Views/dbo_vwRptProfileTCEQ.md)
* [[dbo].[vwSelectEManifest]](../../../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectProfilesWithErrors]](../../../Views/dbo_vwSelectProfilesWithErrors.md)
* [[dbo].[vwSelectReviewProfileProperShippingName]](../../../Views/dbo_vwSelectReviewProfileProperShippingName.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

