#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileInReview

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileInReview]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 4229 |
| Created | 7:38:05 PM Monday, May 26, 2014 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileInReview: ReviewProfileId](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_stat_1719677174_2_6_1](../../../../Images/Index.png)](#indexes) | ReviewProfileId | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes _dta_stat_1719677174_2_6_1](../../../../Images/Index.png)](#indexes) | ProfileId | bigint | 8 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_stat_1719677174_2_6_1](../../../../Images/Index.png)](#indexes) | Status | varchar(20) | 20 | NULL allowed |  |
|  | ReviewCompletedDate | datetime | 8 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfileInReview: ReviewProfileId](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileInReview | ReviewProfileId | YES |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_1719677174_2_6_1 | ProfileId, Status, ReviewProfileId |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileInReview]
(
[ReviewProfileId] [bigint] NOT NULL IDENTITY(1, 1),
[ProfileId] [bigint] NULL,
[CreateDateTime] [datetime] NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReviewCompletedDate] [datetime] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileInReview] ADD CONSTRAINT [PK_ProfileInReview] PRIMARY KEY CLUSTERED ([ReviewProfileId]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_1719677174_2_6_1] ON [dbo].[ProfileInReview] ([ProfileId], [Status], [ReviewProfileId])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectProfileReviewForMarc]](../Views/dbo_vwSelectProfileReviewForMarc.md)
* [[dbo].[vwSelectProfilesInReview]](../Views/dbo_vwSelectProfilesInReview.md)
* [[dbo].[vwSelectProfilesInReviewNextReviewUser]](../Views/dbo_vwSelectProfilesInReviewNextReviewUser.md)
* [[dbo].[vwSelectProfilesInReviewNextUser]](../Views/dbo_vwSelectProfilesInReviewNextUser.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

