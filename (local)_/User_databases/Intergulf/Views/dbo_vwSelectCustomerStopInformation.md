#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectCustomerStopInformation

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectCustomerStopInformation]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 6:00:35 PM Sunday, April 30, 2017 |
| Last Modified | 6:00:35 PM Sunday, April 30, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| CustomerId | bigint | 8 |
| CustomerName | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectCustomerStopInformation]
AS
SELECT        dbo.Loads.Id, dbo.Profile.CustomerId, dbo.Customer.Name AS CustomerName, dbo.UserMaster.FirstName, dbo.UserMaster.LastName, 
                         dbo.Profile.SalesPersonId
FROM            dbo.UserMaster INNER JOIN
                         dbo.Loads ON dbo.UserMaster.UserName = dbo.Loads.SalesPersonId LEFT OUTER JOIN
                         dbo.Customer INNER JOIN
                         dbo.Profile ON dbo.Customer.Id = dbo.Profile.CustomerId ON dbo.Loads.ProfileId = dbo.Profile.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

