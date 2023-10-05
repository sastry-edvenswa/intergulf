#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileReviewDepartments

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileReviewDepartments]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 28 |
| Created | 7:38:24 PM Monday, May 26, 2014 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileReviewDepartments: Name\ProfileType](../../../../Images/pkcluster.png)](#indexes) | Name | varchar(50) | 50 | NOT NULL |
| [![Cluster Primary Key PK_ProfileReviewDepartments: Name\ProfileType](../../../../Images/pkcluster.png)](#indexes) | ProfileType | varchar(15) | 15 | NOT NULL |
|  | SortOrder | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfileReviewDepartments: Name\ProfileType](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileReviewDepartments | Name, ProfileType | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileReviewDepartments]
(
[Name] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[ProfileType] [varchar] (15) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[SortOrder] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileReviewDepartments] ADD CONSTRAINT [PK_ProfileReviewDepartments] PRIMARY KEY CLUSTERED ([Name], [ProfileType]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

