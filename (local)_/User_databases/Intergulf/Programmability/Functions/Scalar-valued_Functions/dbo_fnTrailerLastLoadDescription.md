#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnTrailerLastLoadDescription

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnTrailerLastLoadDescription]

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


CREATE FUNCTION [dbo].[fnTrailerLastLoadDescription] (@TrailerId as Varchar(30))

RETURNS varchar(3000)
AS
BEGIN

Declare @LastLocationStatus as Varchar(3000)
Declare @Customer as Varchar(3000)
Declare @Location as Varchar(3000)
Declare @LocationStatus as Varchar(3000)
Declare @Date as Varchar(3000)
Declare @Time as Varchar(3000)
Declare @MaterialDescription as Varchar(3000)
Declare @Return	as Varchar(3000)

DECLARE curDB CURSOR FAST_FORWARD FOR

SELECT TOP (1) dbo.Equipment.LastLocationStatus, dbo.Equipment.TrailerCustomerDescription, dbo.Equipment.Location, dbo.Equipment.LocationStatus, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Profile.TrailerLastLoadDescription FROM dbo.Loads LEFT OUTER JOIN dbo.Equipment ON dbo.Loads.TrailerId = dbo.Equipment.Id LEFT OUTER JOIN dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id WHERE (dbo.Loads.DispatchStatus = 'Scheduled' Or dbo.Loads.DispatchStatus = 'Complete' Or dbo.Loads.DispatchStatus = 'Loaded') AND (LEN(dbo.Loads.TrailerId) > 0) AND (dbo.Equipment.Id = @TrailerId) AND (ScheduledDate <= GetDate()) ORDER BY dbo.Loads.ScheduledDate DESC, dbo.Loads.ScheduledTime DESC

OPEN curDB 

FETCH NEXT FROM curDB INTO @LastLocationStatus, @Customer, @Location, @LocationStatus, @Date, @Time, @MaterialDescription

WHILE @@FETCH_STATUS = 0

BEGIN

	FETCH NEXT FROM curDB INTO @LastLocationStatus, @Customer, @Location, @LocationStatus, @Date, @Time, @MaterialDescription

END

CLOSE curDB

DEALLOCATE curDB

If @Location = 'Customer'
	SET @Return = @Customer
else If @LocationStatus = 'Clean'
	SET @Return = @LocationStatus
else if @LocationStatus = 'Ready'
	if @LastLocationStatus = 'Clean'
		SET @Return = 'Ready Clean'
	else if Len(@MaterialDescription) > 0 
		SET @Return = @MaterialDescription
	else
	Set @Return = 'Not Found'
else If Len(@MaterialDescription) > 0 
	SET @Return = @MaterialDescription
else
	Set @Return = 'Not Found'

Bottom:

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

* [[dbo].[vwSelectEquipmentActiveTrailers]](../../../Views/dbo_vwSelectEquipmentActiveTrailers.md)
* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadDescriptionOld]](../../../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadDescriptionOld.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

