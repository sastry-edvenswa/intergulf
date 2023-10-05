#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectCustomerStopAssignment

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectCustomerStopAssignment]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 5:59:54 PM Sunday, April 30, 2017 |
| Last Modified | 5:42:26 PM Wednesday, August 19, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| Name | varchar(100) | 100 |  |
| Address | varchar(3000) | 3000 |  |
| City | varchar(50) | 50 |  |
| State | varchar(50) | 50 |  |
| Zip | varchar(50) | 50 |  |
| BillingName | varchar(100) | 100 |  |
| BillingAddress | varchar(3000) | 3000 |  |
| BillingCity | varchar(50) | 50 |  |
| BillingState | varchar(50) | 50 |  |
| BillingZip | varchar(50) | 50 |  |
| CustomerStop | bit | 1 |  |
| SageCustomerNumber | varchar(20) | 20 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectCustomerStopAssignment]
AS
SELECT        Id, Name, Address, City, State, Zip, BillingName, BillingAddress, BillingCity, BillingState, BillingZip, CustomerStop, SageCustomerNumber
FROM            dbo.Customer
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

