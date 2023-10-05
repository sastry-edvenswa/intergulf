#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectCustomerForSaturn

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectCustomerForSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:25:15 PM Thursday, December 15, 2022 |
| Last Modified | 4:25:15 PM Thursday, December 15, 2022 |


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
| SageCustomerNumber | varchar(20) | 20 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectCustomerForSaturn]
AS
SELECT        Id, Name, Address, City, State, Zip, SageCustomerNumber
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

