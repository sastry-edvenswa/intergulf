#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectCustomerAll

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectCustomerAll]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:11:12 PM Thursday, June 6, 2019 |
| Last Modified | 4:38:13 PM Thursday, June 6, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| Name | varchar(50) | 50 |  |
| Address | varchar(50) | 50 |  |
| City | varchar(50) | 50 |  |
| State | varchar(50) | 50 |  |
| Zip | varchar(50) | 50 |  |
| BillingName | varchar(50) | 50 |  |
| BillingAddress | varchar(50) | 50 |  |
| BillingCity | varchar(50) | 50 |  |
| BillingState | varchar(50) | 50 |  |
| BillingZip | varchar(50) | 50 |  |
| Contact | varchar(50) | 50 |  |
| Phone | varchar(50) | 50 |  |
| Fax | varchar(50) | 50 |  |
| Email | varchar(50) | 50 |  |
| RegistrationNo | varchar(50) | 50 |  |
| EpaIdNo | varchar(50) | 50 |  |
| Type | varchar(50) | 50 |  |
| Classification | varchar(50) | 50 |  |
| MaterialDisbursement | int | 4 |  |
| CustomerStop | bit | 1 |  |
| CompanyId | varchar(25) | 25 |  |
| SageCustomerNumber | varchar(20) | 20 |  |
| Active | varchar(30) | 30 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectCustomerAll]
AS
SELECT        Id, Name, Address, City, State, Zip, BillingName, BillingAddress, BillingCity, BillingState, BillingZip, Contact, Phone, Fax, Email, RegistrationNo, EpaIdNo, Type, Classification, MaterialDisbursement, 
                         CustomerStop, CompanyId, SageCustomerNumber, dbo.fnSelectCustomerActiveProfile(Id) AS Active
FROM            dbo.Customer
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[fnSelectCustomerActiveProfile]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSelectCustomerActiveProfile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

