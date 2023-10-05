#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnSelectProfileVolume

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnSelectProfileVolume]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @profileId | bigint | 8 |
| @beginDate | datetime | 8 |
| @endDate | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE FUNCTION [dbo].[fnSelectProfileVolume] 
(
	@profileId bigint,
	@beginDate datetime, 
	@endDate datetime
)
RETURNS Decimal(15,2)
AS
BEGIN
	DECLARE @Result Decimal(15,2)

	select
		@Result = sum(dbo.fnLoadManifestQuantityToGallons(lt.Quantity, lt.Units))
	from
		Loads ld
	left join
		LabTest lt on lt.LoadId = ld.Id
	where
		ld.ProfileId = @profileId
		and ld.ScheduledDate between @beginDate and dateadd(s, 86399, @endDate)
		and isnull(lt.Quantity, 0) > 0

	RETURN @Result
END

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../../../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../../../Tables/dbo_Loads.md)
* [[dbo].[fnLoadManifestQuantityToGallons]](dbo_fnLoadManifestQuantityToGallons.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectExportProfileVolume]](../../../Views/dbo_vwSelectExportProfileVolume.md)
* [[dbo].[vwSelectProfileVolumeTest]](../../../Views/dbo_vwSelectProfileVolumeTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

