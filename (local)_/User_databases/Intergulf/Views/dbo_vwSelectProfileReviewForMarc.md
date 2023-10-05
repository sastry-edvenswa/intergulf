#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileReviewForMarc

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileReviewForMarc]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:37:47 PM Thursday, August 10, 2017 |
| Last Modified | 11:37:47 PM Thursday, August 10, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ReviewProfileId | bigint | 8 |
| Id | bigint | 8 |
| UserId | varchar(50) | 50 |
| ReviewUserStatus | varchar(20) | 20 |
| ProfileReviewStatus | varchar(20) | 20 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| Customer Id | numeric(18,0) | 9 |
| Generator Id | numeric(18,0) | 9 |
| Generator Address | varchar(3000) | 3000 |
| Profile Number | varchar(50) | 50 |
| SortOrder | numeric(18,0) | 9 |
| ProfileId | bigint | 8 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| ReviewDate | datetime | 8 |
| ProfileType | varchar(50) | 50 |
| ReviewProfileType | varchar(15) | 15 |
| CreateDateTime | datetime | 8 |
| ReviewTime | datetime | 8 |
| Comments | varchar(500) | 500 |
| ProfileInReviewUsersId | bigint | 8 |
| BackupFirstName | varchar(50) | 50 |
| BackupLastName | varchar(50) | 50 |
| ActualFirstName | varchar(50) | 50 |
| ActualLastName | varchar(50) | 50 |
| CurrentProfileReviewer | varchar(50) | 50 |
| CurrentProfileReviewerFirstName | varchar(50) | 50 |
| CurrentProfileReviewerLastName | varchar(50) | 50 |
| BackupProfileReviewerUserName | varchar(50) | 50 |
| ActualProfileReviewer | varchar(50) | 50 |
| ActualProfileReviewerFirstName | varchar(50) | 50 |
| ActualProfileReviewerLastName | varchar(50) | 50 |
| ReviewerUserId | varchar(50) | 50 |
| Status | varchar(20) | 20 |
| Hold | bit | 1 |
| Department | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfileReviewForMarc]
AS
SELECT        TOP (100) PERCENT dbo.ProfileInReview.ReviewProfileId, dbo.ProfileInReview.ProfileId AS Id, dbo.ProfileInReviewUsers.UserId, 
                         dbo.ProfileInReviewUsers.Status AS ReviewUserStatus, dbo.ProfileInReview.Status AS ProfileReviewStatus, dbo.Generator.Name AS [Generator Name], 
                         dbo.Customer.Name AS [Customer Name], dbo.Profile.WasteCode, dbo.Profile.MaterialDescription, dbo.Customer.Id AS [Customer Id], 
                         dbo.Generator.Id AS [Generator Id], dbo.Generator.Address AS [Generator Address], dbo.Profile.ProfileNumber AS [Profile Number], 
                         dbo.ProfileInReviewUsers.SortOrder, dbo.ProfileInReviewUsers.ProfileId, dbo.UserMaster.FirstName, dbo.UserMaster.LastName, 
                         dbo.ProfileInReviewUsers.ReviewDate, dbo.Profile.ProfileType, 
                         CASE WHEN dbo.Profile.ProfileType = 'Product' THEN 'Product' ELSE 'Recycle / Waste' END AS ReviewProfileType, dbo.ProfileInReviewUsers.CreateDateTime, 
                         dbo.ProfileInReviewUsers.ReviewTime, dbo.ProfileInReviewUsers.Comments, dbo.ProfileInReviewUsers.Id AS ProfileInReviewUsersId, 
                         UserMaster_1.FirstName AS BackupFirstName, UserMaster_1.LastName AS BackupLastName, UserMaster_2.FirstName AS ActualFirstName, 
                         UserMaster_2.LastName AS ActualLastName, 
                         CASE WHEN dbo.UserMaster.UseBackupReviewer = 1 THEN dbo.UserMaster.BackupProfileReviewerUserName ELSE UserId END AS CurrentProfileReviewer, 
                         CASE WHEN dbo.UserMaster.UseBackupReviewer = 1 THEN UserMaster_1.FirstName ELSE dbo.UserMaster.FirstName END AS CurrentProfileReviewerFirstName, 
                         CASE WHEN dbo.UserMaster.UseBackupReviewer = 1 THEN UserMaster_1.LastName ELSE dbo.UserMaster.LastName END AS CurrentProfileReviewerLastName, 
                         dbo.UserMaster.BackupProfileReviewerUserName, CASE WHEN LEN(ReviewerUserId) 
                         > 0 THEN ReviewerUserId ELSE CASE WHEN dbo.UserMaster.UseBackupReviewer = 1 THEN dbo.UserMaster.BackupProfileReviewerUserName ELSE UserId END END
                          AS ActualProfileReviewer, CASE WHEN LEN(ReviewerUserId) 
                         > 0 THEN UserMaster_2.FirstName ELSE CASE WHEN dbo.UserMaster.UseBackupReviewer = 1 THEN UserMaster_1.FirstName ELSE dbo.UserMaster.FirstName END
                          END AS ActualProfileReviewerFirstName, CASE WHEN LEN(ReviewerUserId) 
                         > 0 THEN UserMaster_2.LastName ELSE CASE WHEN dbo.UserMaster.UseBackupReviewer = 1 THEN UserMaster_1.LastName ELSE dbo.UserMaster.LastName END
                          END AS ActualProfileReviewerLastName, dbo.ProfileInReviewUsers.ReviewerUserId, dbo.Profile.Status, dbo.ProfileInReviewUsers.Hold, 
                         dbo.ProfileInReviewUsers.Department, dbo.ProfileInReviewUsers.BillingDepartment
FROM            dbo.UserMaster AS UserMaster_2 RIGHT OUTER JOIN
                         dbo.ProfileInReviewUsers ON UserMaster_2.UserName = dbo.ProfileInReviewUsers.ReviewerUserId LEFT OUTER JOIN
                         dbo.UserMaster AS UserMaster_1 INNER JOIN
                         dbo.UserMaster ON UserMaster_1.UserName = dbo.UserMaster.BackupProfileReviewerUserName ON 
                         dbo.ProfileInReviewUsers.UserId = dbo.UserMaster.UserName RIGHT OUTER JOIN
                         dbo.Profile LEFT OUTER JOIN
                         dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id RIGHT OUTER JOIN
                         dbo.ProfileInReview ON dbo.Profile.Id = dbo.ProfileInReview.ProfileId ON dbo.ProfileInReviewUsers.ReviewProfileId = dbo.ProfileInReview.ReviewProfileId
WHERE        (dbo.Profile.ProfileNumber = '07815')
ORDER BY dbo.ProfileInReviewUsers.SortOrder

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ProfileInReview]](../Tables/dbo_ProfileInReview.md)
* [[dbo].[ProfileInReviewUsers]](../Tables/dbo_ProfileInReviewUsers.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

