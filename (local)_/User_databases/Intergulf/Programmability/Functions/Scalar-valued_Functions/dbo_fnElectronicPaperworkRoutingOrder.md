#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnElectronicPaperworkRoutingOrder

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnElectronicPaperworkRoutingOrder]

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
| @SentBillingDepartment | varchar(30) | 30 |
| @SentSalesPersonId | varchar(30) | 30 |
| @SentDestinationId | varchar(30) | 30 |


---

## <a name="#sqlscript"></a>SQL Script

```sql


CREATE FUNCTION [dbo].[fnElectronicPaperworkRoutingOrder] (@SentBillingDepartment as Varchar(30),@SentSalesPersonId as Varchar(30),@SentDestinationId as Varchar(30))

RETURNS varchar(3000)
AS
BEGIN

Declare @BillingDepartment as Varchar(3000)
Declare @SalesPersonId as Varchar(3000)
Declare @DestinationId as Varchar(3000)
Declare @BillingPersonId as Varchar(3000)
Declare @BillingOrder as Varchar(3000)
Declare @Return	as Varchar(3000)

DECLARE curDB CURSOR FAST_FORWARD FOR

SELECT dbo.vwSelectElectronicPaperworkRoutingOrder.BillingDepartment,dbo.vwSelectElectronicPaperworkRoutingOrder.SalesPersonId, dbo.vwSelectElectronicPaperworkRoutingOrder.DestinationId, dbo.vwSelectElectronicPaperworkRoutingOrder.BillingPersonId, dbo.vwSelectElectronicPaperworkRoutingOrder.BillingOrder from dbo.vwSelectElectronicPaperworkRoutingOrder where dbo.vwSelectElectronicPaperworkRoutingOrder.BillingDepartment = @SentBillingDepartment ORDER BY dbo.vwSelectElectronicPaperworkRoutingOrder.BillingDepartment, dbo.vwSelectElectronicPaperworkRoutingOrder.BillingOrder DESC

OPEN curDB 

FETCH NEXT FROM curDB INTO @BillingDepartment, @SalesPersonId, @DestinationId, @BillingPersonId, @BillingOrder

WHILE @@FETCH_STATUS = 0

BEGIN

	FETCH NEXT FROM curDB INTO @BillingDepartment, @SalesPersonId, @DestinationId, @BillingPersonId, @BillingOrder

	If @BillingOrder = 4
		If @SentSalesPersonId = @SalesPersonId And @SentDestinationId = @DestinationId
			SET @Return = @BillingPersonId
		else
			SET @Return = 'Unassigned'
	else If @BillingOrder = 3
		If @SentDestinationId = @DestinationId
			SET @Return = @BillingPersonId
		else
			SET @Return = 'Unassigned'
	else if @BillingOrder = 2
		If @SentSalesPersonId = @SalesPersonId
			SET @Return = @BillingPersonId
		else
			SET @Return = 'Unassigned'
	else If @BillingOrder = 1
		SET @Return = @BillingPersonId
	else If @BillingOrder = 0
		SET @Return = 'Unassigned'
	else
		Set @Return = 'Not Found'

END

Bottom:

CLOSE curDB

DEALLOCATE curDB

if @Return IS NULL
	SET @Return = 'Error'

Return  @Return

END
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[vwSelectElectronicPaperworkRoutingOrder]](../../../Views/dbo_vwSelectElectronicPaperworkRoutingOrder.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

