#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectElectronicPaperworkRoutingOrder

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectElectronicPaperworkRoutingOrder]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:57:30 AM Wednesday, January 2, 2019 |
| Last Modified | 4:54:23 PM Thursday, February 7, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| BillingDepartment | varchar(50) | 50 |  |
| SalesPersonId | varchar(50) | 50 |  |
| DestinationId | bigint | 8 |  |
| BillingPersonId | varchar(50) | 50 |  |
| BillingOrder | numeric(1,0) | 5 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectElectronicPaperworkRoutingOrder]
AS
SELECT        TOP (100) PERCENT Id, BillingDepartment, SalesPersonId, DestinationId, BillingPersonId, dbo.fnBillingRoutingOrder(BillingDepartment, SalesPersonId, DestinationId, BillingPersonId) AS BillingOrder
FROM            dbo.ElectronicPaperworkRouting
ORDER BY BillingOrder DESC
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ElectronicPaperworkRouting]](../Tables/dbo_ElectronicPaperworkRouting.md)
* [[dbo].[fnBillingRoutingOrder]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnBillingRoutingOrder.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[fnElectronicPaperworkRoutingOrder]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnElectronicPaperworkRoutingOrder.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

