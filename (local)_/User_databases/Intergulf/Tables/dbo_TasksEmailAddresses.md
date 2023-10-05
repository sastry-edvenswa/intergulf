#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.TasksEmailAddresses

# ![Tables](../../../../Images/Table32.png) [dbo].[TasksEmailAddresses]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 9 |
| Created | 10:09:28 PM Sunday, September 17, 2017 |
| Last Modified | 10:09:28 PM Sunday, September 17, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TasksEmailAddresses: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | TaskName | varchar(50) | 50 | NULL allowed |  |
|  | EmailAddress | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TasksEmailAddresses: Id](../../../../Images/pkcluster.png)](#indexes) | PK_TasksEmailAddresses | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[TasksEmailAddresses]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[TaskName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EmailAddress] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[TasksEmailAddresses] ADD CONSTRAINT [PK_TasksEmailAddresses] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

