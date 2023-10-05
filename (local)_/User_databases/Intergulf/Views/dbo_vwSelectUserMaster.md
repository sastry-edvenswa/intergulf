#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectUserMaster

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectUserMaster]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:08:17 AM Wednesday, August 12, 2015 |
| Last Modified | 4:00:19 PM Wednesday, September 29, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| UserName | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| UserType | varchar(50) | 50 |
| UserPassword | varchar(50) | 50 |
| ProfileReviewerText | varchar(3) | 3 |
| BackupProfileReviewerText | varchar(3) | 3 |
| BackupProfileReviewerUserName | varchar(50) | 50 |
| BackupReviewerNameText | varchar(101) | 101 |
| ProfileReviewer | varchar(2) | 2 |
| BackupFirstName | varchar(50) | 50 |
| BackupLastName | varchar(50) | 50 |
| UseBackupReviewer | varchar(2) | 2 |
| ProspectEmail | varchar(3) | 3 |
| CSRep | varchar(3) | 3 |
| CSRPersonId | varchar(50) | 50 |
| CSRepName | varchar(101) | 101 |
| EManifestUser | varchar(3) | 3 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectUserMaster]
AS
SELECT        dbo.UserMaster.UserName, dbo.UserMaster.FirstName, dbo.UserMaster.LastName, dbo.UserMaster.UserType, dbo.UserMaster.UserPassword, 
                         CASE WHEN dbo.UserMaster.ProfileReviewer = 1 THEN 'Yes' ELSE 'No' END AS ProfileReviewerText, 
                         CASE WHEN dbo.UserMaster.BackupProfileReviewer = 1 THEN 'Yes' ELSE ' No' END AS BackupProfileReviewerText, dbo.UserMaster.BackupProfileReviewerUserName, 
                         UserMaster_1.FirstName + ' ' + UserMaster_1.LastName AS BackupReviewerNameText, dbo.UserMaster.ProfileReviewer, UserMaster_1.FirstName AS BackupFirstName, 
                         UserMaster_1.LastName AS BackupLastName, dbo.UserMaster.UseBackupReviewer, CASE WHEN dbo.UserMaster.ProspectEmail = 1 THEN 'Yes' ELSE 'No' END AS ProspectEmail, 
                         CASE WHEN dbo.UserMaster.CustomerServiceRep = 1 THEN 'Yes' ELSE 'No' END AS CSRep, dbo.UserMaster.CSRPersonId, UserMaster_2.FirstName + ' ' + UserMaster_2.LastName AS CSRepName, 
                         CASE WHEN dbo.UserMaster.EManifestUser = 1 THEN 'Yes' ELSE 'No' END AS EManifestUser
FROM            dbo.UserMaster LEFT OUTER JOIN
                         dbo.UserMaster AS UserMaster_2 ON dbo.UserMaster.CSRPersonId = UserMaster_2.UserName LEFT OUTER JOIN
                         dbo.UserMaster AS UserMaster_1 ON dbo.UserMaster.BackupProfileReviewerUserName = UserMaster_1.UserName
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

