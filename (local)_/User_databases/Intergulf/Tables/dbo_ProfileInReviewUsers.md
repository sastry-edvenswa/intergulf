#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileInReviewUsers

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileInReviewUsers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 35903 |
| Created | 7:38:13 PM Monday, May 26, 2014 |
| Last Modified | 3:58:22 PM Tuesday, February 5, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileInReviewUsers: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | ProfileId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_ProfileInReviewUsers_5_1751677288__K3_K11_K4_6, _dta_stat_1751677288_3_6_4, _dta_stat_1751677288_3_4, _dta_stat_1751677288_11_3_6_4, _dta_stat_1751677288_11_3_4](../../../../Images/Index.png)](#indexes)(5) | ReviewProfileId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_ProfileInReviewUsers_5_1751677288__K3_K11_K4_6, _dta_stat_1751677288_3_6_4, _dta_stat_1751677288_3_4, _dta_stat_1751677288_11_3_6_4, _dta_stat_1751677288_11_3_4, _dta_stat_1751677288_11_4](../../../../Images/Index.png)](#indexes)(6) | UserId | varchar(50) | 50 | NULL allowed |  |
|  | BackupUserId | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_ProfileInReviewUsers_5_1751677288__K3_K11_K4_6, _dta_stat_1751677288_3_6_4, _dta_stat_1751677288_11_3_6_4](../../../../Images/Index.png)](#indexes)(3) | ReviewerUserId | varchar(50) | 50 | NULL allowed |  |
|  | ReviewDate | datetime | 8 | NULL allowed |  |
|  | ReviewTime | datetime | 8 | NULL allowed |  |
|  | Comments | varchar(500) | 500 | NULL allowed |  |
|  | SortOrder | numeric(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_ProfileInReviewUsers_5_1751677288__K3_K11_K4_6, _dta_stat_1751677288_11_3_6_4, _dta_stat_1751677288_11_3_4, _dta_stat_1751677288_11_4](../../../../Images/Index.png)](#indexes)(4) | Status | varchar(20) | 20 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |
|  | Hold | bit | 1 | NULL allowed |  |
|  | Department | varchar(50) | 50 | NULL allowed |  |
|  | BillingDepartment | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileInReviewUsers: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileInReviewUsers | Id |  | YES |
|  | _dta_index_ProfileInReviewUsers_5_1751677288__K3_K11_K4_6 | ReviewProfileId, Status, UserId | ReviewerUserId |  |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_1751677288_11_3_4 | Status, ReviewProfileId, UserId |
| _dta_stat_1751677288_11_3_6_4 | Status, ReviewProfileId, ReviewerUserId, UserId |
| _dta_stat_1751677288_11_4 | Status, UserId |
| _dta_stat_1751677288_3_4 | ReviewProfileId, UserId |
| _dta_stat_1751677288_3_6_4 | ReviewProfileId, ReviewerUserId, UserId |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileInReviewUsers]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[ProfileId] [bigint] NULL,
[ReviewProfileId] [bigint] NULL,
[UserId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BackupUserId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReviewerUserId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReviewDate] [datetime] NULL,
[ReviewTime] [datetime] NULL,
[Comments] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SortOrder] [numeric] (18, 0) NULL,
[Status] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Hold] [bit] NULL,
[Department] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingDepartment] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileInReviewUsers] ADD CONSTRAINT [PK_ProfileInReviewUsers] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_ProfileInReviewUsers_5_1751677288__K3_K11_K4_6] ON [dbo].[ProfileInReviewUsers] ([ReviewProfileId], [Status], [UserId]) INCLUDE ([ReviewerUserId]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_1751677288_3_6_4] ON [dbo].[ProfileInReviewUsers] ([ReviewProfileId], [ReviewerUserId], [UserId])
GO
CREATE STATISTICS [_dta_stat_1751677288_3_4] ON [dbo].[ProfileInReviewUsers] ([ReviewProfileId], [UserId])
GO
CREATE STATISTICS [_dta_stat_1751677288_11_3_6_4] ON [dbo].[ProfileInReviewUsers] ([Status], [ReviewProfileId], [ReviewerUserId], [UserId])
GO
CREATE STATISTICS [_dta_stat_1751677288_11_3_4] ON [dbo].[ProfileInReviewUsers] ([Status], [ReviewProfileId], [UserId])
GO
CREATE STATISTICS [_dta_stat_1751677288_11_4] ON [dbo].[ProfileInReviewUsers] ([Status], [UserId])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectProfileReviewForMarc]](../Views/dbo_vwSelectProfileReviewForMarc.md)
* [[dbo].[vwSelectProfilesInReviewNextReviewUser]](../Views/dbo_vwSelectProfilesInReviewNextReviewUser.md)
* [[dbo].[vwSelectProfilesInReviewNextUser]](../Views/dbo_vwSelectProfilesInReviewNextUser.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

