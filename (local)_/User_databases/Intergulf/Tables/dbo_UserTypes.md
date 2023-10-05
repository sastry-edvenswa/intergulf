#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.UserTypes

# ![Tables](../../../../Images/Table32.png) [dbo].[UserTypes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 5 |
| Created | 6:47:38 PM Monday, January 29, 2007 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_UserTypes: UserTypes](../../../../Images/pkcluster.png)](#indexes) | UserTypes | varchar(50) | 50 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_UserTypes: UserTypes](../../../../Images/pkcluster.png)](#indexes) | PK_UserTypes | UserTypes | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[UserTypes]
(
[UserTypes] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[UserTypes] ADD CONSTRAINT [PK_UserTypes] PRIMARY KEY CLUSTERED ([UserTypes]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

