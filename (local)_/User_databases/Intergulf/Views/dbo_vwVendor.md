#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwVendor

# ![Views](../../../../Images/View32.png) [dbo].[vwVendor]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:42:13 AM Saturday, February 10, 2007 |
| Last Modified | 12:28:41 PM Tuesday, October 4, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Mas90Id | varchar(50) | 50 |
| Name | varchar(50) | 50 |
| Address | varchar(300) | 300 |
| City | varchar(100) | 100 |
| State | varchar(50) | 50 |
| Zip | varchar(50) | 50 |
| PaymentName | varchar(50) | 50 |
| PaymentAddress | varchar(300) | 300 |
| PaymentCity | varchar(100) | 100 |
| PaymentState | varchar(50) | 50 |
| PaymentZip | varchar(50) | 50 |
| Contact | varchar(50) | 50 |
| Phone | varchar(50) | 50 |
| Fax | varchar(50) | 50 |
| Email | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |
| ShortName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwVendor]
AS
SELECT        Id, Mas90Id, Name, Address, City, State, Zip, PaymentName, PaymentAddress, PaymentCity, PaymentState, PaymentZip, Contact, Phone, Fax, Email, UpdateDateTime, UpdateUser, UpdateComputer, 
                         ShortName
FROM            dbo.fnSelectVendor() AS fnSelectVendor
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectVendor]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectVendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

