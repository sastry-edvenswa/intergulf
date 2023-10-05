#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileForSales

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileForSales]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:09:32 PM Monday, March 19, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Name | varchar(100) | 100 |
| Address | varchar(3000) | 3000 |
| City | varchar(50) | 50 |
| State | varchar(50) | 50 |
| Contact | varchar(50) | 50 |
| Phone | varchar(50) | 50 |
| Fax | varchar(50) | 50 |
| Email | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ProcessDescription | varchar(3000) | 3000 |
| ProductCategory | varchar(50) | 50 |
| Status | varchar(20) | 20 |
| SalesPersonId | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfileForSales]
AS
SELECT     TOP 100 PERCENT dbo.Generator.Name, dbo.Generator.Address, dbo.Generator.City, dbo.Generator.State, dbo.Generator.Contact, 
                      dbo.Generator.Phone, dbo.Generator.Fax, dbo.Generator.Email, dbo.Profile.ProfileType, dbo.Profile.ProfileNumber, dbo.Profile.MaterialDescription, 
                      dbo.Profile.ProcessDescription, dbo.Profile.ProductCategory, dbo.Profile.Status, dbo.Profile.SalesPersonId, dbo.UserMaster.FirstName, 
                      dbo.UserMaster.LastName
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.Profile.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
ORDER BY dbo.Generator.Name

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

