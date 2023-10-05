#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwProfilesActiveNoMSDS

# ![Views](../../../../Images/View32.png) [dbo].[vwProfilesActiveNoMSDS]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:30:58 PM Thursday, May 16, 2013 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LastName | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| Id | bigint | 8 |
| GeneratorName | varchar(100) | 100 |
| CustomerName | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ProfileType | varchar(50) | 50 |
| Status | varchar(20) | 20 |
| MSDSFileName | varchar(600) | 600 |
| Expr1 | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwProfilesActiveNoMSDS]
AS
SELECT     TOP 100 PERCENT dbo.UserMaster.LastName, dbo.UserMaster.FirstName, dbo.Profile.Id, dbo.Generator.Name AS GeneratorName, 
                      dbo.Customer.Name AS CustomerName, dbo.Profile.ProfileNumber, dbo.Profile.WasteCode, dbo.Profile.MaterialDescription, dbo.Profile.ProfileType, 
                      dbo.Profile.Status, dbo.Profile.MSDSFileName, LEN(COALESCE (dbo.Profile.MSDSFileName, '')) AS Expr1
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.Profile.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
WHERE     (LEN(COALESCE (dbo.Profile.MSDSFileName, '')) = 0) AND (dbo.Profile.Status = 'Active') AND (dbo.Profile.ProfileType <> 'Waste')
ORDER BY dbo.UserMaster.LastName, dbo.Generator.Name, dbo.Profile.ProfileType

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

