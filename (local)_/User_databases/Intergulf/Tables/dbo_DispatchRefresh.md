#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.DispatchRefresh

# ![Tables](../../../../Images/Table32.png) [dbo].[DispatchRefresh]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 3 |
| Created | 4:02:06 PM Monday, March 26, 2007 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_DispatchRefresh: Name](../../../../Images/pkcluster.png)](#indexes) | Name | varchar(50) | 50 | NOT NULL |
|  | Refresh | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_DispatchRefresh: Name](../../../../Images/pkcluster.png)](#indexes) | PK_DispatchRefresh | Name | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[DispatchRefresh]
(
[Name] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Refresh] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[DispatchRefresh] ADD CONSTRAINT [PK_DispatchRefresh] PRIMARY KEY CLUSTERED ([Name]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

