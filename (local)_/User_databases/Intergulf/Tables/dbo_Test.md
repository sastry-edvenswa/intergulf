#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Test

# ![Tables](../../../../Images/Table32.png) [dbo].[Test]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 0 |
| Created | 10:15:07 PM Friday, February 1, 2008 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TestIn: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | Customer | varchar(50) | 50 | NULL allowed |  |
|  | Category | varchar(50) | 50 | NULL allowed |  |
|  | Test | varchar(10) | 10 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TestIn: Id](../../../../Images/pkcluster.png)](#indexes) | PK_TestIn | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Test]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[Customer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Category] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Test] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Test] ADD CONSTRAINT [PK_TestIn] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

