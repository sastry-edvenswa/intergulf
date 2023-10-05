#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileReviewUsers

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileReviewUsers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:39:56 PM Monday, May 26, 2014 |
| Last Modified | 8:07:17 PM Tuesday, September 17, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| UserId | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| Department | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| BackupFirstName | varchar(50) | 50 |
| BackupLastName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfileReviewUsers]
AS
SELECT        TOP (100) PERCENT dbo.ProfileReviewUsers.UserId, dbo.UserMaster.FirstName, dbo.UserMaster.LastName, dbo.ProfileReviewUsers.Department, dbo.ProfileReviewUsers.BillingDepartment, 
                         dbo.ProfileReviewUsers.ProfileType, UserMaster_1.FirstName AS BackupFirstName, UserMaster_1.LastName AS BackupLastName
FROM            dbo.UserMaster AS UserMaster_1 RIGHT OUTER JOIN
                         dbo.UserMaster ON UserMaster_1.UserName = dbo.UserMaster.BackupProfileReviewerUserName RIGHT OUTER JOIN
                         dbo.ProfileReviewUsers ON dbo.UserMaster.UserName = dbo.ProfileReviewUsers.UserId
ORDER BY dbo.UserMaster.LastName, dbo.UserMaster.FirstName
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ProfileReviewUsers]](../Tables/dbo_ProfileReviewUsers.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

