#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnBillingRout

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnBillingRout]

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
| @BillingDepartment | varchar(300) | 300 |
| @SalesPersonId | varchar(300) | 300 |
| @DestinationId | varchar(300) | 300 |
| @BillingPersonId | varchar(300) | 300 |
| @BillingRoutingOrder | varchar(300) | 300 |


---

## <a name="#sqlscript"></a>SQL Script

```sql




CREATE FUNCTION [dbo].[fnBillingRout] (@BillingDepartment as Varchar(300),@SalesPersonId as Varchar(300),@DestinationId as Varchar(300),@BillingPersonId as Varchar(300),@BillingRoutingOrder as Varchar(300))

RETURNS varchar(300)
AS
BEGIN

/*
Declare @BillingDepartment as Varchar(3000)
Declare @SalesPersonId as Varchar(3000)
Declare @DestinationId as Varchar(3000)
Declare @BillingPersonId as Varchar(3000)
Declare @BillingRoutingOrder as Varchar(3000)
*/

Declare @Return	as Varchar(3000)

DECLARE curDB CURSOR FAST_FORWARD FOR

--SELECT dbo.ElectronicPaperworkRouting.BillingDepartment, dbo.ElectronicPaperworkRouting.SalesPersonId, dbo.ElectronicPaperworkRouting.DestinationId, dbo.ElectronicPaperworkRouting.BillingPersonId, dbo.fnBillingRoutingOrder(BillingDepartment, SalesPersonId,DestinationId, BillingPersonId) AS BillingRoutingOrder FROM dbo.ElectronicPaperworkRouting WHERE (BillingDepartment = @BillingDepartment) ORDER BY BillingRoutingOrder DESC

SELECT dbo.vwSelectElectronicPaperworkRoutingUpdate.BillingDepartment, dbo.vwSelectElectronicPaperworkRoutingUpdate.SalesPersonId, dbo.vwSelectElectronicPaperworkRoutingUpdate.DestinationId, dbo.vwSelectElectronicPaperworkRoutingUpdate.BillingPersonId, dbo.vwSelectElectronicPaperworkRoutingUpdate.BillingOrder FROM dbo.vwSelectElectronicPaperworkRoutingUpdate WHERE (BillingDepartment = @BillingDepartment) ORDER BY BillingOrder DESC

OPEN curDB 

FETCH NEXT FROM curDB INTO @BillingDepartment, @SalesPersonId, @DestinationId, @BillingPersonId, @BillingRoutingOrder

WHILE @@FETCH_STATUS = 0

BEGIN

	FETCH NEXT FROM curDB INTO @BillingDepartment, @SalesPersonId, @DestinationId, @BillingPersonId, @BillingRoutingOrder

/*
	if @BillingRoutingOrder = 4
		Set @return = @BillingPersonId
	else if @BillingRoutingOrder = 3
		Set @return = @BillingPersonId
	else if @BillingRoutingOrder = 2
		Set @return = @BillingPersonId
	else if @BillingRoutingOrder = 1
		Set @return = @BillingPersonId
	else if @BillingRoutingOrder = 0
		goto Done
*/

	if @BillingRoutingOrder = 4
		Set @return = @BillingRoutingOrder
	else if @BillingRoutingOrder = 3
		Set @return = @BillingRoutingOrder
	else if @BillingRoutingOrder = 2
		Set @return = @BillingRoutingOrder
	else if @BillingRoutingOrder = 1
		Set @return = @BillingRoutingOrder
	else if @BillingRoutingOrder = 0
		goto Done


END

Done:

CLOSE curDB

DEALLOCATE curDB

Bottom:

Return  @Return

END
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

