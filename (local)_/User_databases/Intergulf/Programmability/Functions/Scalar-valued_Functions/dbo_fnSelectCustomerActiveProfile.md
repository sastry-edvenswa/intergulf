#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnSelectCustomerActiveProfile

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnSelectCustomerActiveProfile]

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

CREATE  FUNCTION [dbo].[fnSelectCustomerActiveProfile] (@Id as bigint)

RETURNS varchar(30)
AS
BEGIN

DECLARE @Status as varchar(30)
DECLARE @YesNo as varchar(3)

SET @Status = ''
SET @YesNo = 'No'

DECLARE curDB CURSOR FAST_FORWARD FOR

       SELECT dbo.profile.Status
       FROM dbo.Profile
       WHERE [CustomerId] = @Id And [Status] <> 'InActive'

OPEN curDB

FETCH NEXT FROM curDB INTO @Status

if @Status = 'Active'
	SET @YesNo = 'Yes'
else
	SET @YesNo = 'No'

CLOSE curDB

DEALLOCATE curDB

RETURN @YesNo

END

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Profile]](../../../Tables/dbo_Profile.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectCustomerAll]](../../../Views/dbo_vwSelectCustomerAll.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

