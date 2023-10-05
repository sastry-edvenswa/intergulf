#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnIsTrailerLoaded

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnIsTrailerLoaded]

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



CREATE FUNCTION [dbo].[fnIsTrailerLoaded] (@TrailerId as Varchar(30))

RETURNS varchar(3)
AS
BEGIN

Declare @Id as bigint
Declare @YN as Varchar(3)

SET @YN = 'No'

DECLARE curDB CURSOR FAST_FORWARD FOR

       SELECT Id
       FROM dbo.Loads
       WHERE TrailerId = @TrailerId and DispatchStatus = 'Loaded'

OPEN curDB

FETCH NEXT FROM curDB INTO @Id

WHILE @@FETCH_STATUS = 0

BEGIN

	SET @YN = 'Yes'

	FETCH NEXT FROM curDB INTO @Id

END

CLOSE curDB

DEALLOCATE curDB

RETURN @YN 

END


GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../../../Tables/dbo_Loads.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadDescription]](../../../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadDescription.md)
* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadDescriptionOld]](../../../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadDescriptionOld.md)
* [[dbo].[vwSelectEquipmentNotInUse]](../../../Views/dbo_vwSelectEquipmentNotInUse.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

