#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsScheduleColors

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsScheduleColors]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 10 |
| Created | 4:41:40 PM Monday, January 11, 2016 |
| Last Modified | 11:50:49 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsScheduleColors: Id](../../../../Images/pkcluster.png)](#indexes) | Id | varchar(50) | 50 | NOT NULL |
|  | ColorNumber | numeric(18,0) | 9 | NULL allowed |
|  | SortOrder | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LoadsScheduleColors: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LoadsScheduleColors | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsScheduleColors]
(
[Id] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[ColorNumber] [numeric] (18, 0) NULL,
[SortOrder] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsScheduleColors] ADD CONSTRAINT [PK_LoadsScheduleColors] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

