#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProspectContact

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProspectContact]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:53:56 AM Tuesday, May 19, 2015 |
| Last Modified | 10:53:56 AM Tuesday, May 19, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| ProspectId | numeric(18,0) | 9 |  |
| FirstName | varchar(50) | 50 |  |
| LastName | varchar(50) | 50 |  |
| OfficePhone | varchar(50) | 50 |  |
| CellPhone | varchar(50) | 50 |  |
| Email | varchar(50) | 50 |  |
| Department | varchar(50) | 50 |  |
| Category | varchar(50) | 50 |  |
| SalesPersonFirstName | varchar(50) | 50 |  |
| SalesPersonLastName | varchar(50) | 50 |  |
| Notes | varchar(5000) | 5000 |  |
| OpportunityId | numeric(18,0) | 9 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProspectContact]
AS
SELECT     dbo.ProspectContact.Id, dbo.ProspectContact.ProspectId, dbo.ProspectContact.FirstName, dbo.ProspectContact.LastName, dbo.ProspectContact.OfficePhone, 
                      dbo.ProspectContact.CellPhone, dbo.ProspectContact.Email, dbo.ProspectDepartment.Name AS Department, dbo.ProspectCategory.Name AS Category, 
                      dbo.UserMaster.FirstName AS SalesPersonFirstName, dbo.UserMaster.LastName AS SalesPersonLastName, dbo.ProspectContact.Notes, 
                      dbo.ProspectContact.OpportunityId
FROM         dbo.ProspectContact LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.ProspectContact.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                      dbo.ProspectDepartment ON dbo.ProspectContact.DepartmentId = dbo.ProspectDepartment.Id LEFT OUTER JOIN
                      dbo.ProspectCategory ON dbo.ProspectContact.CategoryId = dbo.ProspectCategory.Id

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

