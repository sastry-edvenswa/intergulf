#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsScheduleControl

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsScheduleControl]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1 |
| Created | 2:22:20 PM Thursday, December 17, 2015 |
| Last Modified | 11:50:49 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadScheduleControl: Name](../../../../Images/pkcluster.png)](#indexes) | Name | varchar(50) | 50 | NOT NULL |
|  | Locked | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LoadScheduleControl: Name](../../../../Images/pkcluster.png)](#indexes) | PK_LoadScheduleControl | Name | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsScheduleControl]
(
[Name] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Locked] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsScheduleControl] ADD CONSTRAINT [PK_LoadScheduleControl] PRIMARY KEY CLUSTERED ([Name]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

