#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnSelectLoadTanks

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnSelectLoadTanks]

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
| @Id | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE  FUNCTION [dbo].[fnSelectLoadTanks] (@Id as bigint)

RETURNS varchar(30)
AS
BEGIN

DECLARE @Tank as varchar(30)
DECLARE @Tanks as varchar(30)

SET @Tanks = ''

DECLARE curDB CURSOR FAST_FORWARD FOR

       SELECT Tank
       FROM dbo.LabTestDisbursement
       WHERE [LabTestId] = @Id

OPEN curDB

FETCH NEXT FROM curDB INTO @Tank

WHILE @@FETCH_STATUS = 0

BEGIN

	if len(@Tanks) = 0
		SET @Tanks =  @Tank
	else
		SET @Tanks = @Tanks + ',' + @Tank

    FETCH NEXT FROM curDB INTO @Tank

END

CLOSE curDB

DEALLOCATE curDB

RETURN @Tanks 

END

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTestDisbursement]](../../../Tables/dbo_LabTestDisbursement.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadMaterialGeneratorKStarks]](../../../Views/dbo_vwRptLoadMaterialGeneratorKStarks.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarksProfileNo]](../../../Views/dbo_vwRptLoadMaterialGeneratorKStarksProfileNo.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

