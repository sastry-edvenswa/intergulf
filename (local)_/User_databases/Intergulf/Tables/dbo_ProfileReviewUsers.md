#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileReviewUsers

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileReviewUsers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 74 |
| Created | 7:38:38 PM Monday, May 26, 2014 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileReviewUsers: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | UserId | varchar(50) | 50 | NULL allowed |  |
|  | Department | varchar(50) | 50 | NULL allowed |  |
|  | BillingDepartment | varchar(50) | 50 | NULL allowed |  |
|  | ProfileType | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfileReviewUsers: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileReviewUsers | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileReviewUsers]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[UserId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Department] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingDepartment] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileReviewUsers] ADD CONSTRAINT [PK_ProfileReviewUsers] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectProfileReviewUsers]](../Views/dbo_vwSelectProfileReviewUsers.md)
* [[dbo].[vwSelectProfilesInReviewNextUser]](../Views/dbo_vwSelectProfilesInReviewNextUser.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

