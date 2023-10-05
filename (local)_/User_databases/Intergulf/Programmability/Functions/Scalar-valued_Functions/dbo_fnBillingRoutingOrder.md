#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fnBillingRoutingOrder

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fnBillingRoutingOrder]

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
| @BillingDepartment | varchar(300) | 300 |
| @SalesPersonId | varchar(300) | 300 |
| @DestinationId | varchar(300) | 300 |
| @BillingPersonId | varchar(300) | 300 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE FUNCTION [dbo].[fnBillingRoutingOrder] (@BillingDepartment as Varchar(300),@SalesPersonId as Varchar(300),@DestinationId as Varchar(300),@BillingPersonId as Varchar(300))

RETURNS numeric(1)
 AS  
BEGIN 

declare @return numeric(1)

if len(@BillingDepartment) > 0 and len(@SalesPersonId) > 0 and len(@DestinationId) > 0 and len(@BillingPersonId) > 0 
	Set @return = 4
else if len(@BillingDepartment) > 0 and len(@DestinationId) > 0 and len(@BillingPersonId) > 0 
	Set @return = 3
else if len(@BillingDepartment) > 0 and len(@SalesPersonId) > 0 and len(@BillingPersonId) > 0 
	Set @return = 2
else if len(@BillingDepartment) > 0 and len(@BillingPersonId) > 0
	Set @return = 1
else
	Set @return = 0

Return format(@return ,"###0")

END

GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectElectronicPaperworkRoutingOrder]](../../../Views/dbo_vwSelectElectronicPaperworkRoutingOrder.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

