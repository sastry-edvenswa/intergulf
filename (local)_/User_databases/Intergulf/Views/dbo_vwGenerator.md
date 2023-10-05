#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwGenerator

# ![Views](../../../../Images/View32.png) [dbo].[vwGenerator]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 1:00:45 AM Saturday, February 10, 2007 |
| Last Modified | 8:20:19 PM Thursday, July 27, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | numeric(18,0) | 9 |
| Name | varchar(100) | 100 |
| Address | varchar(3000) | 3000 |
| City | varchar(50) | 50 |
| State | varchar(50) | 50 |
| Zip | varchar(50) | 50 |
| BillingName | varchar(100) | 100 |
| BillingAddress | varchar(3000) | 3000 |
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
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwGenerator]
AS
SELECT        Id, Name, Address, City, State, Zip, BillingName, BillingAddress, BillingCity, BillingState, BillingZip, Contact, Phone, Fax, Email, RegistrationNo, EpaIdNo, Type, Classification, UpdateDateTime, UpdateUser, 
                         UpdateComputer
FROM            dbo.fnSelectGenerator() AS fnSelectGenerator
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

