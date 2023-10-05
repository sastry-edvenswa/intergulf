#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.AutoClose

# ![Tables](../../../../Images/Table32.png) [dbo].[AutoClose]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 9 |
| Created | 6:47:33 PM Monday, January 29, 2007 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_AutoClose: Id](../../../../Images/pkcluster.png)](#indexes) | Id | varchar(50) | 50 | NOT NULL |
|  | AutoClose | varchar(1) | 1 | NULL allowed |
|  | Path | varchar(100) | 100 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_AutoClose: Id](../../../../Images/pkcluster.png)](#indexes) | PK_AutoClose | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[AutoClose]
(
[Id] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[AutoClose] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Path] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[AutoClose] ADD CONSTRAINT [PK_AutoClose] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

