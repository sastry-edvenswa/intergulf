#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsScheduleDefaultResources

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsScheduleDefaultResources]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1 |
| Created | 11:10:56 PM Monday, April 25, 2016 |
| Last Modified | 11:50:49 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsScheduleDefaultResources: Id](../../../../Images/pkcluster.png)](#indexes) | Id | varchar(50) | 50 | NOT NULL |
|  | ShiftOne | varchar(100) | 100 | NULL allowed |
|  | ShiftTwo | varchar(100) | 100 | NULL allowed |
|  | Lunch | varchar(100) | 100 | NULL allowed |
|  | CreateUser | varchar(50) | 50 | NULL allowed |
|  | CreateDateTime | datetime | 8 | NULL allowed |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LoadsScheduleDefaultResources: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LoadsScheduleDefaultResources | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsScheduleDefaultResources]
(
[Id] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[ShiftOne] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ShiftTwo] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Lunch] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsScheduleDefaultResources] ADD CONSTRAINT [PK_LoadsScheduleDefaultResources] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

