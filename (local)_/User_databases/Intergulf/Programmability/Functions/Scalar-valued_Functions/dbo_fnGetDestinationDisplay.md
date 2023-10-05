#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnGetDestinationDisplay

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnGetDestinationDisplay]

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
| @Destination | varchar(255) | 255 |
| @Facility | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO
CREATE FUNCTION [dbo].[fnGetDestinationDisplay] (@Destination varchar(255),@Facility varchar(255))  
RETURNS varchar(255)
 AS  
BEGIN 
declare @return varchar(255)

If  @Facility = null or len(@Facility) = 0
	Set @Return = @Destination
else
	Set @Return = @Facility + " - " + @Destination

Return  @return
END
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfile]](../../../Views/dbo_vwChooseProfile.md)
* [[dbo].[vwDestination]](../../../Views/dbo_vwDestination.md)
* [[dbo].[vwSelectLoads]](../../../Views/dbo_vwSelectLoads.md)
* [[dbo].[vwSelectPendingLoads]](../../../Views/dbo_vwSelectPendingLoads.md)
* [[dbo].[vwSelectRequestedLoads]](../../../Views/dbo_vwSelectRequestedLoads.md)
* [[dbo].[vwSelectScheduledLoads]](../../../Views/dbo_vwSelectScheduledLoads.md)
* [[dbo].[fnSelectProfileGlobalSearch]](../Table-valued_Functions/dbo_fnSelectProfileGlobalSearch.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

