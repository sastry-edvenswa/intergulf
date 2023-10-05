#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnTrailerLastLoadId

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnTrailerLastLoadId]

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
| @TrailerId | varchar(30) | 30 |


---

## <a name="#sqlscript"></a>SQL Script

```sql



CREATE FUNCTION [dbo].[fnTrailerLastLoadId] (@TrailerId as Varchar(30))

RETURNS varchar(3000)
AS
BEGIN

Declare @Customer as Varchar(3000)
Declare @Location as Varchar(3000)
Declare @LocationStatus as Varchar(3000)
Declare @LoadId as Varchar(100)
Declare @Date as Varchar(3000)
Declare @Time as Varchar(3000)
Declare @MaterialDescription as Varchar(3000)
Declare @Return	as Varchar(3000)

DECLARE curDB CURSOR FAST_FORWARD FOR

SELECT TOP (1) dbo.Equipment.TrailerCustomerDescription, dbo.Equipment.Location, dbo.Equipment.LocationStatus, dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Profile.TrailerLastLoadDescription FROM dbo.Loads LEFT OUTER JOIN dbo.Equipment ON dbo.Loads.TrailerId = dbo.Equipment.Id LEFT OUTER JOIN dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id WHERE (dbo.Loads.DispatchStatus <> 'Pending') AND (LEN(dbo.Loads.TrailerId) > 0) AND (dbo.Equipment.Id = @TrailerId) ORDER BY dbo.Loads.ScheduledDate DESC, dbo.Loads.ScheduledTime DESC

OPEN curDB

FETCH NEXT FROM curDB INTO @Customer, @Location, @LocationStatus, @LoadId, @Date, @Time, @MaterialDescription

WHILE @@FETCH_STATUS = 0

BEGIN

	FETCH NEXT FROM curDB INTO @Customer, @Location, @LocationStatus, @LoadId, @Date, @Time, @MaterialDescription

END

CLOSE curDB

DEALLOCATE curDB

If Len(@LoadId) > 0 
	SET @Return = @LoadId
else
	Set @Return = 'Not Found'

Return  @Return

END

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Equipment]](../../../Tables/dbo_Equipment.md)
* [[dbo].[Loads]](../../../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../../../Tables/dbo_Profile.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadId]](../../../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadId.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

