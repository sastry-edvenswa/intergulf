#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwCustomer

# ![Views](../../../../Images/View32.png) [dbo].[vwCustomer]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:38:49 AM Saturday, February 10, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | numeric(18,0) | 9 |
| Name | varchar(50) | 50 |
| Address | varchar(50) | 50 |
| City | varchar(50) | 50 |
| State | varchar(50) | 50 |
| Zip | varchar(50) | 50 |
| BillingName | varchar(50) | 50 |
| BillingAddress | varchar(50) | 50 |
| BillingCity | varchar(50) | 50 |
| BillingState | varchar(50) | 50 |
| BillingZip | varchar(50) | 50 |
| Contact | varchar(50) | 50 |
| Phone | varchar(50) | 50 |
| Fax | varchar(50) | 50 |
| Email | varchar(50) | 50 |
| RegistrationNo | varchar(50) | 50 |
| EpaIdNo | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| Classification | varchar(50) | 50 |
| MaterialDisbursement | int | 4 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwCustomer]
AS
SELECT     fnSelectCustomer.*
FROM         dbo.fnSelectCustomer() fnSelectCustomer
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCustomer.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

