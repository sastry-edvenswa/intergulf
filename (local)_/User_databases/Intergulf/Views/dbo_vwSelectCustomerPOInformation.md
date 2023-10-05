#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectCustomerPOInformation

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectCustomerPOInformation]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:42:12 PM Sunday, February 28, 2021 |
| Last Modified | 7:43:00 PM Sunday, February 28, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| PoRequired | int | 4 |  |
| PoNumber | varchar(50) | 50 |  |
| PoNumberExpirationDate | date | 3 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectCustomerPOInformation]
AS
SELECT        Id, PoRequired, PoNumber, PoNumberExpirationDate
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

