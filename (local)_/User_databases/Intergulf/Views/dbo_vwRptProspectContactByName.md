#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProspectContactByName

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProspectContactByName]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:21:13 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ProspectId | numeric(18,0) | 9 |
| ContactId | numeric(18,0) | 9 |
| Name | varchar(50) | 50 |
| Phone | varchar(50) | 50 |
| Email | varchar(50) | 50 |
| Notes | varchar(5000) | 5000 |
| CategoryName | varchar(50) | 50 |
| DepartmentName | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptProspectContactByName]
AS
SELECT     TOP 100 PERCENT dbo.ProspectContact.ProspectId, dbo.ProspectContact.ContactId, dbo.ProspectContact.Name, dbo.ProspectContact.Phone, 
                      dbo.ProspectContact.Email, dbo.ProspectContact.Notes, dbo.ProspectCategory.Name AS CategoryName, 
                      dbo.ProspectDepartment.Name AS DepartmentName, dbo.UserMaster.FirstName, dbo.UserMaster.LastName
FROM         dbo.ProspectContact INNER JOIN
                      dbo.ProspectCategory ON dbo.ProspectContact.CategoryId = dbo.ProspectCategory.Id INNER JOIN
                      dbo.ProspectDepartment ON dbo.ProspectContact.DepartmentId = dbo.ProspectDepartment.Id INNER JOIN
                      dbo.UserMaster ON dbo.ProspectContact.SalesPersonId = dbo.UserMaster.UserName
ORDER BY dbo.ProspectContact.Name
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ProspectCategory]](../Tables/dbo_ProspectCategory.md)
* [[dbo].[ProspectContact]](../Tables/dbo_ProspectContact.md)
* [[dbo].[ProspectDepartment]](../Tables/dbo_ProspectDepartment.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

