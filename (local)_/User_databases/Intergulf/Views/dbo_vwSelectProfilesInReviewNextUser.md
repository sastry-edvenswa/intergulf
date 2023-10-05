#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfilesInReviewNextUser

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfilesInReviewNextUser]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:40:21 PM Monday, May 26, 2014 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ProfileId | bigint | 8 |
| UserId | varchar(50) | 50 |
| ReviewDate | datetime | 8 |
| ReviewTime | datetime | 8 |
| SortOrder | numeric(18,0) | 9 |
| ReviewUserStatus | varchar(20) | 20 |
| Customer Name | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(3000) | 3000 |
| Profile Number | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| Customer Id | bigint | 8 |
| Generator Id | bigint | 8 |
| Status | varchar(20) | 20 |
| Id | bigint | 8 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| Department | varchar(50) | 50 |
| ReviewProfileType | varchar(50) | 50 |
| ReviewProfileId | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfilesInReviewNextUser]
AS
SELECT     TOP 100 PERCENT dbo.ProfileInReviewUsers.ProfileId, dbo.ProfileInReviewUsers.UserId, dbo.ProfileInReviewUsers.ReviewDate, 
                      dbo.ProfileInReviewUsers.ReviewTime, dbo.ProfileInReviewUsers.SortOrder, dbo.ProfileInReviewUsers.Status AS ReviewUserStatus, 
                      dbo.Customer.Name AS [Customer Name], dbo.Generator.Name AS [Generator Name], dbo.Generator.Address AS [Generator Address], 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Profile.ProfileType, dbo.Profile.WasteCode, dbo.Profile.MaterialDescription, 
                      dbo.Profile.CustomerId AS [Customer Id], dbo.Profile.GeneratorId AS [Generator Id], dbo.ProfileInReview.Status, dbo.Profile.Id, 
                      dbo.UserMaster.FirstName, dbo.UserMaster.LastName, dbo.ProfileInReviewUsers.CreateDateTime, dbo.ProfileReviewUsers.Department, 
                      dbo.ProfileReviewUsers.ProfileType AS ReviewProfileType, dbo.ProfileInReviewUsers.ReviewProfileId
FROM         dbo.ProfileInReview RIGHT OUTER JOIN
                      dbo.UserMaster INNER JOIN
                      dbo.ProfileInReviewUsers ON dbo.UserMaster.UserName = dbo.ProfileInReviewUsers.UserId INNER JOIN
                      dbo.ProfileReviewUsers ON dbo.ProfileInReviewUsers.UserId = dbo.ProfileReviewUsers.UserId ON 
                      dbo.ProfileInReview.ReviewProfileId = dbo.ProfileInReviewUsers.ReviewProfileId LEFT OUTER JOIN
                      dbo.Profile ON dbo.ProfileInReviewUsers.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id LEFT OUTER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id
ORDER BY dbo.ProfileInReviewUsers.ProfileId, dbo.ProfileInReviewUsers.SortOrder

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ProfileInReview]](../Tables/dbo_ProfileInReview.md)
* [[dbo].[ProfileInReviewUsers]](../Tables/dbo_ProfileInReviewUsers.md)
* [[dbo].[ProfileReviewUsers]](../Tables/dbo_ProfileReviewUsers.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

