#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Tasks

# ![Tables](../../../../Images/Table32.png) [dbo].[Tasks]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 11 |
| Created | 10:09:01 PM Sunday, September 17, 2017 |
| Last Modified | 10:09:01 PM Sunday, September 17, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Tasks: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | TaskName | varchar(200) | 200 | NULL allowed |  |
|  | Frequency | varchar(50) | 50 | NULL allowed |  |
|  | Interval | int | 4 | NULL allowed |  |
|  | RunDate | date | 3 | NULL allowed |  |
|  | RunMonth | int | 4 | NULL allowed |  |
|  | RunWeek | int | 4 | NULL allowed |  |
|  | RunDay | int | 4 | NULL allowed |  |
|  | RunHour | int | 4 | NULL allowed |  |
|  | RunMinute | int | 4 | NULL allowed |  |
|  | LastRun | varchar(50) | 50 | NULL allowed |  |
|  | NextRunDate | date | 3 | NULL allowed |  |
|  | NextRunMonth | int | 4 | NULL allowed |  |
|  | NextRunWeek | int | 4 | NULL allowed |  |
|  | NextRunDay | int | 4 | NULL allowed |  |
|  | NextRunHour | int | 4 | NULL allowed |  |
|  | NextRunMinute | int | 4 | NULL allowed |  |
|  | Status | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Tasks: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Tasks | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Tasks]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[TaskName] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Frequency] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Interval] [int] NULL,
[RunDate] [date] NULL,
[RunMonth] [int] NULL,
[RunWeek] [int] NULL,
[RunDay] [int] NULL,
[RunHour] [int] NULL,
[RunMinute] [int] NULL,
[LastRun] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NextRunDate] [date] NULL,
[NextRunMonth] [int] NULL,
[NextRunWeek] [int] NULL,
[NextRunDay] [int] NULL,
[NextRunHour] [int] NULL,
[NextRunMinute] [int] NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Tasks] ADD CONSTRAINT [PK_Tasks] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectTasks]](../Views/dbo_vwSelectTasks.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

